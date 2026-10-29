---
tags:
  - source
up: []
related: []
type:
author:
url:
cover:
created: "[[<% tp.date.now("YYYY-MM-DD") %>]]"
---
# <% tp.file.title %>
*An article, video, talk, paper or docs page. Use `type` for which. For books use the Book template.*
## Summary
*What it says in two or three sentences.*
## Key points
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
