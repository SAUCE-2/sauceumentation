---
tags:
  - idea
up: []
related: []
created: "[[<% tp.date.now("YYYY-MM-DD") %>]]"
---
# <% tp.file.title %>
**Claim:** *State the idea in one sentence. It should be something that could turn out to be wrong.*
## Because
*The reasons you believe this.*
## Impact
*Which efforts would change if this is true. Link to them.*
## Used by
```base
filters:
  and:
    - file.hasTag("effort")
    - file.hasLink(this.file)
views:
  - type: table
    name: Efforts using this idea
    order:
      - file.name
      - status
      - projects
    sort:
      - property: file.mtime
        direction: DESC
```
