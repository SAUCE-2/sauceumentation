---
tags:
  - project
status: active
related: []
created: "[[2026-09-14]]"
---
# Pantry Pal

**What it is:** Web app that tracks what's in my fridge and suggests dinner before things expire. Vibe-coded over a few weekends.
**Stack:** Next.js, Tailwind, [[Supabase]], Vercel
**Repo / links:** github.com/me/pantry-pal
## Decisions
- Barcode scanning in the browser, not a native app. See [[Prompt recipes]].
## Open tasks
```tasks
not done
(path includes Efforts/Pantry Pal) OR (heading includes Pantry Pal)
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
