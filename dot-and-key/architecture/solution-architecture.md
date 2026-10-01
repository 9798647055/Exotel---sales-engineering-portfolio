# Solution Architecture

## High-level flow
```mermaid
flowchart TD
    A["Customer calls the single Exotel number"] --> B["Exotel captures caller number"]
    B --> C["Exotel sends number to Dot and Key API"]
    C --> D{"HTTP 200 OK?"}
    D -->|Yes, registered| E["Order details returned"]
    D -->|No| F["IVR asks for registered mobile number"]
    F --> G["Customer enters number on keypad"]
    G --> H["Exotel sends number to Dot and Key API again"]
    H --> E
    E --> I{"More than one order?"}
    I -->|Yes| J["IVR lists products, customer selects one"]
    I -->|No| K["Play status IVR"]
    J --> K
```

## Sequence: registered number
```mermaid
sequenceDiagram
    participant Customer
    participant Exotel as Exotel IVR
    participant API as Dot and Key API / Database
    Customer->>Exotel: Calls single number
    Exotel->>API: Send caller number
    API-->>Exotel: 200 OK with order details
    Exotel->>Customer: Plays order-status IVR
```

## Sequence: different number
```mermaid
sequenceDiagram
    participant Customer
    participant Exotel as Exotel IVR
    participant API as Dot and Key API / Database
    Customer->>Exotel: Calls single number
    Exotel->>API: Send caller number
    API-->>Exotel: Not 200 OK
    Exotel->>Customer: Asks for registered mobile number
    Customer->>Exotel: Enters number on keypad
    Exotel->>API: Send entered number
    API-->>Exotel: Order details
    Exotel->>Customer: Plays order-status IVR
```

## Components
| Component | Owner | Role |
|---|---|---|
| Website | Client | Promotes the single number |
| Exotel number and IVR | Exotel | Receives calls, runs the call flow, plays messages |
| Order database / API | Client | Looks up orders by mobile number, returns status |
| Order-confirmation call | Exotel + Client | Outbound call after the order is booked |

## Design notes
- **Number as the key:** the mobile number identifies the customer and their orders
- **HTTP status drives the flow:** 200 OK continues, otherwise the keypad fallback starts
- **Always live data:** status comes from the client's system at the time of the call

## Diagram files
_Add the original draw.io / PNG architecture diagram here if one exists._
