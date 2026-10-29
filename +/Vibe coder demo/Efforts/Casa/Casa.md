---
tags:
  - project
status: active
related: []
created: "[[2026-09-06]]"
---
# Casa

**What it is:** Running the house: lights, sensors, heating and energy, all through [[Home Assistant]] on a Raspberry Pi.
**Stack:** [[Home Assistant]], [[MQTT]], Zigbee sensors, a Pi 5
**Repo / links:** casa-config repo (YAML, kept in git)

## Decisions

- [[Zigbee vs Z-Wave]]: Zigbee, because it's cheap.

## Open tasks

```tasks
not done
(path includes Efforts/Casa) OR (heading includes Casa)
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
