---
title: Master Dashboard
type: dashboard
tags:
  - dashboard
  - mastery
  - tracking
---

# Master Learning Dashboard

> 30-second orientation before every study session.

## Control Panel

- [[Islamic Science Framework Hub]]
- [[Pre-Lesson Protocol]]
- [[Core Lesson Template]]
- [[Weekly Review Protocol]]
- [[Master Shubuhat Log]]
- [[Conflict Register]]
- [[Khata Log]]

---

## Subject Progress (Auto - Dataview)

```dataview
TABLE file.link AS Lesson, subject AS Subject, level AS Level, lesson_no AS "#", fahm AS Fahm, status AS Status
FROM "05_Lessons"
WHERE type = "lesson"
SORT subject ASC, lesson_no DESC
```

## Active Lesson Queue (Auto - Dataview)

```dataview
TABLE file.link AS Lesson, subject AS Subject, level AS Level, lesson_no AS "#", mode AS Mode, fahm AS Fahm, next_review AS "Next Review", status AS Status
FROM "05_Lessons"
WHERE type = "lesson" AND status != "complete"
SORT next_review ASC, subject ASC, lesson_no ASC
```

## Reviews Due Today (Auto - Dataview)

```dataview
TABLE file.link AS Lesson, subject AS Subject, lesson_no AS "#", fahm AS Fahm, next_review AS "Next Review"
FROM "05_Lessons"
WHERE type = "lesson" AND next_review AND date(next_review) <= date(today) AND status != "complete"
SORT next_review ASC
```

## Lessons Below Fahm 3 (Auto - Dataview)

```dataview
TABLE file.link AS Lesson, subject AS Subject, lesson_no AS "#", fahm AS Fahm, status AS Status
FROM "05_Lessons"
WHERE type = "lesson" AND fahm < 3 AND status != "complete"
SORT subject ASC, lesson_no ASC
```

## Open Shubuhat / Conflict Tasks (Auto - Dataview)

```dataview
TASK
FROM ""
WHERE !completed AND (contains(tags, "#shubhah") OR contains(tags, "#conflict"))
SORT file.name ASC
```

---

## This Week's Priority Lessons (Manual Planning)

| Subject | Lesson / Topic | Priority (Green/Yellow/Black) | Reason | Mode (First/Rapid/Deep) | Status |
|---|---|---|---|---|---|
|  |  |  |  |  | ☐ |
|  |  |  |  |  | ☐ |
|  |  |  |  |  | ☐ |
|  |  |  |  |  | ☐ |
|  |  |  |  |  | ☐ |

## Open Issues (Manual Override)

| Type | Ref | Subject/Lesson | Referred To | Resolved |
|---|---|---|---|---|
| Shubhah / Conflict / Gap | SH- / CR- |  |  | ☐ |
| Shubhah / Conflict / Gap | SH- / CR- |  |  | ☐ |
| Shubhah / Conflict / Gap | SH- / CR- |  |  | ☐ |
| Shubhah / Conflict / Gap | SH- / CR- |  |  | ☐ |
| Shubhah / Conflict / Gap | SH- / CR- |  |  | ☐ |

## Weekly Cadence (Default)

- **Saturday:** New Aqidah lesson + weekly Speed Spine recall
- **Sunday:** New Fiqh lesson + Tatbiq from Saturday
- **Monday:** New Tafsir lesson + Day-3 review (Saturday)
- **Tuesday:** New Hadith lesson + Day-3 review (Sunday)
- **Wednesday:** New Adab lesson + Day-3 review (Monday)
- **Thursday:** Catch-up / deep dive / Q&A + resolve top 2 doubts
- **Friday:** [[Weekly Review Protocol]] + cross-subject integration

