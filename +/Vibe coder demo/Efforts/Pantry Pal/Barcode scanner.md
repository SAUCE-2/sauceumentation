---
tags:
  - effort
aliases:
status: active
projects:
  - "[[Pantry Pal]]"
related: []
created: "[[2026-09-15]]"
---
# Barcode scanner
**Definition of done:** Point the phone at a tin, and it lands in the pantry with a name and expiry guess.
## Why
Typing in groceries is why the last three attempts at this died. Scan or nothing.
## Actions
- [x] Camera permission flow on mobile Safari
- [x] Look up barcodes with the Open Food Facts API
- [ ] Fallback when the barcode isn't found: ask for a photo and let the model name it
- [ ] Fix scanner freezing on Android Chrome

```tasks
not done
path includes {{query.file.path}}
heading does not include Actions
group by heading
short mode
```
