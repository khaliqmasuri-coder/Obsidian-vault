---
tags: [index, tafsir]
aliases: [Tafsir Index, Tafsīr Index]
---

# 🟢 Tafsīr — Subject Index

> [!info] How to create a new lesson
> 1. Create a new note in the `Lessons/` folder (e.g., `Tafsir L02 - Surah al-Fatiha Verse 1`)
> 2. Use `Ctrl/Cmd + T` → insert [[Core Lesson Template]]
> 3. Then insert [[Tafsir Module]] below the core template
> 4. For Intermediate level, also add [[Intermediate Additions]]
> 5. For Advanced level, also add [[Advanced Additions]]

---

## Current Text: → See [[Recommended Texts]]

## Teacher: → See [[Sanad - Tafsir]]

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
FROM "03 - Tafsir/Lessons"
WHERE type = "lesson" AND !contains(tags, "template")
SORT lesson_number ASC
```

---

## Related

- [[Sanad - Tafsir|Sanad — Tafsīr]]
- [[Shubhat - Tafsir|Shubhāt — Tafsīr]]
- [[Recommended Texts]]
- [[Vocabulary Builder]]

---

*[[🏠 Home]] · [[Master Dashboard]] · [[Tafsir Index]]*
