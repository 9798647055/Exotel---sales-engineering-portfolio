# Implementation Approach

## Phases
| Phase | Activity | Owner |
|---|---|---|
| 1. Discovery | Understand the customer experience, order statuses and current support flow | Sales Engineer + Client |
| 2. Solution design | Design the IVR flow, 200 OK logic, keypad fallback and multi-order menu | Sales Engineer |
| 3. API definition | Agree the lookup request and response (mobile number in, order details out) | Client tech team + Exotel tech team |
| 4. Message mapping | Map each order status to an IVR message | Client + Sales Engineer |
| 5. Integration | Connect the Exotel number and IVR to the client's database / API | Client tech team + Exotel tech team |
| 6. Testing | Test registered number, different number, multiple orders and confirmation call | Client + Exotel |
| 7. Go-live | Publish the single number on the website | Client |

## Responsibilities
**Client:** order database and API access, order-status data, publishing the number on the website.
**Exotel:** number, IVR, call handling, API calls, outbound confirmation call.
**Sales Engineer (me):** requirements, solution design, integration proposal, coordination between teams.

## Timeline and milestones
_To be added from project records._
