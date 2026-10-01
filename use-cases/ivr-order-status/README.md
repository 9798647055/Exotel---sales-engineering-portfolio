# Use Case: IVR Order Status (Caller Recognition + API Lookup)

## Pattern
A customer calls one number. The cloud telephony platform checks the caller's number against the business's system through an API. If the number is known, the IVR plays the status. If not, it asks for the registered number on the keypad and checks again.

```
Inbound call -> Caller number -> Business API lookup -> 200 OK: play status
                                        -> Not found: keypad entry -> lookup -> play status
```

## Where it fits
| Industry | Information played | Caller |
|---|---|---|
| E-commerce / D2C | Order and delivery status | Customer |
| Logistics | Shipment tracking | Sender or receiver |
| Banking | Loan or card application status | Customer |
| Healthcare | Appointment or report status | Patient |
| Utilities | Complaint or service request status | Customer |

## Projects using this pattern
| Project | Industry |
|---|---|
| [Dot & Key: Order Status IVR](../../dot-and-key/README.md) | Beauty & Cosmetics / D2C |
| [Swiss Beauty: Order Status IVR + WebRTC Agent Calling](../../swiss-beauty/README.md) | Beauty & Cosmetics / D2C |
