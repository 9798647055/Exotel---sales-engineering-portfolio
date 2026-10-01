# IVR Flow and Agent Handover

## Call flow
| Step | What happens | Next step |
|---|---|---|
| 1 | Customer calls the single Exotel number | Step 2 |
| 2 | IVR plays the order status and expected delivery date | Step 3 |
| 3 | Customer is satisfied | Call ends |
| 3 | Customer is not satisfied or wants a change | Step 4 |
| 4 | Call is routed to the support team | Step 5 |
| 5 | Agent answers on the laptop through WebRTC | Step 6 |
| 6 | Agent talks to the customer and takes the request (address, product) | Call ends |

## IVR messages
| Situation | Message intent |
|---|---|
| Order shipped | Your order has been shipped |
| Order dispatched | Your order has been dispatched |
| Delivery date | Your order will be delivered by [date] |
| Need more help | Option to talk to the support team |

The option to reach the support team is offered after the status message. The exact keypad option and wording are _to be confirmed from project records_.

## Agent experience (WebRTC)
| Item | Detail |
|---|---|
| Device | Laptop with a browser and a headset |
| Connection | Internet (VoIP), no mobile or desk phone needed |
| Calls received | Customers who asked for the support team from the IVR |
| What agents handle | Order concerns and change requests such as delivery address or product |

## Changes the support team can take
- Delivery address change
- Product change
- Other order concerns raised by the customer

How each change is applied in the client's order system is handled by the client's team.

## Open items
- How the IVR gets order status and delivery date from the client's system
- How calls are routed when several agents are available
- What happens when no agent is free or outside working hours
- Call recording and quality monitoring needs
- Languages for IVR messages
