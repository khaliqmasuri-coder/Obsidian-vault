---
title: Subjects Hub
type: hub
tags:
  - subjects
  - index
---

# Subjects Hub

- [[Aqidah Index]]
- [[Fiqh Index]]
- [[Tafsir Index]]
- [[Hadith Index]]
- [[Adab Index]]

## Cross-Subject Active Lessons (Auto - Dataview)

```dataview
TABLE file.link AS Lesson, subject AS Subject, level AS Level, lesson_no AS "#", fahm AS Fahm, next_review AS "Next Review"
FROM "05_Lessons"
WHERE type = "lesson" AND status != "complete"
SORT subject ASC, lesson_no ASC
```

