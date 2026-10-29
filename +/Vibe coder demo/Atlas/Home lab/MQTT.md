---
tags:
  - note
sources: []
up:
  - "[[Home lab]]"
related: []
created: "[[2026-10-18]]"
---
# MQTT
*A tiny publish/subscribe protocol. Devices publish to a topic, anything can subscribe.*
- Broker: Mosquitto on the Pi. See [[Set up MQTT broker on the Pi]].
- Topic names: `casa/<room>/<thing>` and `fridge/door`.
- Used by [[Casa]] and [[Fridge Gossip]].
