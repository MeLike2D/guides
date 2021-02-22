---
title: Introduction to the Discord Gateway authors:
- melike2d 
categories:
- Javascript 
tags:
- Discord
- Bot Development
- WebSockets
---

An introduction to the Discord Gateway and it's quirks.

## Introduction

If you've ever wondered how discord libraries such as [discord.js](https://discord.js.org)
or [eris](https://abal.moe/Eris) work then feel free to keep reading!

The Discord Gateway is used for real-time communication between your bot and Discord. It allows your application to
receive [events](#gateway-events) (such as `MESSAGE_CREATE`) and send [commands](#commands). It's the core for each and
every Discord Bot, albeit being only half an actual Discord Bot.

---

Here are the core concepts for successfully implementing the Discord Gateway.

- [Heart-Beating](/topics/discord-gateway/heart-beating.md)
- [Identification](/topics/discord-gateway/identification.md)
- [Rate-limiting](/topics/discord-gateway/rate-limiting.md)
- [Sharding](/topics/discord-gateway/sharding.md)

## Gateway Events

Events are payloads describing a **Discord Event** that just occurred, such as sending a message, deleting a message,
and editing a message. There are quite a few of them.

- [**List of Gateway Events**](https://discord.com/developers/docs/topics/gateway#commands-and-events-gateway-events)

## Commands

Commands are requests sent do Discord, e.g. Updating your Bot's Presence, or heart-beating, which will be explained in
another page.
