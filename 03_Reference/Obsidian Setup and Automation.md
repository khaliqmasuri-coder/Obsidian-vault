---
title: Obsidian Setup and Automation
type: reference
tags:
  - obsidian
  - setup
  - automation
---

# Obsidian Setup and Automation

## One-Click Community Plugin Links

- [Dataview](obsidian://show-plugin?id=dataview)
- [Templater](obsidian://show-plugin?id=templater-obsidian)
- [Calendar](obsidian://show-plugin?id=calendar)
- [Tasks](obsidian://show-plugin?id=obsidian-tasks-plugin)

> If those links do not open directly on your device, install the same plugins from Obsidian Settings -> Community plugins -> Browse.

## Core Plugins (Recommended)

- Daily notes
- Templates
- Backlinks
- Outgoing links
- Command palette

## Community Plugins (Optional but Powerful)

- **Dataview** (for auto dashboards in this vault)
- **Templater** (for fast note creation)
- **Tasks** (for SH/CR task workflow)
- **Calendar** (for daily/weekly review rhythm)

## Vault Is Already Preconfigured

This vault now includes:

- `.obsidian/community-plugins.json`
- `.obsidian/core-plugins.json`
- `.obsidian/daily-notes.json`
- `.obsidian/templates.json`
- plugin data files for Dataview, Templater, Calendar, and Tasks

So once plugins are installed/enabled, your dashboards and templates work immediately.

## Template Folder Configuration

- Set Templates folder to: `02_Templates`
- Store all lesson notes in: `05_Lessons`
- Daily notes folder: `06_Daily`
- Pin:
  - [[Master Dashboard]]
  - [[Core Lesson Template]]
  - [[Master Shubuhat Log]]
  - [[Conflict Register]]
  - [[00 Subjects Hub]]

## Naming Standards

- Lesson note: `SUBJECT - LXX - Short Title`
  - Example: `Aqidah - L03 - Tawhid al-Uluhiyyah`
- Weekly review note: `Weekly Review - YYYY-MM-DD`
- Keep SH refs as `SH-001`, `SH-002`, ...
- Keep CR refs as `CR-001`, `CR-002`, ...

## Lesson Creation Rule

- Always duplicate [[Core Lesson Template]] into `05_Lessons/`.
- Keep `type: lesson` in frontmatter.
- Fill `subject`, `level`, `lesson_no`, `fahm`, `status`, and `next_review` before closing the note.

## Templater Folder Rules (Already Set)

- Any new note in `05_Lessons` -> use `Core Lesson Template`.
- Any new note in `06_Daily` -> use `Daily Study Session Template`.

## Metadata Requirements for Lesson Notes

Every lesson note should have:

- `type: lesson`
- `subject: aqidah|fiqh|tafsir|hadith|adab`
- `level: madkhal|beginner|intermediate|advanced`
- `lesson_no: <number>`
- `fahm: 1..4`
- `status: active|needs-restudy|ready-to-advance|complete`
- `next_review: YYYY-MM-DD`

If these are missing, dashboard automation will be incomplete.

See full schema: [[Lesson Metadata Schema]]

## Friday Operations Checklist

1. Run [[Weekly Review Protocol]].
2. Update lesson statuses and next review dates.
3. Resolve/assign SH and CR items.
4. Update [[Master Dashboard]] priority rows.
5. Define one process correction for next week.

