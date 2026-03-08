---
tags: [dashboard, framework]
type: dashboard
version: 9.0
created_date: 2026-03-08
modified_date: 2026-03-08
---

# 📊 Master Dashboard

Your 30-second orientation point before every study session.

## Subject Health Snapshot
```dataview
TABLE
  length(rows) AS "Lessons",
  round(average(rows.fahm), 1) AS "Avg Fahm",
  min(rows.muraja_due) AS "Next Muraja",
  max(rows.last_reviewed) AS "Last Reviewed"
FROM ""
WHERE type = "lesson" AND contains(tags, "lesson")
GROUP BY subject
SORT subject ASC
```

## Murajaʿah Due / Overdue
```dataviewjs
const lessons = dv.pages()
  .where(p => p.type === "lesson" && p.muraja_due);
const parsed = lessons.map(p => {
  const due = dv.luxon.DateTime.fromFormat(String(p.muraja_due), "dd/MM/yyyy");
  return { p, due };
}).where(x => x.due.isValid)
  .sort((a, b) => a.due.toMillis() - b.due.toMillis());

const today = dv.luxon.DateTime.now().startOf("day");
dv.table(
  ["Subject", "Lesson", "Muraja Due", "Status"],
  parsed
    .filter(x => x.due <= today)
    .map(x => [x.p.subject, x.p.file.link, x.p.muraja_due, x.p.status ?? "active"])
);
```

## Lessons With Open Shubhāt
```dataview
TABLE subject, lesson_number, open_shubhat, file.link AS Lesson
FROM ""
WHERE type = "lesson" AND open_shubhat > 0
SORT open_shubhat DESC
```

## Stale Notes (No Review in 14+ Days)
```dataviewjs
const stale = dv.pages()
  .where(p => p.type === "lesson" && p.last_reviewed)
  .map(p => {
    const reviewed = dv.luxon.DateTime.fromFormat(String(p.last_reviewed), "dd/MM/yyyy");
    const age = reviewed.isValid ? Math.floor(dv.luxon.DateTime.now().diff(reviewed, "days").days) : null;
    return { p, age };
  })
  .where(x => x.age !== null && x.age >= 14)
  .sort((a, b) => b.age - a.age);

dv.table(
  ["Subject", "Lesson", "Last Reviewed", "Days Old"],
  stale.map(x => [x.p.subject, x.p.file.link, x.p.last_reviewed, x.age])
);
```

## ✅ Completed (status: mastered)
```dataview
TABLE subject, lesson_number, fahm, last_reviewed, file.link AS Lesson
FROM ""
WHERE type = "lesson" AND status = "mastered"
SORT subject ASC, lesson_number ASC
```

---
Framework v9.0

*[[🏠 Home]] • [[Dashboard/Master Dashboard|Master Dashboard]] • [[Dashboard/Daily Study Engine|Daily Study Engine]]*
