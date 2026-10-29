---
tags:
  - map
up:
  - "[[Side projects]]"
related: []
created: "[[2026-09-03]]"
---
# Vibe coding
*How I build with an AI pair. What works, what doesn't.*
## Key notes
- [[Prompt recipes]]: prompts I keep reusing
- [[Vibe coding rules]]: the ground rules after getting burnt
- [[Supabase]]: the backend I reach for
- [[SwiftUI]]: the iOS bits
- [[Widget]]: a word that means two things in my projects
- [[Phone widget beats app]]: idea behind Plant Parent
- [[Read the diff]]: lesson from a bad week
## Related maps
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
