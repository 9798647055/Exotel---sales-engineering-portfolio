# Requirements: Haptik (for Jio)

## Business context
Haptik is a conversational AI company in the Reliance group and already had its own chatbot and voicebot. It worked with Jio, one of India's largest telecom providers and also part of Reliance. Haptik received the service from Exotel and onboarded Jio onto the same application.

## Client pain points
- A very large customer base whose recharges expire every month
- Customers forget to recharge their mobile or Jio Fiber plan
- Manual calling cannot cover this volume
- Haptik needed a telephony layer for its existing bot, at acceptable cost and voice quality

## Client needs
| # | Need | Priority |
|---|---|---|
| 1 | Automated **outbound call** telling the customer their recharge is **about to expire** or has expired | High |
| 2 | Call **before** the validity ends, every month | High |
| 3 | **Three attempts in total** to the same customer | High |
| 4 | Same flow for **mobile SIM** and **Jio Fiber** customers | High |
| 5 | **Two-way** conversation: customer can talk to the bot | High |
| 6 | Bot can tell the customer about **offers and discounts** when asked | Medium |
| 7 | Work with Haptik's **existing chatbot** | High |
| 8 | **Low cost and low latency** at very large scale | High |
| 9 | Customer can **ask for a callback** from the MyJio chatbot | High |

## Scenarios
| # | Scenario | Expected behaviour |
|---|---|---|
| 1 | Recharge about to expire | Bot calls ahead of expiry (for example the 5th if validity ends on the 10th) |
| 2 | Customer does not answer | Bot retries, up to three attempts in total |
| 3 | Customer asks about offers | Bot explains the discounts available |
| 4 | Customer is a Jio Fiber user | Same reminder flow as for SIM users |
| 5 | Customer asks for a callback in the chat | Chatbot triggers the Exotel outbound call API, and the customer receives a call |

## Success criteria
- Reminder calls reach customers on time, every month
- Conversations are natural, with minimal delay
- Cost stays workable at this scale

## Information still to capture
- Call volume per month and peak concurrency
- Time gap between attempts
- Languages supported
- Regulatory rules applied to outbound calls
