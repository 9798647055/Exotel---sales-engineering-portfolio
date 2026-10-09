# Call Campaign, SIP Trunk and API Flow

## Recharge reminder campaign
| Step | What happens |
|---|---|
| 1 | Client identifies customers whose recharge or plan is about to expire |
| 2 | Reminder date is reached (for example 5th for validity ending on the 10th) |
| 3 | Exotel places an outbound call to the customer |
| 4 | If answered, the call is connected to Haptik's bot over the SIP trunk |
| 5 | Bot reminds the customer and handles questions, including offers and discounts |
| 6 | If not answered, the call is retried, up to three attempts in total |
| 7 | The cycle repeats every month |

## Attempt rules
| Rule | Detail |
|---|---|
| First call | Ahead of expiry, for example 5 days before |
| Maximum attempts | 3 in total per customer |
| Applies to | Mobile SIM and Jio Fiber customers |
| Gap between attempts | _To be added from project records_ |

## Voice path
| Leg | Detail |
|---|---|
| Customer phone to Exotel | Normal phone call |
| Exotel to Haptik bot | **SIP trunk**, voice carried as packets in both directions |
| Haptik bot to customer | Same path in reverse |

Because the voice goes both ways, the customer can speak to the bot and the bot can respond.

## Chat-to-callback API flow
| Step | What happens |
|---|---|
| 1 | Customer asks for a callback in the MyJio chat |
| 2 | The chatbot sends a request to the **Exotel outbound call API** |
| 3 | The request carries the **customer's phone number** |
| 4 | The request also carries a **reference** capturing why the call is needed, from the chat discussion |
| 5 | Exotel dials the customer |

## Data exchanged
| Field | Direction | Description |
|---|---|---|
| Customer number | Chatbot to Exotel | Number to be called |
| Reference | Chatbot to Exotel | Context of the chat, so the reason for the call is known |
| Call status | Exotel to client (if used) | Answered / not answered |

## Open items
- Time gap between the three attempts
- What the bot does after the call connects in the callback flow (assumed same bot as the reminder flow, to confirm)
- Expected peak concurrent calls
- Outbound-call regulatory rules, such as allowed calling hours and consent
- Languages for the bot
