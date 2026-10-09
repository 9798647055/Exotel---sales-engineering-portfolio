# Use Case: Voicebot on a SIP Trunk

## Pattern
A business that already has a chatbot or voicebot connects it to the telephone network through a **SIP trunk**. Voice flows both ways, so customers can have a natural conversation with the bot.

```
Cloud telephony platform <-> SIP trunk <-> Bot platform
        |
Customer phone (inbound or outbound call)
```

## SIP trunk vs streaming channel
| Factor | Streaming channel | SIP trunk |
|---|---|---|
| Cost at very large scale | Higher | Lower |
| Voice latency | Adds delay | Lower |
| Best for | Smaller volumes or custom stream handling | Large-scale call campaigns |

## Where it fits
| Industry | Use |
|---|---|
| Telecom | Recharge and renewal reminders |
| BFSI | Payment dues, collections, KYC follow-ups |
| Insurance | Premium reminders |
| Utilities | Bill and service reminders |

## Projects using this pattern
| Project | Industry |
|---|---|
| [Haptik (for Jio): Recharge Reminder Voicebot](../../haptik-jio-voicebot/README.md) | Telecom / Conversational AI |
