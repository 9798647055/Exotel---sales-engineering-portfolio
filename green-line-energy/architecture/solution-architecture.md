# Solution Architecture

## High-level flow
```mermaid
flowchart LR
    A[Bus sensors and GPS] --> B[Client Telematics Platform]
    B -->|Event / signal| C[Exotel Cloud Telephony API]
    C --> D[Signal processing]
    D --> E[Driver identification<br/>bus to driver mapping]
    E --> F[Automated outbound call]
    F --> G[Driver receives real-time alert]
```

## Sequence
```mermaid
sequenceDiagram
    participant Bus
    participant Telematics as Client Telematics Platform
    participant API as Exotel Cloud Telephony API
    participant Driver
    Bus->>Telematics: Speed, engine and driving data
    Telematics->>Telematics: Detect predefined condition
    Telematics->>API: Send event (bus ID, event type)
    API->>API: Process signal, find mapped driver
    API->>Driver: Outbound voice call
    Driver-->>API: Call answered / not answered
    Note over Driver: Hears alert message and takes action
```

## Components
| Component | Owner | Role |
|---|---|---|
| Vehicle sensors / GPS | Client | Capture speed, engine and driving data |
| Telematics platform | Client | Monitor the vehicle and generate signals |
| Exotel Cloud Telephony API | Exotel | Receive signals and place outbound calls |
| Bus-to-driver mapping | Client / Exotel | Identify who to call for each bus |
| Voice alert content | Client / Exotel | Message played to the driver per event type |

## Design notes
- **Event-driven:** no polling, an alert is raised only when a condition is met
- **Loosely coupled:** the telematics platform only needs to send an event to the API
- **Extensible:** new signals can be added by defining a new event and message

## Diagram files
_Add the original draw.io / PNG architecture diagram here if one exists._
