# Solution Architecture

## High-level flow
```mermaid
flowchart TD
    A["Customer calls the single Exotel number"] --> B["Exotel IVR"]
    B --> C["Plays order status: shipped or dispatched, delivery date"]
    C --> D{"Customer satisfied?"}
    D -->|"Yes"| E["Call ends"]
    D -->|"No, or wants a change"| F["Call routed to support team"]
    F --> G["Agent answers on laptop via WebRTC"]
    G --> H["Agent handles request: delivery address, product change"]
```

## Sequence
```mermaid
sequenceDiagram
    participant Customer
    participant Exotel as Exotel IVR
    participant Agent as Support agent (laptop, WebRTC)
    Customer->>Exotel: Calls single number
    Exotel->>Customer: Plays order status and delivery date
    Customer->>Exotel: Needs more help or a change
    Exotel->>Agent: Routes call over the internet (VoIP)
    Agent->>Customer: Talks to the customer and takes the request
```

## Components
| Component | Owner | Role |
|---|---|---|
| Website | Client | Promotes the single number |
| Exotel number and IVR | Exotel | Receives calls, plays order status, offers agent handover |
| Order information | Client | Source of status and delivery date |
| WebRTC calling | Exotel | Delivers calls to agents' browsers over the internet |
| Support team laptops | Client | Where agents answer calls |

## Design notes
- **IVR first:** routine queries are answered automatically
- **Human fallback:** customers can always reach a person
- **Browser-based agent calling:** agents use laptops and headsets, no mobile phones
- **Internet-based voice (VoIP):** call quality depends on the agent's internet connection

## Diagram files
_Add the original draw.io / PNG architecture diagram here if one exists._
