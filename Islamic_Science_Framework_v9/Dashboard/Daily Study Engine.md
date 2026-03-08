---
tags: [dashboard, daily-engine]
type: dashboard
created_date: 2026-03-08
modified_date: 2026-03-08
---

# ⏰ Daily Study Engine

## Dynamic Daily Recommendation
```dataviewjs
const schedule = {
  Saturday: "Aqidah",
  Sunday: "Fiqh",
  Monday: "Tafsir",
  Tuesday: "Hadith",
  Wednesday: "Adab",
  Thursday: "Catch-up / Deep Dive / Teacher Q&A",
  Friday: "Weekly Review Protocol"
};

const today = dv.luxon.DateTime.now();
const dayName = today.toFormat("cccc");
const focus = schedule[dayName] ?? "Review";

const lessons = dv.pages()
  .where(p => p.type === "lesson");

const dueRows = lessons
  .where(p => p.muraja_due)
  .map(p => {
    const due = dv.luxon.DateTime.fromFormat(String(p.muraja_due), "dd/MM/yyyy");
    return { p, due };
  })
  .where(x => x.due.isValid && x.due <= today.startOf("day"))
  .sort((a, b) => a.due.toMillis() - b.due.toMillis());

const overdue = dueRows.length ? dueRows[0] : null;

dv.paragraph(`**Today (${dayName})**: ${focus}`);
if (overdue) {
  dv.paragraph(`**Oldest overdue muraja:** ${overdue.p.file.link} (due ${overdue.p.muraja_due})`);
} else {
  dv.paragraph("**Oldest overdue muraja:** None overdue. Proceed with new lesson focus.");
}
```

## Non-Negotiable 20-Minute Minimum
1. **Mins 1-5:** Speed Spine recall (3 random lessons, memory only)
2. **Mins 6-12:** New lesson or rapid review (based on schedule)
3. **Mins 13-17:** Taṭbīq out loud (Scenario 1 from yesterday)
4. **Mins 18-20:** Athar al-Qalb and duʿa review

## Weekly Architecture
- **Saturday:** New Lesson (Aqidah) + weekly speed spine sweep
- **Sunday:** New Lesson (Fiqh) + Saturday Taṭbīq out loud
- **Monday:** New Lesson (Tafsir) + Day-3 review of Saturday
- **Tuesday:** New Lesson (Hadith) + Day-3 review of Sunday
- **Wednesday:** New Lesson (Adab) + Day-3 review of Monday
- **Thursday:** Catch-up / Deep Dive / Teacher Q&A + resolve top 2 Shubhāt
- **Friday:** Weekly review + cross-subject integration

*[[🏠 Home]] • [[Dashboard/Master Dashboard|Master Dashboard]] • [[Templates/Weekly Review|Weekly Review]]*
