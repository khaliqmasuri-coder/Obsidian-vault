---
title: Aqidah Index
type: subject-index
subject: aqidah
tags:
  - aqidah
  - subject-index
---

# Aqidah Index

## Workflow

- Use [[Pre-Lesson Protocol]]
- Write with [[Core Lesson Template]]
- Append module from [[Subject Modules]]
- Track issues in [[Master Shubuhat Log]] and [[Conflict Register]]

## Aqidah Lessons (Auto - Dataview)

```dataview
TABLE file.link AS Lesson, level AS Level, lesson_no AS "#", study_date AS Date, fahm AS Fahm, next_review AS "Next Review", status AS Status
FROM "05_Lessons"
WHERE type = "lesson" AND subject = "aqidah"
SORT lesson_no ASC
```

