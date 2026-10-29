---
tags:
  - map
up:
  - "[[Home]]"
related: []
created: "[[2026-09-03]]"
---
# Side projects
*Map of everything I build for fun. Projects live in Efforts, what I know about building them lives here.*
## Projects
- [[Pantry Pal]]: web app
- [[Plant Parent]]: iOS app
- [[Casa]]: house IoT
- [[Fridge Gossip]]: pointless on purpose
## Maps
- [[Vibe coding]]
- [[Home lab]]

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
