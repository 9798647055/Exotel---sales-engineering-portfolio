# Use Case: WebRTC Agent Calling (Browser-Based VoIP)

## Pattern
Support agents make and receive customer calls **in a web browser on a laptop** over the internet, using WebRTC (voice over internet protocol), instead of mobile phones or desk phones.

```
Customer call -> Cloud telephony platform -> Routed over the internet -> Agent's browser (laptop + headset)
```

## Where it fits
| Industry | Use | Who uses it |
|---|---|---|
| E-commerce / D2C | Support calls after the IVR | Support team |
| Banking and finance | Customer service and collections | Service agents |
| Healthcare | Appointment and patient queries | Front-desk team |
| Sales teams | Inbound leads and follow-ups | Sales agents |
| Remote teams | Work-from-home support | Any agent |

## Typical requirements
- Laptop with a supported browser
- Headset with a microphone
- Stable internet connection

## Projects using this pattern
| Project | Industry |
|---|---|
| [Swiss Beauty: Order Status IVR + WebRTC Agent Calling](../../swiss-beauty/README.md) | Beauty & Cosmetics / D2C |
