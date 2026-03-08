---
tags: [dashboard, upkeep]
type: dashboard
created_date: 2026-03-08
modified_date: 2026-03-08
---

# 🧰 Obsidian Upkeep

Monthly vault health diagnostics.

## Lesson Metadata Completeness Check
```dataview
TABLE
  choice(subject, "OK", "MISSING") AS Subject,
  choice(lesson_number, "OK", "MISSING") AS Lesson_Number,
  choice(fahm, "OK", "MISSING") AS Fahm,
  choice(status, "OK", "MISSING") AS Status,
  choice(date, "OK", "MISSING") AS Date,
  choice(last_reviewed, "OK", "MISSING") AS Last_Reviewed,
  choice(muraja_due, "OK", "MISSING") AS Muraja_Due
FROM ""
WHERE type = "lesson"
```

## Files Tagged template But Not Marked type: template
```dataview
TABLE file.link, type, tags
FROM ""
WHERE contains(tags, "template") AND type != "template"
```

## Duplicate Lesson Number Audit (Per Subject)
```dataviewjs
const lessons = dv.pages()
  .where(p => p.type === "lesson");

const groups = {};
for (const p of lessons) {
  const key = `${p.subject}::${p.lesson_number}`;
  groups[key] = groups[key] ?? [];
  groups[key].push(p.file.link);
}

const duplicates = Object.entries(groups)
  .filter(([_, links]) => links.length > 1)
  .map(([key, links]) => {
    const [subject, lesson] = key.split("::");
    return [subject, lesson, links];
  });

dv.table(["Subject", "Lesson #", "Duplicates"], duplicates);
```

*[[🏠 Home]] • [[Dashboard/Master Dashboard|Master Dashboard]] • [[Logs and Registers/Khata Log|Khata Log]]*
