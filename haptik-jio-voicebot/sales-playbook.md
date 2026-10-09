# Sales Playbook: Voicebot on SIP Trunk at Scale

Reusable notes for telecom, BFSI and other businesses running large outbound campaigns with a conversational bot.

## Elevator pitch
"You already have the bot. We give it the phone line. A SIP trunk connects your bot to the telephone network, so it can call millions of customers and hold a natural two-way conversation, at lower cost and less delay than a streaming channel."

## Ideal customer
- Telecom, BFSI, insurance and utilities with very large customer bases
- Businesses with recurring reminders (renewals, dues, expiries)
- Companies that already have a chatbot or voicebot and need telephony

## Discovery questions
1. How many customers need a call each month, and what is the peak?
2. How far ahead of the due date should the call go?
3. How many attempts, and how far apart?
4. Do you already have a chatbot or voicebot platform?
5. Does your bot platform support SIP?
6. How sensitive is the conversation to voice delay?
7. What should the bot talk about beyond the reminder (offers, payments, support)?
8. Do customers need to be able to request a callback from chat or an app?
9. Which regulatory rules apply to your outbound calls?
10. Which languages are needed?

## Value proposition
| Client pain | Our answer |
|---|---|
| Huge base, manual calling cannot cover it | Automated outbound campaigns |
| Bot conversation feels slow | SIP trunk keeps latency low |
| Streaming cost grows with volume | SIP trunk is more cost-effective at scale |
| Customers want to ask questions | Two-way conversation with the bot |
| Customers chat, then want a call | Chatbot triggers the outbound call API |

## Likely objections
| Objection | Response |
|---|---|
| "Can the bot really have a two-way conversation?" | Yes. Voice flows in both directions over the SIP trunk, so the customer can speak and the bot can answer. |
| "Why not use a streaming channel?" | At very large scale, it costs more and adds voice latency. A SIP trunk avoids both. |
| "Can we reuse our existing bot?" | Yes. We provide the telephony layer, and your bot stays as it is. |
| "What if the customer does not answer?" | Retries are built into the campaign, up to the number of attempts you define. |

## Cross-sell ideas
- Payment reminders and collections
- Renewal and upsell campaigns
- Callback services from chat, app and website
- Call recording and analytics
- WhatsApp or SMS follow-ups
