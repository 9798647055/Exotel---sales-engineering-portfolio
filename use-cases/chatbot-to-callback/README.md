# Use Case: Chatbot to Callback (API-Triggered Outbound Call)

## Pattern
A customer chatting with a bot asks for a call. The chatbot calls the cloud telephony **outbound call API** with the customer's number and a reference to the chat, and the platform dials the customer.

```
Customer chat -> Chatbot -> Outbound call API (number + reference) -> Call to customer
```

## Where it fits
| Industry | Use |
|---|---|
| Telecom | Plan, recharge and fiber support callbacks |
| BFSI | Loan or card enquiry callbacks |
| E-commerce | Order issue callbacks |
| Healthcare | Appointment callbacks |

## Projects using this pattern
| Project | Industry |
|---|---|
| [Haptik (for Jio): Recharge Reminder Voicebot](../../haptik-jio-voicebot/README.md) | Telecom / Conversational AI |
