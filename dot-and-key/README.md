# Dot & Key: Order Status IVR (Single Number Self-Service)

| | |
|---|---|
| **Client** | Dot & Key |
| **Industry** | Beauty & Cosmetics / D2C E-commerce (India) |
| **Solution** | Exotel IVR + API integration with the client's order database |
| **Channel** | Voice: IVR (inbound) and order-confirmation call |
| **Status** | Implemented |
| **My role** | Sales Engineer: discovery, solution design, integration proposal, coordination |
| **Year** | _To be added_ |

## One-line pitch
One number, promoted on the website, that lets any Dot & Key customer **hear their order status by phone**: the IVR recognizes the caller, fetches the order from the client's system and plays the right update.

## The problem
Dot & Key wanted customers to know how soon their product would reach the doorstep: whether the order is received, packed, shipped or out for delivery. This had to be **over a call, not through the app or website**.

## The solution
- One Exotel number is published on the Dot & Key website
- The caller's number is checked against the client's database through an API
- **Registered number (HTTP 200 OK):** the IVR plays the order status directly
- **Unregistered number (no 200 OK):** the IVR asks for the registered mobile number on the keypad, checks again and plays the status
- **Multiple orders:** the IVR lists the products and the caller selects one with a keypad press

```
Customer calls Exotel number -> Caller number sent to Dot & Key API
   -> 200 OK: play order-status IVR
   -> Not 200 OK: ask for registered mobile number -> check again -> play order-status IVR
```

## Business value (expected, to be confirmed with results)
- Customers get delivery updates by voice, with no app or website needed
- One easy-to-remember number to promote
- Automated status handling without agents for routine "where is my order" calls
- Better post-purchase experience

## Documents in this folder
| File | What it covers |
|---|---|
| [requirements.md](requirements.md) | Client's problem, needs and scenarios |
| [proposed-solution.md](proposed-solution.md) | What was proposed and why |
| [architecture/solution-architecture.md](architecture/solution-architecture.md) | Architecture and flow diagrams |
| [integration/ivr-flow-and-api-logic.md](integration/ivr-flow-and-api-logic.md) | IVR flow, API logic and status messages |
| [implementation-plan.md](implementation-plan.md) | Approach and responsibilities |
| [sales-playbook.md](sales-playbook.md) | Pitch, discovery questions, objection handling |
| [outcome.md](outcome.md) | Business value, results and lessons learned |

> Items marked _To be added_ are not yet captured and should be filled in from the deal records.
