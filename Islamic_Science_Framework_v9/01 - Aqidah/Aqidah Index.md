---
tags: [index, aqidah]
aliases: [Aqidah Index, ʿAqīdah Index]
---

# 🔴 ʿAqīdah — Subject Index

> [!info] How to create a new lesson
> 1. Create a new note in the `Lessons/` folder (e.g., `Aqidah L02 - Kashf al-Shubhat Lesson 1`)
> 2. Use `Ctrl/Cmd + T` → insert [[Core Lesson Template]]
> 3. Then insert [[Aqidah Module]] below the core template
> 4. For Intermediate level, also add [[Intermediate Additions]]
> 5. For Advanced level, also add [[Advanced Additions]]

---

## Current Text: → See [[Recommended Texts]]

## Teacher: → See [[Sanad - Aqidah]]

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
FROM "01 - Aqidah/Lessons"
WHERE type = "lesson" AND !contains(tags, "template")
SORT lesson_number ASC
```

---

## Related

- [[Sanad - Aqidah|Sanad — ʿAqīdah]]
- [[Shubhat - Aqidah|Shubhāt — ʿAqīdah]]
- [[Recommended Texts]]
- [[Vocabulary Builder]]

---

*[[🏠 Home]] · [[Master Dashboard]] · [[Aqidah Index]]*
