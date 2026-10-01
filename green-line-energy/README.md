# Green Line Energy: Telematics & Driver Safety Automation

| | |
|---|---|
| **Client** | Green Line Energy |
| **Industry** | Travel / Transportation (bus fleet operations) |
| **Solution** | Exotel Cloud Telephony API + Telematics integration |
| **Channel** | Automated outbound voice calls |
| **Status** | Implemented |
| **My role** | Sales Engineer: discovery, solution design, integration proposal, coordination |
| **Year** | _To be added_ |

## One-line pitch
Turn the client's vehicle telematics signals into **real-time automated voice calls to the driver**, so critical safety events are acted on in seconds instead of waiting for manual monitoring.

## The problem
Green Line Energy needed real-time visibility into bus status, speed, operating conditions and driver behaviour. They also needed to catch critical events (overspeeding, engine overheating, prolonged driving, driver fatigue) and reach the driver **immediately**.

## The solution
The client's telematics platform generates predefined signals. Each signal is sent to the Exotel Cloud Telephony API, which identifies the bus and driver and places an automated outbound call with the right safety message.

```
Telematics Software -> Event/Signal -> Exotel Cloud Telephony API -> Signal Processing
        -> Driver Identification -> Automated Outbound Call -> Real-Time Driver Alert
```

## Business value
- Telematics data becomes **real-time, voice-based safety alerts**
- **Less dependency on manual monitoring**
- **Faster communication** with drivers during critical conditions
- Safer driving behaviour and better fleet-safety control

## Documents in this folder
| File | What it covers |
|---|---|
| [requirements.md](requirements.md) | Client's problem, needs and success criteria |
| [proposed-solution.md](proposed-solution.md) | What was proposed and why |
| [architecture/solution-architecture.md](architecture/solution-architecture.md) | Architecture and flow diagrams |
| [integration/event-to-call-mapping.md](integration/event-to-call-mapping.md) | Telematics signal to voice-alert mapping |
| [implementation-plan.md](implementation-plan.md) | Approach and responsibilities |
| [sales-playbook.md](sales-playbook.md) | Pitch, discovery questions, objection handling |
| [outcome.md](outcome.md) | Business value, results and lessons learned |

> Items marked _To be added_ are not yet captured and should be filled in from the deal records.
