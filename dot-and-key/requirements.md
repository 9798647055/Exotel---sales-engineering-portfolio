# Requirements: Dot & Key

## Business context
Dot & Key is a well-known cosmetics brand in India selling to customers online. After a customer places an order, they want to know when it will arrive.

## Client pain points
- Customers want to know how soon the product will reach their doorstep
- Customers want to know whether the order is packed, shipped or out for delivery
- Order updates were expected through the app or website, but the client wanted a **call-based** option

## Client needs
| # | Need | Priority |
|---|---|---|
| 1 | Inform the customer of order status over a **voice call**, not the app or website | High |
| 2 | Call the customer after order booking to confirm the order and tell them they can call back for status | High |
| 3 | **One single number** promoted on the website for all status queries | High |
| 4 | Recognize customers calling from their **registered mobile number** automatically | High |
| 5 | If calling from a different number, collect the **registered mobile number** via keypad | High |
| 6 | Play the right IVR message based on the order status and item | High |
| 7 | Handle customers with **multiple orders** by letting them choose which one | High |

## Scenarios
| # | Scenario | Expected behaviour |
|---|---|---|
| 1 | Order booked | Customer receives a call: order received for the named product, and they can call the number for status |
| 2 | Customer calls from registered number | Number is recognized, order is fetched, status is played |
| 3 | Customer calls from a different number | IVR asks for the registered mobile number, then plays the status |
| 4 | Customer has multiple orders | IVR lists the products, customer selects one, status for that order is played |

## Example status messages
- Your order is received and saved
- Your order is out for delivery
- Your order will be dispatched within 2 days

## Success criteria
- Customers can get their order status by calling one number
- The right status is played for the right order
- No dependency on the app or website for status

## Information still to capture
- Daily call volume and number of orders
- Languages needed
- Whether an agent fallback is required
