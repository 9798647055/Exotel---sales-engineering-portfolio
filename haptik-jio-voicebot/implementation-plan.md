# Implementation Approach

## Phases
| Phase | Activity | Owner |
|---|---|---|
| 1. Discovery | Understand the recharge reminder need, scale, and Haptik's existing bot | Sales Engineer + Client |
| 2. Architecture decision | Compare streaming channel and SIP trunk on cost and latency, recommend SIP trunk | Sales Engineer |
| 3. Call flow design | Define timing of the first call, retries and monthly cycle | Sales Engineer + Client |
| 4. SIP trunk setup | Connect Haptik's bot platform to the Exotel SIP trunk | Haptik tech team + Exotel tech team |
| 5. API integration | Connect the chatbot to the Exotel outbound call API for callbacks | Haptik tech team + Exotel tech team |
| 6. Testing | Test reminder calls, retries, two-way conversation and callbacks | Client + Exotel |
| 7. Go-live | Start campaigns for SIM and Jio Fiber customers | Client |

## Responsibilities
**Haptik / Jio:** bot, expiry data, customer list, offer content, chatbot integration.
**Exotel:** SIP trunk, outbound calling, outbound call API.
**Sales Engineer (me):** requirements, architecture recommendation, call flow design, coordination between teams.

## Timeline and milestones
_To be added from project records._
