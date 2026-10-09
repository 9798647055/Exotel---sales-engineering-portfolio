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
| Telecom | Recharge or plan expiry reminder | Customer |
| Utilities | Outage or payment due | Customer |
| Logistics | Delivery exception | Customer or driver |

## Projects using this pattern
| Project | Industry |
|---|---|
| [Green Line Energy: Telematics & Driver Safety](../../green-line-energy/README.md) | Travel / Transportation |
| [Haptik (for Jio): Recharge Reminder Voicebot](../../haptik-jio-voicebot/README.md) | Telecom / Conversational AI |
