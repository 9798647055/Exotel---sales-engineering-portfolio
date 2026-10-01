# Requirements: Swiss Beauty

## Business context
Swiss Beauty is a D2C cosmetics brand in India selling to customers online. After an order is placed, customers want to know when it will arrive, and sometimes need to change something about it.

## Client pain points
- Customers want to know whether the order is shipped or dispatched, and the delivery date
- Customers who are not satisfied with the automated answer have no direct way to reach the backend team
- The support team did not want to take customer calls on mobile phones

## Client needs
| # | Need | Priority |
|---|---|---|
| 1 | Tell customers over a call that the order is **shipped or dispatched** | High |
| 2 | Tell customers the **expected delivery date** | High |
| 3 | **One single number** promoted on the website | High |
| 4 | Let customers **talk to the backend / support team** if not satisfied with the IVR | High |
| 5 | Support team takes these calls **on a laptop, not a mobile phone** | High |
| 6 | Support team can handle **changes** such as delivery address or product | High |

## Scenarios
| # | Scenario | Expected behaviour |
|---|---|---|
| 1 | Customer calls to check order | IVR plays that the order is shipped or dispatched, with the delivery date |
| 2 | Customer is satisfied | Call ends after the IVR message |
| 3 | Customer is not satisfied with the IVR response | Call is connected to the support team |
| 4 | Customer wants to change the delivery address or product | Call is connected to the support team, who take the request |
| 5 | Agent receives the call | Agent answers on a laptop through WebRTC |

## Example status messages
- Your order has been shipped
- Your order has been dispatched
- Your order will be delivered by [date]

## Success criteria
- Customers can get order status by calling one number
- Customers who need more help reach an agent easily
- Agents handle calls on laptops without mobile phones

## Information still to capture
- Number of support agents and expected call volume
- Support working hours
- Languages needed
- How order data is made available to the IVR
