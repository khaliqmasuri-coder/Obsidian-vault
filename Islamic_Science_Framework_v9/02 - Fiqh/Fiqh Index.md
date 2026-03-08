---
tags: [index, fiqh]
aliases: [Fiqh Index]
---

# 🔵 Fiqh — Subject Index

> [!info] How to create a new lesson
> 1. Create a new note in the `Lessons/` folder (e.g., `Fiqh L02 - Conditions of Salah`)
> 2. Use `Ctrl/Cmd + T` → insert [[Core Lesson Template]]
> 3. Then insert [[Fiqh Module]] below the core template
> 4. For Intermediate level, also add [[Intermediate Additions]]
> 5. For Advanced level, also add [[Advanced Additions]]

---

## Current Text: → See [[Recommended Texts]]

## Teacher: → See [[Sanad - Fiqh]]

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
FROM "02 - Fiqh/Lessons"
WHERE type = "lesson" AND !contains(tags, "template")
SORT lesson_number ASC
```

---

## Related

- [[Sanad - Fiqh|Sanad — Fiqh]]
- [[Shubhat - Fiqh|Shubhāt — Fiqh]]
- [[Recommended Texts]]
- [[Vocabulary Builder]]

---

*[[🏠 Home]] · [[Master Dashboard]] · [[Fiqh Index]]*
