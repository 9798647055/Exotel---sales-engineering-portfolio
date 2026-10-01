# Sales Playbook: Order-Status IVR for E-commerce / D2C

Reusable notes for similar opportunities in e-commerce, retail and D2C brands.

## Elevator pitch
"Your customers keep asking where their order is. We give you one number on your website. When they call, we recognize them, check your system and tell them the status of their order, with no app, no website and no waiting for an agent."

## Ideal customer
- D2C brands and online retailers with high order volumes
- Customers who prefer calling over using an app
- Teams spending agent time on "where is my order" calls

## Discovery questions
1. How do customers check their order status today?
2. What share of support calls is about order status?
3. Do customers call from the registered number or from others?
4. How many statuses exist in your order lifecycle?
5. Can your system look up orders by mobile number through an API?
6. How long does that lookup take?
7. Do customers often have more than one open order?
8. Which languages do your customers speak?
9. Do you want an outbound call after order placement?

## Value proposition
| Client pain | Our answer |
|---|---|
| Customers want status without using an app or website | A voice IVR on one number |
| Too many routine status calls reach agents | Automated self-service |
| Customers call from different numbers | Keypad fallback for the registered number |
| Customers with several orders get confused | Product-wise selection menu |
| Status goes stale | Live lookup from your system on every call |

## Likely objections
| Objection | Response |
|---|---|
| "Our database cannot be opened to a third party." | Only a controlled lookup API is needed (mobile number in, order status out). The client decides what is shared. |
| "What if the API is slow?" | Define response-time targets in the design phase and add a clear waiting prompt. |
| "Customers might not trust a phone call." | Use a consistent number and wording, and promote it on the website. |
| "Can we add more languages or statuses?" | Yes, by adding messages and mapping new statuses. |

## Cross-sell ideas
- WhatsApp or SMS order updates
- Delivery-failure (NDR) calls
- Cash-on-delivery confirmation calls
- Post-delivery feedback calls
- Agent handover from the IVR (contact center)
