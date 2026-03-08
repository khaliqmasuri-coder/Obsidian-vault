# Islamic Science Framework v5 (Obsidian Vault)

This repository contains an Obsidian-ready implementation of the **Islamic Science Master Learning Framework (v5.0)**.

It is structured as a practical vault system, not a raw PDF dump, so you can immediately:

- run daily study sessions,
- take lessons with consistent templates,
- track mastery and review cycles,
- manage doubts/conflicts/mistakes,
- and build long-term retention using spaced repetition.

## Vault Structure

- `00_Hub/Islamic Science Framework Hub.md`
  - Main index (start here)
- `01_Dashboards/`
  - `Master Dashboard.md`
  - `Master Shubuhat Log.md`
  - `Conflict Register.md`
  - `Khata Log.md`
- `02_Templates/`
  - `Pre-Lesson Protocol.md`
  - `Core Lesson Template.md`
  - `Daily Study Session Template.md`
  - `Subject Modules.md`
  - `Sanad Registry.md`
  - `Arabic Technical Vocabulary Builder.md`
  - `Khilaf and Tahqiq Template.md`
  - `Weekly Review Protocol.md`
- `04_Subjects/`
  - `00 Subjects Hub.md`
  - `Aqidah Index.md`
  - `Fiqh Index.md`
  - `Tafsir Index.md`
  - `Hadith Index.md`
  - `Adab Index.md`
- `03_Reference/`
  - `Color System.md`
  - `Recommended Texts Pathway.md`
  - `Study Engine and Anki System.md`
  - `Level Gates and 90-Day Challenge.md`
  - `Hybrid Paper-Digital Workflow.md`
  - `Obsidian Setup and Automation.md`
  - `Lesson Metadata Schema.md`
  - `Execution SOP.md`
- `05_Lessons/`
  - `README.md` (store all lesson notes here)
- `06_Daily/`
  - `README.md` (daily execution notes)
- `.obsidian/`
  - preconfigured core + community plugin settings

## How To Use In Obsidian

1. Open this repository folder as a vault in Obsidian.
2. Start with `[[Islamic Science Framework Hub]]`.
3. Pin `[[Master Dashboard]]` and `[[Core Lesson Template]]`.
4. For each lesson:
   - Run `[[Pre-Lesson Protocol]]`
   - Duplicate `[[Core Lesson Template]]` into `05_Lessons/`
   - Append the relevant section from `[[Subject Modules]]`
5. Run `[[Daily Study Session Template]]` for daily 20-minute execution.
6. Log unresolved doubts in `[[Master Shubuhat Log]]` and apparent conflicts in `[[Conflict Register]]`.
7. Run `[[Weekly Review Protocol]]` every Friday.
8. Use `[[Obsidian Setup and Automation]]` for plugin/config best results.

## Community Plugin Install Links

- [Dataview](obsidian://show-plugin?id=dataview)
- [Templater](obsidian://show-plugin?id=templater-obsidian)
- [Calendar](obsidian://show-plugin?id=calendar)
- [Tasks](obsidian://show-plugin?id=obsidian-tasks-plugin)

This vault already includes `.obsidian` settings for these plugins.

## Naming Convention (Recommended)

- Lesson notes: `SUBJECT - LXX - Short Title`
  - Example: `Aqidah - L03 - Tawhid al-Uluhiyyah`
- Weekly reviews: `Weekly Review - YYYY-MM-DD`
- Shubuhat refs: `SH-001`, `SH-002`, ...
- Conflict refs: `CR-001`, `CR-002`, ...

## Note

This vault version preserves the framework's intent while formatting it for fast use inside Obsidian (wiki links, checklists, reusable templates, and dashboard-oriented workflows).

## Advanced Mode

If you enable Dataview, the dashboard and subject indexes auto-populate from lesson note metadata (`type`, `subject`, `lesson_no`, `fahm`, `next_review`, `status`).