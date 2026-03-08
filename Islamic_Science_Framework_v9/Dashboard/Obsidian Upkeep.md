---
tags: [dashboard, upkeep, maintenance]
aliases: [Obsidian Upkeep]
---

# 🔧 Obsidian Upkeep — Monthly Health Diagnostics

> [!info] Run this once a month to keep your vault healthy. A well-maintained vault means your Dataview queries stay accurate and your notes remain findable.

---

## 📊 Vault Health Overview

### Total Lessons by Subject

```dataviewjs
const lessons = dv.pages().where(p => p.type === "lesson" && !p.tags?.includes("template"));
const subjects = ["Aqidah", "Fiqh", "Tafsir", "Hadith", "Adab"];
const rows = subjects.map(s => {
  const subjectLessons = lessons.where(p => p.subject === s);
  return [s, subjectLessons.length];
});
dv.table(["Subject", "Lesson Count"], rows);
```

### Lessons Missing Key Fields

```dataviewjs
const lessons = dv.pages().where(p => p.type === "lesson" && !p.tags?.includes("template"));
const missing = lessons.where(p => !p.fahm || !p.date || !p.muraja_due || !p.last_reviewed);
if (missing.length > 0) {
  dv.table(
    ["Lesson", "Missing Fields"],
    missing.map(p => {
      let fields = [];
      if (!p.fahm) fields.push("fahm");
      if (!p.date) fields.push("date");
      if (!p.muraja_due) fields.push("muraja_due");
      if (!p.last_reviewed) fields.push("last_reviewed");
      return [p.file.link, fields.join(", ")];
    })
  );
} else {
  dv.paragraph("✅ All lessons have complete frontmatter.");
}
```

### Orphaned Notes (No Tags)

```dataviewjs
const orphans = dv.pages().where(p => !p.tags || p.tags.length === 0);
if (orphans.length > 0) {
  dv.table(["File", "Folder"], orphans.map(p => [p.file.link, p.file.folder]));
} else {
  dv.paragraph("✅ No orphaned notes found.");
}
```

### Unresolved Shubhāt Count

```dataviewjs
const lessons = dv.pages().where(p => p.type === "lesson" && !p.tags?.includes("template") && p.open_shubhat > 0);
if (lessons.length > 0) {
  const total = lessons.values.reduce((sum, p) => sum + (p.open_shubhat || 0), 0);
  dv.paragraph(`🟠 **${total} open shubhāt** across ${lessons.length} lessons.`);
  dv.table(["Lesson", "Open Shubhāt"], lessons.map(p => [p.file.link, p.open_shubhat]));
} else {
  dv.paragraph("✅ No open shubhāt.");
}
```

---

## 🔍 Monthly Checklist

- [ ] All lesson files have complete YAML frontmatter
- [ ] No duplicate `lesson_number` values within the same subject
- [ ] All `muraja_due` dates are set and realistic
- [ ] Master Shubhāt Log entries match `open_shubhat` counts in lessons
- [ ] Conflict Register entries are up to date
- [ ] Khataʾ Log has been reviewed for patterns
- [ ] Weekly Reviews have been completed for the past 4 weeks
- [ ] 90-Day Tracker is up to date
- [ ] Anki cards are synced with lesson Speed Spines
- [ ] Obsidian Git is backing up regularly

---

## 🗑️ Cleanup Tasks

- [ ] Remove any stray files not in the standard folder structure
- [ ] Verify all `[[wikilinks]]` resolve to existing files
- [ ] Check that template files are NOT tagged with `lesson`
- [ ] Archive completed weekly reviews older than 90 days

---

*[[🏠 Home]] · [[Master Dashboard]] · [[Obsidian Upkeep]]*
