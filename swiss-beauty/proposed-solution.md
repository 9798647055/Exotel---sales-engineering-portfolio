# Proposed Solution

## Positioning
Cloud telephony as a **voice-based order-status channel with a human fallback**: an automated IVR for routine queries, and a browser-based calling experience (WebRTC) for the support team when a customer needs help.

## What was proposed
1. An **Exotel IVR on a single number**, promoted on Swiss Beauty's website, that plays the customer's order status and delivery date.
2. A **WebRTC (VoIP) solution** so the backend / support team can take customer calls **on their laptops** instead of mobile phones.

## How it works
1. Swiss Beauty publishes **one Exotel number** on its website.
2. The customer calls the number.
3. The IVR plays the order status: the order is **shipped or dispatched**, and it will be delivered by a given date.
4. If the customer is **satisfied**, the call ends.
5. If the customer is **not satisfied**, or wants a **change** (for example delivery address or product), the call is **connected to the Swiss Beauty support team**.
6. The agent receives the call **in the browser on a laptop** through WebRTC and talks to the customer over the internet.
7. The agent takes the customer's request and handles the change.

## What WebRTC means for the client
WebRTC lets a browser make and receive calls directly over the internet. It is the same idea as VoIP (voice over internet protocol). The agent needs a laptop, a headset and an internet connection, and does not need a mobile phone or a desk phone.

## What the client provides
- The order information needed for the IVR to play status and delivery date
- Support team members and their laptops
- The single number's placement on the website

## Why this approach
| Reason | Benefit to client |
|---|---|
| Single number | Simple to promote and remember |
| Automated status IVR | Routine "where is my order" calls need no agent |
| Human fallback | Customers who are unhappy or need changes reach a person |
| WebRTC on laptops | No mobile phones for agents, and calls are handled where agents already work |
| Cloud-based | No telephony hardware, scales with the team |

## My contribution
- Understood the client's order-communication challenge and the support team's working preference
- Designed the call flow: IVR first, then handover to an agent when needed
- Proposed the WebRTC solution for browser-based agent calling
- Coordinated requirements between the client and Exotel's teams
