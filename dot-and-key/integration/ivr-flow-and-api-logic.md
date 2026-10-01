# IVR Flow and API Logic

## Inbound call logic
| Step | What happens | Next step |
|---|---|---|
| 1 | Customer calls the single Exotel number | Step 2 |
| 2 | Exotel captures the caller's number and sends it to the Dot & Key API | Step 3 |
| 3 | API replies | 200 OK: Step 6. Otherwise: Step 4 |
| 4 | IVR asks the customer to enter the registered mobile number on the keypad | Step 5 |
| 5 | Exotel sends the entered number to the Dot & Key API | Step 6 if order info returned |
| 6 | One order: play status. Multiple orders: Step 7 | Play status |
| 7 | IVR lists the products and asks the customer to select one | Play status for the selected order |

## Order status messages
| Order status | IVR message (intent) |
|---|---|
| Order received / saved | Your order has been received and saved |
| Dispatch pending | Your order will be dispatched within 2 days |
| Out for delivery | Your order is out for delivery |
| Packed / shipped | _Sample wording, to be confirmed with client_ |
| Other statuses | _To be added_ |

Only the received, dispatch and out-for-delivery wording is confirmed. The rest is to be filled in from project records.

## Multi-order menu
Example: "You have two orders. For [first product name], press 1. For [second product name], press 2."
The product names come from the API response. The status for the chosen order is then played.

## Data exchanged
| Field | Direction | Description |
|---|---|---|
| Customer mobile number | Exotel to Dot & Key | Caller's number or number entered on keypad |
| HTTP response code | Dot & Key to Exotel | 200 OK means registered, otherwise fallback |
| Order list | Dot & Key to Exotel | Product name(s) and status for the customer |
| Keypad inputs | Customer to Exotel | Mobile number digits and order selection |

## Order-confirmation call
| Trigger | Message intent |
|---|---|
| Order booked | "We have received your order for [product]. Call this number any time to check your delivery status." |

## Open items
- Retry rules if the customer enters an invalid or unknown number
- Maximum number of orders listed in the menu
- Expected API response time, so the caller does not wait in silence
- Agent fallback, if required
- Languages for IVR messages
- Calling-time rules and consent for the confirmation call
