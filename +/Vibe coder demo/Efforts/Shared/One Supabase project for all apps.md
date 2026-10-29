---
tags:
  - effort
aliases:
status: done
projects:
  - "[[Pantry Pal]]"
  - "[[Plant Parent]]"
related: []
created: "[[2026-09-21]]"
---
# One Supabase project for all apps
*Shared effort: auth and storage for [[Pantry Pal]] and [[Plant Parent]] from one free-tier project.*
**Definition of done:** Both apps sign in against the same project with separate schemas.
## Why
Free tier gives me one project. See [[Supabase]].
## Pantry Pal
- [x] Schema `pantry`
- [x] Row-level security
## Plant Parent
- [x] Schema `plants`
- [x] Sign in with Apple
