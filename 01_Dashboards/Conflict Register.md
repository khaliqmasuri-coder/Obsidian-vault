---
title: Conflict Register
type: log
tags:
  - conflict
  - usul
  - tracking
---

# Conflict Register

## Conflict Types

1. **Textual:** Two texts appear to conflict (attempt *jam'* first).
2. **Usuli:** A ruling appears to conflict with a foundational principle.
3. **Personal:** New evidence conflicts with your previously held position.

## Fast Capture (Task Format for Dashboard Automation)

- [ ] CR-001 Type:: textual New::  Earlier::  Resolution::  #conflict #open
- [ ] CR-002 Type:: usuli New::  Earlier::  Resolution::  #conflict #open
- [ ] CR-003 Type:: personal New::  Earlier::  Resolution::  #conflict #open

## Open Conflicts (Auto - Dataview)

```dataview
TASK
FROM "01_Dashboards"
WHERE contains(tags, "#conflict") AND !completed
SORT text ASC
```

## Entries

| Ref | New Lesson / Principle | Earlier Principle (lesson ref) | Type | Resolution | Status |
|---|---|---|---|---|---|
| CR-001 |  |  | Textual / Usuli / Personal |  | Open |
| CR-002 |  |  | Textual / Usuli / Personal |  | Open |
| CR-003 |  |  | Textual / Usuli / Personal |  | Open |
| CR-004 |  |  | Textual / Usuli / Personal |  | Open |
| CR-005 |  |  | Textual / Usuli / Personal |  | Open |
| CR-006 |  |  | Textual / Usuli / Personal |  | Open |
| CR-007 |  |  | Textual / Usuli / Personal |  | Open |
| CR-008 |  |  | Textual / Usuli / Personal |  | Open |

