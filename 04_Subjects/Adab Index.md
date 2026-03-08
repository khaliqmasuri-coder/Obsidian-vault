---
title: Adab Index
type: subject-index
subject: adab
tags:
  - adab
  - subject-index
---

# Adab Index

## Adab Lessons (Auto - Dataview)

```dataview
TABLE file.link AS Lesson, level AS Level, lesson_no AS "#", study_date AS Date, fahm AS Fahm, next_review AS "Next Review", status AS Status
FROM "05_Lessons"
WHERE type = "lesson" AND subject = "adab"
SORT lesson_no ASC
```

