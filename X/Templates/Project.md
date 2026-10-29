---
tags:
  - project
status: active
related: []
created: "[[<% tp.date.now("YYYY-MM-DD") %>]]"
---
# <% tp.file.title %>
*The main page for this project. Make one per project folder. It automatically lists every effort that has this project in its `projects` property, including shared efforts stored in other folders.*
**What it is:** *One or two sentences on what this project is.*
**Repo / links:** *Where the code and other resources live.*
## Decisions
*Link the notes that explain why the project is built the way it is.*
## Open tasks
```tasks
not done
(path includes <% tp.file.folder(true) %>) OR (heading includes <% tp.file.title %>)
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
