---
title: Master Shubuhat Log
type: log
tags:
  - shubuhat
  - doubts
  - tracking
---

# Master Shubuhat Log

> [!warning]
> A shubhah ignored multiplies.  
> A shubhah logged and referred is being handled responsibly.

## Logging Rules

- Write each doubt precisely (not vaguely).
- Add where it came from (lesson, speaker, post, book, etc.).
- Assign a **SH-XXX** code immediately.
- Do not close until written resolution is recorded.

## Fast Capture (Task Format for Dashboard Automation)

- [ ] SH-001 Subject:: aqidah Lesson::  Source::  Doubt::  Resolution::  #shubhah #open
- [ ] SH-002 Subject:: fiqh Lesson::  Source::  Doubt::  Resolution::  #shubhah #open
- [ ] SH-003 Subject:: tafsir Lesson::  Source::  Doubt::  Resolution::  #shubhah #open
- [ ] SH-004 Subject:: hadith Lesson::  Source::  Doubt::  Resolution::  #shubhah #open
- [ ] SH-005 Subject:: adab Lesson::  Source::  Doubt::  Resolution::  #shubhah #open

## Open Shubuhat (Auto - Dataview)

```dataview
TASK
FROM "01_Dashboards"
WHERE contains(tags, "#shubhah") AND !completed
SORT text ASC
```

## Full Reference Tables (By Subject)

### Aqidah

| Ref | Shubhah (precise) | Source | Resolution | Status |
|---|---|---|---|---|
| SH-001 |  |  |  | Open |
| SH-002 |  |  |  | Open |
| SH-003 |  |  |  | Open |
| SH-004 |  |  |  | Open |
| SH-005 |  |  |  | Open |

### Fiqh

| Ref | Shubhah (precise) | Source | Resolution | Status |
|---|---|---|---|---|
| SH-001 |  |  |  | Open |
| SH-002 |  |  |  | Open |
| SH-003 |  |  |  | Open |
| SH-004 |  |  |  | Open |
| SH-005 |  |  |  | Open |

### Tafsir

| Ref | Shubhah (precise) | Source | Resolution | Status |
|---|---|---|---|---|
| SH-001 |  |  |  | Open |
| SH-002 |  |  |  | Open |
| SH-003 |  |  |  | Open |
| SH-004 |  |  |  | Open |
| SH-005 |  |  |  | Open |

### Hadith

| Ref | Shubhah (precise) | Source | Resolution | Status |
|---|---|---|---|---|
| SH-001 |  |  |  | Open |
| SH-002 |  |  |  | Open |
| SH-003 |  |  |  | Open |
| SH-004 |  |  |  | Open |
| SH-005 |  |  |  | Open |

### Adab

| Ref | Shubhah (precise) | Source | Resolution | Status |
|---|---|---|---|---|
| SH-001 |  |  |  | Open |
| SH-002 |  |  |  | Open |
| SH-003 |  |  |  | Open |
| SH-004 |  |  |  | Open |
| SH-005 |  |  |  | Open |

