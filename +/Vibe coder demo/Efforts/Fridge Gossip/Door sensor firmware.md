---
tags:
  - effort
aliases:
status: done
projects:
  - "[[Fridge Gossip]]"
related: []
created: "[[2026-10-18]]"
---
# Door sensor firmware
**Definition of done:** The ESP32 publishes every open and close to the broker.
## Why
The hardware has to work before the jokes do.
## Actions
- [x] Reed switch on GPIO 4
- [x] Debounce
- [x] Publish to `fridge/door`

```tasks
not done
path includes {{query.file.path}}
heading does not include Actions
group by heading
short mode
```
