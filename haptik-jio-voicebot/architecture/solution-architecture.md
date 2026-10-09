# Solution Architecture

## Flow 1: Recharge reminder (outbound, two-way voicebot)
```mermaid
flowchart TD
    A["Recharge expiry data from client"] --> B["Reminder due, for example 5 days before expiry"]
    B --> C["Exotel places outbound call to customer"]
    C --> D{"Customer answers?"}
    D -->|"Yes"| E["Voice carried over SIP trunk to Haptik bot"]
    E --> F["Two-way conversation: expiry reminder, offers and discounts"]
    D -->|"No"| G{"Attempts below 3?"}
    G -->|"Yes"| C
    G -->|"No"| H["Stop for this cycle"]
```

## Sequence: reminder call
```mermaid
sequenceDiagram
    participant Exotel
    participant Customer as Customer phone
    participant Bot as Haptik bot platform
    Exotel->>Customer: Outbound call
    Customer-->>Exotel: Answers
    Exotel->>Bot: Voice over SIP trunk
    Bot->>Customer: Recharge expiring, offer details (via SIP trunk and Exotel)
    Customer->>Bot: Questions about discounts (via Exotel and SIP trunk)
```

## Flow 2: Chat-to-callback (Jio Fiber)
```mermaid
sequenceDiagram
    participant Customer
    participant Chat as MyJio chatbot (Haptik)
    participant API as Exotel outbound call API
    Customer->>Chat: Chats and asks for a callback
    Chat->>API: Outbound call request with customer number and reference
    API->>Customer: Dials the customer
    Note over API,Customer: Reason for call carried through the reference from the chat
```

## Components
| Component | Owner | Role |
|---|---|---|
| Recharge data and customer list | Client (Jio / Haptik) | Decides who to call and when |
| Haptik chatbot and voicebot | Haptik | Holds the conversation |
| Exotel SIP trunk | Exotel | Carries two-way voice between the bot and the customer |
| Exotel outbound call API | Exotel | Places calls to customers, including chat-triggered callbacks |
| Customer phone / MyJio chat | Customer | Receives calls, starts chat |

## Design notes
- **SIP trunk over streaming:** lower cost and latency at very large scale
- **Two-way voice:** the customer can speak to the bot, not just listen
- **API-triggered callbacks:** a chat can turn into a call without agent involvement
- **Same design for SIM and Fiber:** one platform, two customer types

## Diagram files
_Add the original draw.io / PNG architecture diagram here if one exists._
