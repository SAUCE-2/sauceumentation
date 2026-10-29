---
tags:
  - effort
aliases:
status: active
projects:
  - "[[<% tp.file.folder() %>]]"
up: []
related: []
created: "[[<% tp.date.now("YYYY-MM-DD") %>]]"
---
# <% tp.file.title %>
*A piece of work with a clear finish, like a feature, a fix or something you're working on. Keep it in the folder of the project/area it belongs to. If other projects share it, add them to `projects`. Status is `backlog`, `active` or `done`.*
**Definition of done:** *One sentence describing what is true when this is finished.*
## Why
*Why this is worth doing. Link the ideas, decisions or notes behind it.*
## Ideas behind this
```base
filters:
  and:
    - file.hasTag("idea")
    - this.file.hasLink(file)
views:
  - type: table
    name: Ideas
    order:
      - file.name
      - up
    sort:
      - property: file.name
        direction: ASC
```
## Actions
- [ ] *Next step to take*
