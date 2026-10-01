# Requirements: Green Line Energy

## Business context
Green Line Energy operates a bus fleet in the travel / transportation sector. Safety and timely communication with drivers are critical to the operation.

## Client pain points
- Limited real-time visibility into bus status, speed and operating conditions
- Dependence on manual monitoring to spot unsafe situations
- Delay between a critical event and the driver being informed
- No automated way to reach the driver at the moment of a safety event

## Client needs
| # | Need | Priority |
|---|---|---|
| 1 | Real-time monitoring of bus status, speed and operating conditions | High |
| 2 | Detect critical events: overspeeding, engine overheating, prolonged driving, driver fatigue | High |
| 3 | Immediately communicate the alert to the respective driver | High |
| 4 | Map each vehicle to its driver so the right person is contacted | High |
| 5 | Work with the client's existing telematics platform (no replacement) | High |

## Success criteria
- Critical events trigger an alert to the correct driver automatically
- Reduced reliance on manual monitoring
- Faster response from the driver after an event is detected

## Assumptions and constraints
- The client's telematics platform already generates the safety signals
- Each bus or driver has a mapped contact number
- Integration is done through APIs, with no change to the client's telematics software beyond sending events

## Information still to capture
- Fleet size and expected daily alert volume
- Languages needed for voice messages
- Retry rules if the driver does not answer
