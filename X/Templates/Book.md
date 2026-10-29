---
tags:
  - book
up: []
related: []
author:
cover:
status: want
started:
finished:
rating:
created: "[[<% tp.date.now("YYYY-MM-DD") %>]]"
---
# <% tp.file.title %>
*Status is `want`, `reading` or `done`. Rating is 1 to 5.*
## Why read it
*What made you pick it up.*
## Notes
- 
## Insights from this
```base
filters:
  and:
    - file.hasTag("insight")
    - file.hasLink(this.file)
views:
  - type: table
    name: Insights
    order:
      - file.name
      - up
    sort:
      - property: file.mtime
        direction: DESC
```
