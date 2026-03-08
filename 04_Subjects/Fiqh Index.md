---
title: Fiqh Index
type: subject-index
subject: fiqh
tags:
  - fiqh
  - subject-index
---

# Fiqh Index

## Fiqh Lessons (Auto - Dataview)

```dataview
TABLE file.link AS Lesson, level AS Level, lesson_no AS "#", study_date AS Date, fahm AS Fahm, next_review AS "Next Review", status AS Status
FROM "05_Lessons"
WHERE type = "lesson" AND subject = "fiqh"
SORT lesson_no ASC
```

