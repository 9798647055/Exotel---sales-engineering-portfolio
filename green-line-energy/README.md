# Green Line Energy: Telematics & Driver Safety Automation

| | |
|---|---|
| **Client** | Green Line Energy |
| **Industry** | Travel / Transportation (bus fleet) |
| **Solution** | Exotel Cloud Telephony API integrated with the client's telematics platform |
| **Channel** | Automated outbound voice calls |
| **My role** | Sales Engineer: solution design, integration proposal and coordination |

## Problem
Green Line Energy needed real-time visibility into the status, speed and operating conditions of its buses, and into driver behaviour. They also needed to catch critical events such as overspeeding, engine overheating, prolonged driving and driver fatigue, and tell the driver **immediately**.

## Solution
I proposed and implemented a solution that connects the client's **telematics software** to **Exotel Cloud Telephony APIs**. The telematics platform monitors each bus and generates a signal when a safety condition is met. That signal is sent to Exotel, which identifies the driver mapped to the bus and places an **automated outbound call** with the right alert.

Example alert: *"Your bus is currently overspeeding. Please reduce the speed and drive safely."*

## Workflow
```mermaid
flowchart LR
    A["Telematics software"] --> B["Event / signal generated"]
    B --> C["Exotel Cloud Telephony API"]
    C --> D["Signal processing"]
    D --> E["Driver identification"]
    E --> F["Automated outbound call"]
    F --> G["Real-time driver alert"]
```

## Signals handled
| Telematics signal | Driver alert |
|---|---|
| Overspeeding | Reduce speed and drive safely |
| Engine overheating | Engine temperature exceeded the defined limit |
| Extended driving hours | Take a break |
| Driver fatigue / break required | Rest before continuing |
| Other predefined safety conditions | As defined with the client |

## My contribution
- Understood the client's operational and safety challenges and turned them into a technical solution
- Designed the cloud telephony and API-based communication workflow
- Proposed integrating the client's telematics platform with Exotel's Cloud Telephony API
- Worked with the client and technical teams to define event triggers and communication workflows
- Mapped telematics signals to automated voice-call alerts
- Coordinated the technical implementation and integration requirements

## Business value
The solution turned vehicle telematics data into **real-time voice safety alerts**. It reduced dependency on manual monitoring and enabled faster communication with drivers when critical vehicle or driving conditions were detected.
