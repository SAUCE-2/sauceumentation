---
tags:
  - map
up:
  - "[[Side projects]]"
related: []
created: "[[2026-09-06]]"
---
# Home lab
*The Pi, the sensors and the plumbing behind [[Casa]] and [[Fridge Gossip]].*
## Key notes
- [[Home Assistant]]
- [[MQTT]]
- [[Zigbee vs Z-Wave]]
- [[Broker]]: the MQTT server both projects share
- [[Boring automations win]]: idea that keeps Casa simple
## Related maps
- [[Vibe coding]]

## Everything linking here
```base
filters:
  and:
    - file.hasLink(this.file)
    - file.ext == "md"
views:
  - type: table
    name: Links here
    order:
      - file.name
      - tags
      - file.folder
    sort:
      - property: file.mtime
        direction: DESC
```
