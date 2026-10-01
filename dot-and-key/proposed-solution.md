# Proposed Solution

## Positioning
Cloud telephony as an **automated, voice-based order-status channel** that connects the customer's call to the client's order data in real time.

## What was proposed
An **Exotel IVR** on a single Exotel number, integrated with Dot & Key's systems through an API. Because the number is an Exotel asset, every inbound call is handled by Exotel, which captures the caller's number and checks it against Dot & Key's database.

## How it works
1. Dot & Key promotes **one Exotel number** on its website.
2. The customer calls the number.
3. Exotel captures the caller's number and **pushes it to the Dot & Key database** (via API).
4. If the number is registered, Dot & Key returns **HTTP 200 OK** with the order details.
5. On 200 OK, Exotel plays the **IVR matching the order status**.
6. If Dot & Key does not return 200 OK, Exotel plays a **different IVR asking for the registered mobile number**.
7. The customer enters the number on the keypad. Exotel pushes it to Dot & Key again.
8. Dot & Key shares the order information and Exotel **plays it over the IVR**.
9. If the customer has **multiple orders**, the IVR lists the products and the customer selects one using the keypad. The matching status is then played.

## Order confirmation call
When an order is booked, the customer receives a call confirming the order for the named product and inviting them to call the single number to check the delivery status.

## What the client provides
- API / database access so Exotel can look up orders by mobile number
- Order status and product data returned in the response
- The single number to be published on their website

## Why this approach
| Reason | Benefit to client |
|---|---|
| Single number | Simple to promote and easy for customers to remember |
| Caller recognition | Registered customers get status without typing anything |
| Fallback to keypad entry | Customers calling from another phone still get served |
| Multi-order menu | Handles real customer behaviour |
| API-based | Live status, always matching the client's system |
| Cloud-based | No telephony hardware, scales with order volume |

## My contribution
- Understood the client's customer-communication challenge and turned it into an IVR and API workflow
- Designed the call flow, including the 200 OK check, keypad fallback and multi-order selection
- Proposed the Exotel API integration with the client's database
- Coordinated requirements between the client's technical team and Exotel's team
