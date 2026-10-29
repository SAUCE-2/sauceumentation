---
tags:
  - daily-note
---
# <% tp.date.now("dddd, Do MMM YYYY") %>
## Tasks
### Due & reminders
```tasks
not done
(due before <% tp.date.now("YYYY-MM-DD", 1) %>) OR (description includes ⏰ <% tp.date.now("YYYY-MM-DD") %>)
path does not include +/
sort by due
```
## Notes
## Linked to today
```base
filters:
  and:
    - file.ext == "md"
    - file.path != this.file.path
    - '!file.inFolder("Templates")'
    - file.hasLink(this.file)
views:
  - type: table
    name: Linked to today
    order:
      - file.name
      - tags
      - file.folder
    sort:
      - property: file.name
        direction: ASC
```
