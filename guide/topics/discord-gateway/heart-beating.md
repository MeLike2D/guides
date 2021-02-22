---
title: Heart-beating
---

## What is Heart-beating

Heartbeats are used by Discord to make sure they aren't sending events to a dead discord bot.
However, it can also be used by the client (your bot) to determine whether there is a zombied or failed connection, or in other words, a service outage.

## How do I start?

To start heart-beating, you'll have to get the `heartbeat_interval` described in the gateway event, [`HELLO`](https://discord.com/developers/docs/topics/gateway#hello).

---

Now every `x` milliseconds the client will send a [`HEARTBEAT` command](https://discord.com/developers/docs/topics/gateway#heartbeat).

- `op` being the operation code, so in this case `1` because we are sending a heartbeat
- `s` being the latest [sequence](/topics/discord-gateway/sequence.md)

```js
<Gateway>.send({
  op: 1,
  d: 1 
})
```

## Detecting a Zombied or Failed Connection.

Zombie connections, aka a service outage can be detected by either not being able to connect to the gateway or lack of `Heartbeat ACK` payloads.

--- 

Whenever the client sends a heart-beat command the gateway should respond back with an operation code `11`  or `Heartbeat ACK`. However, if it doesn't we can assume that a zombied or failed connection has occured and we should wait until the gateway has responded.

