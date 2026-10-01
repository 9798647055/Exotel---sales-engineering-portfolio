# Swiss Beauty: Order Status IVR + WebRTC Agent Calling

| | |
|---|---|
| **Client** | Swiss Beauty |
| **Industry** | Beauty & Cosmetics / D2C e-commerce (India) |
| **Solution** | Exotel IVR on a single number + WebRTC (VoIP) calling for the support team |
| **Channel** | Voice: inbound IVR and browser-based agent calls |
| **Status** | Implemented |
| **My role** | Sales Engineer: discovery, solution design and coordination |
| **Year** | _To be added_ |

## One-line pitch
One number on the website tells customers their **order status by voice**, and if they need more help, the call goes to a Swiss Beauty support agent who answers **on a laptop through WebRTC**, not on a mobile phone.

## The problem
Swiss Beauty wanted customers to know their order was **shipped or dispatched**, and **by what date it would be delivered**. Customers who were not satisfied with the IVR answer, or who wanted a change such as a **new delivery address** or a **change in product**, needed a way to talk to the backend support team. The team did not want to take these calls on mobile phones.

## The solution
- **Single number** promoted on the website for all order queries
- **Exotel IVR** plays the order status: shipped or dispatched, and the expected delivery date
- **Talk to the team:** if the customer is not satisfied or wants changes, the call is connected to the Swiss Beauty support team
- **WebRTC calling:** agents receive and handle those calls **in the browser on their laptops** over the internet (VoIP), with no mobile phone needed

```
Customer calls single number -> Exotel IVR plays order status
   -> Satisfied: call ends
   -> Not satisfied / wants a change: call routed to support agent's laptop (WebRTC) -> agent helps
```

## Business value (expected, to be confirmed with results)
- Customers get delivery updates by voice, with no app or website needed
- Customers who need more help can reach a real person
- Support agents work from laptops and need no mobile phones
- Address and product-change requests are handled by the support team in one call

## Documents in this folder
| File | What it covers |
|---|---|
| [requirements.md](requirements.md) | Client's problem, needs and scenarios |
| [proposed-solution.md](proposed-solution.md) | What was proposed and why |
| [architecture/solution-architecture.md](architecture/solution-architecture.md) | Architecture and flow diagrams |
| [integration/ivr-and-agent-handover-flow.md](integration/ivr-and-agent-handover-flow.md) | IVR flow, handover to agents and messages |
| [implementation-plan.md](implementation-plan.md) | Approach and responsibilities |
| [sales-playbook.md](sales-playbook.md) | Pitch, discovery questions, objection handling |
| [outcome.md](outcome.md) | Business value, results and lessons learned |

> Items marked _To be added_ are not yet captured and should be filled in from the deal records.
