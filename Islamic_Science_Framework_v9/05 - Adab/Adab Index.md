---
tags: [index, adab]
aliases: [Adab Index, Ādāb Index]
---

# 🟣 Ādāb — Subject Index

> [!info] How to create a new lesson
> 1. Create a new note in the `Lessons/` folder (e.g., `Adab L02 - The Station of Tawakkul`)
> 2. Use `Ctrl/Cmd + T` → insert [[Core Lesson Template]]
> 3. Then insert [[Adab Module]] below the core template
> 4. For Intermediate level, also add [[Intermediate Additions]]
> 5. For Advanced level, also add [[Advanced Additions]]

---

## Current Text: → See [[Recommended Texts]]

## Teacher: → See [[Sanad - Adab]]

---

## Lesson Index (Dataview — Auto)

```dataview
TABLE WITHOUT ID
  file.link AS "Lesson",
  lesson_number AS "#",
  title AS "Title",
  fahm AS "Fahm",
  status AS "Status",
  last_reviewed AS "Last Reviewed",
  muraja_due AS "Murājaʿah Due"
FROM "05 - Adab/Lessons"
WHERE type = "lesson" AND !contains(tags, "template")
SORT lesson_number ASC
```

---

## Related

- [[Sanad - Adab|Sanad — Ādāb]]
- [[Shubhat - Adab|Shubhāt — Ādāb]]
- [[Recommended Texts]]
- [[Vocabulary Builder]]

---

*[[🏠 Home]] · [[Master Dashboard]] · [[Adab Index]]*
