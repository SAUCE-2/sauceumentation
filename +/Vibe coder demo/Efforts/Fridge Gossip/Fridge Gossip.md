---
tags:
  - project
status: active
related: []
created: "[[2026-10-18]]"
---
# Fridge Gossip

**What it is:** An ESP32 on the fridge door counts how often it opens, then sends me a snarky push notification. Stupid, but fun.
**Stack:** ESP32, [[MQTT]], a small LLM prompt for the snark
**Repo / links:** github.com/me/fridge-gossip
## Open tasks
```tasks
not done
(path includes Efforts/Fridge Gossip) OR (heading includes Fridge Gossip)
group by filename
group by heading
short mode
```
## Efforts
```base
filters:
  and:
    - file.hasTag("effort")
    - file.hasLink(this.file)
formulas:
  shared: if(projects.length > 1, "shared", "")
views:
  - type: table
    name: Efforts
    order:
      - file.name
      - status
      - formula.shared
      - projects
      - file.mtime
    sort:
      - property: status
        direction: ASC
      - property: file.mtime
        direction: DESC
  - type: kanban
    name: Board
    groupBy:
      property: status
      direction: ASC
    order:
      - file.name
      - formula.shared
    sort:
      - property: file.mtime
        direction: DESC
```
## Notes
```base
filters:
  and:
    - file.hasLink(this.file)
    - file.path != this.file.path
    - '!file.hasTag("effort")'
    - file.ext == "md"
views:
  - type: table
    name: Notes
    order:
      - file.name
      - tags
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
```
