---
tags:
  - map
up:
  - []
related: []
created: "[[<% tp.date.now("YYYY-MM-DD") %>]]"
---
# <% tp.file.title %>
*One sentence on what topic this map covers. Create a map once a topic has about 5 or more notes that are hard to find.*
## Key notes
*Your most important notes on this topic. Group them sensibly and add a short reason after each link.*
- 
## Related maps
- 
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
