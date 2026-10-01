# Use Case: Proactive Voice Alerts (Event-Triggered Outbound Calls)

## Pattern
A business system detects an event and sends it to the cloud telephony API. The API places an automated outbound call with a relevant message.

```
Business system -> Event -> Cloud Telephony API -> Identify recipient -> Outbound call -> Alert
```

## Where it fits
| Industry | Trigger | Recipient |
|---|---|---|
| Transport / fleet | Overspeeding, engine overheating, fatigue | Driver |
| Banking | Suspicious transaction | Customer |
| Healthcare | Appointment or medication reminder | Patient |
| Utilities | Outage or payment due | Customer |
| Logistics | Delivery exception | Customer or driver |

## Projects using this pattern
| Project | Industry |
|---|---|
| [Green Line Energy: Telematics & Driver Safety](../../projects/green-line-energy-telematics-driver-safety/README.md) | Travel / Transportation |
