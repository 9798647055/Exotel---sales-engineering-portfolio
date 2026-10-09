# Haptik (for Jio): Recharge Reminder Voicebot over SIP Trunk

| | |
|---|---|
| **Client** | Haptik (Reliance group), serving **Jio / MyJio** |
| **End customer** | Jio: mobile SIM and Jio Fiber users |
| **Industry** | Telecom / Conversational AI |
| **Solution** | Two-way voicebot on an Exotel SIP trunk + chatbot-triggered outbound call API |
| **Channel** | Voice: outbound calls over SIP trunk, API-triggered callbacks |
| **Status** | Implemented |
| **My role** | Sales Engineer: discovery, architecture recommendation, solution design and coordination |
| **Year** | _To be added_ |

## One-line pitch
A **two-way voicebot** that calls a very large telecom customer base before their recharge expires, built on an Exotel **SIP trunk** instead of a streaming channel to keep cost and voice latency low, plus a **chat-to-callback** flow where the chatbot triggers an outbound call through the Exotel API.

## The problem
Jio wanted to automate calls to customers whose **mobile recharge or Jio Fiber plan was about to expire**, month after month, across a huge customer base. Haptik, which already had its own chatbot and voicebot, needed the **telephony layer** to carry those calls at scale without high cost or voice delay.

## The solution
- **Outbound recharge-reminder calls** placed ahead of expiry. For example, if validity ends on the 10th, the first call goes out on the 5th, with up to **three attempts in total** per customer.
- The same flow serves **SIM and Jio Fiber** customers.
- **SIP trunk instead of a streaming channel:** I recommended a SIP trunk because a streaming channel adds cost at this scale and increases voice latency.
- **Two-way conversation:** the customer can talk to the bot, ask about offers or discounts, and the bot tells them what is available.
- **Chat-to-callback (Jio Fiber):** a customer chatting with the bot in MyJio can ask for a callback. The chatbot calls the **Exotel outbound call API** with the customer's number, and Exotel dials the customer. The reason for the call is carried through a reference from the chat.

## Business value (expected, to be confirmed with results)
- Recharge reminders automated across a huge customer base
- Fewer lapsed recharges through timely, repeated reminders
- Natural two-way conversation, including offer and discount queries
- Lower cost and lower latency than a streaming-channel approach
- Seamless move from chat to a live voice call

## Documents in this folder
| File | What it covers |
|---|---|
| [requirements.md](requirements.md) | Client's problem, needs and scenarios |
| [proposed-solution.md](proposed-solution.md) | What was proposed and why SIP trunk |
| [architecture/solution-architecture.md](architecture/solution-architecture.md) | Architecture and flow diagrams |
| [integration/sip-trunk-and-api-flow.md](integration/sip-trunk-and-api-flow.md) | Call campaign logic, SIP trunk and callback API flow |
| [implementation-plan.md](implementation-plan.md) | Approach and responsibilities |
| [sales-playbook.md](sales-playbook.md) | Pitch, discovery questions, objection handling |
| [outcome.md](outcome.md) | Business value, results and lessons learned |

> Items marked _To be added_ are not yet captured and should be filled in from the deal records.
