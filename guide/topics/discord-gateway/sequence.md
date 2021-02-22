---
title: Sequence
---

## What's the "Sequence"?

The sequence is a number that the client keeps track of every time they received a payload.
It's given to you via the `s` property.

```json
{
  "s": 1,
  ...
}
```

This is later used for [Heart-beating](/topics/discord-gateway/heart-beating.md).
