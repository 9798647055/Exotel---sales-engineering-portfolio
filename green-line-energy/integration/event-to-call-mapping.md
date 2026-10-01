# Event to Voice-Alert Mapping

How each telematics signal maps to an automated driver call.

| Telematics signal | Trigger condition | Who is called | Alert intent | Sample message |
|---|---|---|---|---|
| Overspeeding | Speed above the client-defined limit | Driver of the bus | Slow down immediately | "Your bus is currently overspeeding. Please reduce the speed and drive safely." |
| Engine overheating | Engine temperature above the defined threshold | Driver of the bus | Check the vehicle, stop safely if needed | _Sample wording, to be confirmed with client_ |
| Extended driving hours | Continuous driving beyond the allowed duration | Driver of the bus | Take a break | _Sample wording, to be confirmed with client_ |
| Driver fatigue / break required | Fatigue or mandatory-break condition | Driver of the bus | Rest before continuing | _Sample wording, to be confirmed with client_ |
| Other predefined safety conditions | As defined by client | Driver of the bus | As defined | _To be added_ |

Only the overspeeding message above is confirmed. The other wording is to be filled in from the project records.

## Processing logic
1. Receive event with **bus identifier** and **event type**
2. Look up the **driver mapped to the bus**
3. Select the **message for the event type**
4. Place the **outbound call** to the driver
5. Record the call outcome

## Data exchanged
| Field | Direction | Description |
|---|---|---|
| Bus ID | Telematics to Exotel | Identifies the vehicle |
| Event type | Telematics to Exotel | Overspeeding, overheating, etc. |
| Driver number | Mapping table | Number to be called |
| Call status | Exotel to client (if used) | Answered / not answered |

## Open items
- Retry rules if the driver does not answer
- Whether call status is reported back to the client's system
- Alert frequency limits so a driver is not called repeatedly for the same event
