---
tags: [index, hadith]
aliases: [Hadith Index, Ḥadīth Index]
---

# 🟡 Ḥadīth — Subject Index

> [!info] How to create a new lesson
> 1. Create a new note in the `Lessons/` folder (e.g., `Hadith L02 - Hadith of Umar on Intentions`)
> 2. Use `Ctrl/Cmd + T` → insert [[Core Lesson Template]]
> 3. Then insert [[Hadith Module]] below the core template
> 4. For Intermediate level, also add [[Intermediate Additions]]
> 5. For Advanced level, also add [[Advanced Additions]]

---

## Current Text: → See [[Recommended Texts]]

## Teacher: → See [[Sanad - Hadith]]

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
FROM "04 - Hadith/Lessons"
WHERE type = "lesson" AND !contains(tags, "template")
SORT lesson_number ASC
```

---

## Related

- [[Sanad - Hadith|Sanad — Ḥadīth]]
- [[Shubhat - Hadith|Shubhāt — Ḥadīth]]
- [[Recommended Texts]]
- [[Vocabulary Builder]]

---

*[[🏠 Home]] · [[Master Dashboard]] · [[Hadith Index]]*
