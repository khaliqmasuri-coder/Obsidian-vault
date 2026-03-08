---
tags: [engine, daily, weekly, schedule]
aliases: [Daily Study Engine]
---

# ⏰ Daily Study Engine — The System You Run Every Day

> [!danger] Why This Section Exists
> The original framework had a weekly review but no daily engine. This is what was missing. Mastery is not built in lessons — it is built in the **daily 20-minute habit** between lessons. This page runs that habit.

---

## 📌 Today's Dynamic Recommendations

### 🟢 Today's Recommended New Lesson

```dataview
TABLE WITHOUT ID
  file.link AS "Lesson",
  subject AS "Subject",
  lesson_number AS "#",
  fahm AS "Fahm",
  status AS "Status"
FROM -"Templates"
WHERE type = "lesson" AND !contains(tags, "template") AND status = "active" AND fahm < 3
SORT lesson_number ASC
LIMIT 3
```

### 🟡 Oldest Overdue Murājaʿah

```dataview
TABLE WITHOUT ID
  file.link AS "Lesson",
  subject AS "Subject",
  lesson_number AS "#",
  muraja_due AS "Due Date",
  fahm AS "Fahm"
FROM -"Templates"
WHERE type = "lesson" AND !contains(tags, "template") AND muraja_due AND muraja_due <= date(today)
SORT muraja_due ASC
LIMIT 3
```

---

## 📅 Daily Minimum — The Non-Negotiable 20 Minutes

| Time Block | Activity | Tool | Duration | Check |
|---|---|---|---|---|
| **Mins 1–5** | **Speed Spine Recall:** pick 3 random past lessons, recall Speed Spine from memory only | Notebook or Anki | 5 min | - [ ] |
| **Mins 6–12** | **New Lesson OR Rapid Review:** First Study if new content, Rapid Review if within 7-day window | [[Core Lesson Template\|Framework Template]] | 7 min | - [ ] |
| **Mins 13–17** | **Taṭbīq Out Loud:** speak Scenario 1 from yesterday's lesson without looking | Voice / Notes | 5 min | - [ ] |
| **Mins 18–20** | **Athar al-Qalb:** read your duʿāʾ entry from the lesson. Make it. Mean it. | Notes | 2 min | - [ ] |

---

## 📆 Weekly Architecture

| Day | Primary Activity | Secondary Activity | Min Time |
|---|---|---|---|
| **Saturday** | New Lesson (ʿAqīdah) | Speed Spine of all this week's lessons | 60 min |
| **Sunday** | New Lesson (Fiqh) | Taṭbīq Scenario 1 from Saturday's lesson out loud | 60 min |
| **Monday** | New Lesson (Tafsīr) | Day-3 Rapid Review of Saturday's lesson | 60 min |
| **Tuesday** | New Lesson (Ḥadīth) | Day-3 Rapid Review of Sunday's lesson | 60 min |
| **Wednesday** | New Lesson (Ādāb) | Day-3 Rapid Review of Monday's lesson | 60 min |
| **Thursday** | Catch-up / Deep Dive / Teacher Q&A | Resolve top 2 Shubhāt from the week | 45 min |
| **Friday** | [[Weekly Review\|Weekly Review Protocol]] | Cross-Subject Integration exercise | 30 min |

---

## 🔄 Murājaʿah (Review) Schedule

This is embedded in every lesson, but here it is as a reference:

| Review Point | What to Do | How Long |
|---|---|---|
| **Day 1** (today) | Initial capture. Speed Spine written. Taṭbīq completed. Fahm rated. | Full lesson |
| **Day 3** | Rapid Review — Speed Spine from memory only. If fails → re-study first. | 15 min |
| **Day 7** | Full Rapid Review + redo Taṭbīq Scenario 1 out loud. | 20 min |
| **Day 14** | Redo Taṭbīq Scenarios 2 & 3 out loud. Create/review Anki cards. | 25 min |
| **Day 30** | Monthly review. Re-rate Fahm. Has your level improved? | 20 min |

---

*[[🏠 Home]] · [[Master Dashboard]] · [[Daily Study Engine]]*
