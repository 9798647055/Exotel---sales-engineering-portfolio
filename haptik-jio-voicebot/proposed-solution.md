# Proposed Solution

## Positioning
Exotel provides the **cloud telephony infrastructure** that lets Haptik's existing chatbot hold **two-way voice conversations** with Jio customers at very large scale.

## What was proposed
1. A **SIP trunk** between Haptik's bot platform and Exotel, carrying the call's voice both ways.
2. An **outbound campaign** of recharge-reminder calls, with up to three attempts per customer.
3. A **chat-to-callback flow** where the MyJio chatbot triggers the Exotel outbound call API.

## Why SIP trunk and not a streaming channel
| Factor | Streaming channel | SIP trunk (proposed) |
|---|---|---|
| Cost at very large scale | Higher | Lower |
| Voice latency | Adds delay to the conversation | Lower delay |
| Fit for an existing bot | Needs the bot to work over a stream | Haptik's bot connects as telephony |

Cost and latency were the two key reasons I did not pitch the streaming channel.

## How the recharge reminder works
1. Before a customer's validity ends, an outbound call is placed (for example on the 5th if validity ends on the 10th).
2. The call goes from Exotel to the customer's phone.
3. The voice is carried over the **SIP trunk** to Haptik's bot as packets, and back the same way. This makes the conversation **two-way**.
4. The bot tells the customer the recharge is expiring, and can answer questions, including about **offers and discounts**.
5. If the customer does not answer, the call is retried, up to **three attempts in total**.
6. This repeats **every month**, for both SIM and Jio Fiber customers.

## How chat-to-callback works (Jio Fiber)
1. The customer chats with the bot in MyJio.
2. The customer asks for a **callback**.
3. The chatbot calls the **Exotel outbound call API** and passes the customer's phone number in the request.
4. Exotel dials the customer.
5. The **reason for the call** is captured through a reference from the chat discussion.

## What the client provides
- The bot platform (chatbot and voicebot logic)
- Recharge expiry data and the list of customers to call
- Offer and discount content for the bot
- API integration from the chatbot to Exotel

## My contribution
- Understood the scale and the cost and latency constraints
- Compared a streaming channel with a SIP trunk and recommended the SIP trunk
- Designed the outbound reminder flow with retries
- Designed the chat-to-callback flow using the outbound call API
- Coordinated with the Haptik technical team on integration
