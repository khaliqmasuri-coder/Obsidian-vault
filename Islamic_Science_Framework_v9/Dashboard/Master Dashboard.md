---
tags: [dashboard, tracking, mastery]
aliases: [Master Dashboard, Dashboard]
type: dashboard
---

# 📊 Master Learning Dashboard

> [!danger] Fill this in once. Update continuously.
> This is your **30-second orientation** — the first thing you look at every study session.

---

## Subject Progress (Dataview — Auto)

```dataview
TABLE WITHOUT ID
  subject AS "Subject",
  length(rows) AS "Lessons",
  round(average(rows.fahm), 1) AS "Avg Fahm",
  min(rows.muraja_due) AS "Next Review Due"
FROM -"Templates"
WHERE type = "lesson" AND !contains(tags, "template")
GROUP BY subject
SORT subject ASC
```

## All Lessons Overview

```dataview
TABLE WITHOUT ID
  file.link AS "Lesson",
  subject AS "Subject",
  lesson_number AS "#",
  fahm AS "Fahm",
  status AS "Status",
  last_reviewed AS "Last Reviewed",
  muraja_due AS "Murājaʿah Due"
FROM -"Templates"
WHERE type = "lesson" AND !contains(tags, "template")
SORT subject ASC, lesson_number ASC
```

---

## 🟡 Murājaʿah Due (Reviews Overdue)

```dataview
TABLE WITHOUT ID
  file.link AS "Lesson",
  subject AS "Subject",
  lesson_number AS "#",
  fahm AS "Fahm",
  muraja_due AS "Due Date"
FROM -"Templates"
WHERE type = "lesson" AND !contains(tags, "template") AND muraja_due AND muraja_due <= date(today)
SORT muraja_due ASC
```

---

## 🔴 Lessons Below Fahm ③

```dataview
TABLE WITHOUT ID
  file.link AS "Lesson",
  subject AS "Subject",
  lesson_number AS "#",
  fahm AS "Fahm",
  status AS "Status"
FROM -"Templates"
WHERE type = "lesson" AND !contains(tags, "template") AND fahm < 3
SORT subject ASC, lesson_number ASC
```

---

## 🟠 Lessons With Open Shubhāt

```dataview
TABLE WITHOUT ID
  file.link AS "Lesson",
  subject AS "Subject",
  open_shubhat AS "Open Shubhāt"
FROM -"Templates"
WHERE type = "lesson" AND !contains(tags, "template") AND open_shubhat > 0
SORT open_shubhat DESC
```

---

## 🏆 Completed Lessons (Mastered)

```dataview
TABLE WITHOUT ID
  file.link AS "Lesson",
  subject AS "Subject",
  lesson_number AS "#",
  fahm AS "Fahm",
  last_reviewed AS "Last Reviewed"
FROM -"Templates"
WHERE type = "lesson" AND !contains(tags, "template") AND status = "mastered"
SORT subject ASC, lesson_number ASC
```

---

## 📅 Stale Notes (Not Reviewed in 30+ Days)

```dataview
TABLE WITHOUT ID
  file.link AS "Lesson",
  subject AS "Subject",
  last_reviewed AS "Last Reviewed",
  fahm AS "Fahm"
FROM -"Templates"
WHERE type = "lesson" AND !contains(tags, "template") AND last_reviewed AND (date(today) - last_reviewed).days > 30
SORT last_reviewed ASC
```

---

## ⚡ This Week's Priority Lessons

| Subject | Lesson / Topic | Priority Reason | Mode | Status |
|---|---|---|---|---|
| | | | 🟢 / 🟡 / ⚫ | |
| | | | 🟢 / 🟡 / ⚫ | |
| | | | 🟢 / 🟡 / ⚫ | |
| | | | 🟢 / 🟡 / ⚫ | |
| | | | 🟢 / 🟡 / ⚫ | |

---

## 🔴 Open Issues — Resolve Before Advancing

| Type | Issue | Subject / Lesson | Referred To | Resolved |
|---|---|---|---|---|
| Shubhah / Conflict / Gap | | | SH-XXX / CR-XXX | - [ ] |
| Shubhah / Conflict / Gap | | | SH-XXX / CR-XXX | - [ ] |
| Shubhah / Conflict / Gap | | | SH-XXX / CR-XXX | - [ ] |

---

## Quick Links

- [[Daily Study Engine]] — Your daily 20-minute system
- [[Anki Card System]] — Spaced repetition cards
- [[Master Shubhat Log|Master Shubhāt Log]] — All doubts tracked
- [[Conflict Register]] — All conflicts tracked
- [[Khata Log|Khataʾ Log]] — All mistakes tracked
- [[Level Transition Gates]] — Advancement criteria
- [[90-Day Tracker]] — Habit tracker

---

*[[🏠 Home]] · [[Master Dashboard]] · [[Daily Study Engine]]*
*Islamic Science Framework v9.0*
