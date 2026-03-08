---
tags: [register, tafsir]
type: register
created_date: 2026-03-08
modified_date: 2026-03-08
---

# 🟢 Shubhat - Tafsir

```dataview
TABLE file.link AS Lesson, open_shubhat, last_reviewed
FROM "03 - Tafsir/Lessons"
WHERE type = "lesson" AND open_shubhat > 0
SORT open_shubhat DESC
```

*[[🏠 Home]] • [[Dashboard/Master Dashboard|Master Dashboard]] • [[Logs and Registers/Master Shubhat Log|Master Shubhat Log]]*
