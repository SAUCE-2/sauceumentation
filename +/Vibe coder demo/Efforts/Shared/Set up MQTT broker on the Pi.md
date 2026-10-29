---
tags:
  - effort
aliases:
status: active
projects:
  - "[[Casa]]"
  - "[[Fridge Gossip]]"
related: []
created: "[[2026-10-18]]"
---
# Set up MQTT broker on the Pi
*Shared effort: both [[Casa]] and [[Fridge Gossip]] need a broker.*
**Definition of done:** Mosquitto runs on the Pi, survives a reboot, and both projects publish to it.
## Why
Stop hard-coding two separate setups. See [[MQTT]].
## Casa
- [x] Install the Mosquitto add-on in [[Home Assistant]]
- [ ] Move the Zigbee2MQTT topics under `casa/`
## Fridge Gossip
- [x] Point the ESP32 at the Pi's address
- [ ] Add a username and password
