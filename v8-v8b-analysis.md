# Islamic Science Framework — v8 vs v8b Complete Analysis

## Executive Summary

**v8b is dramatically more complete** and is the correct base for building v9. v8 is essentially a broken/failed export with almost entirely empty files. v8b has ~35 fully-written content files totaling ~2,500 lines of markdown, plus 9 templates, proper Obsidian configuration, and a coherent folder structure.

---

## 1. /tmp/v8/ — FILE-BY-FILE ANALYSIS

### Critical Issue: BROKEN EXPORT
v8 appears to be a failed directory creation where filenames with spaces were truncated at the first space. Nearly every file is **0 bytes**. The structure was intended to be:

```
00_Hub/Islamic Science Framework Hub.md  → truncated to: 00_Hub/Islamic (0 bytes)
01_Dashboards/Master Dashboard.md        → truncated to: 01_Dashboards/Master (0 bytes)
02_Templates/Core Lesson Template.md     → truncated to: 02_Templates/Core (0 bytes)
```

### All v8 Files

| File | Size | Analysis |
|---|---|---|
| `00_Hub/Islamic` | 0 bytes | BROKEN — truncated filename for "Islamic Science Framework Hub.md" |
| `01_Dashboards/Conflict` | 0 bytes | BROKEN — truncated "Conflict Register.md" |
| `01_Dashboards/Khata` | 0 bytes | BROKEN — truncated "Khata Log.md" |
| `01_Dashboards/Master` | 0 bytes | BROKEN — truncated "Master Dashboard.md" |
| `02_Templates/Arabic` | 0 bytes | BROKEN — truncated "Arabic Technical Vocabulary Builder.md" |
| `02_Templates/Core` | 0 bytes | BROKEN — truncated "Core Lesson Template.md" |
| `02_Templates/Daily` | 0 bytes | BROKEN — truncated "Daily Study Session Template.md" |
| `02_Templates/Khilaf` | 0 bytes | BROKEN — truncated "Khilaf and Tahqiq Template.md" |
| `02_Templates/Pre-Lesson` | 0 bytes | BROKEN — truncated "Pre-Lesson Protocol.md" |
| `02_Templates/Sanad` | 0 bytes | BROKEN — truncated "Sanad Registry.md" |
| `02_Templates/Subject` | 0 bytes | BROKEN — truncated "Subject Modules.md" |
| `02_Templates/Weekly` | 0 bytes | BROKEN — truncated "Weekly Review Protocol.md" |
| `03_Reference/Color` | 0 bytes | BROKEN — truncated "Color System.md" |
| `03_Reference/Execution` | 0 bytes | BROKEN — truncated "Execution SOP.md" |
| `03_Reference/Hybrid` | 0 bytes | BROKEN — truncated "Hybrid Paper-Digital Workflow.md" |
| `03_Reference/Lesson` | 0 bytes | BROKEN — truncated "Lesson Metadata Schema.md" |
| `03_Reference/Level` | 0 bytes | BROKEN — truncated "Level Gates and 90-Day Challenge.md" |
| `03_Reference/Obsidian` | 0 bytes | BROKEN — truncated "Obsidian Setup and Automation.md" |
| `03_Reference/Recommended` | 0 bytes | BROKEN — truncated "Recommended Texts Pathway.md" |
| `03_Reference/Study` | 0 bytes | BROKEN — truncated "Study Engine and Anki System.md" |
| `04_Subjects/00` | 0 bytes | BROKEN — truncated "00 Subjects Hub.md" |
| `04_Subjects/Adab` | 0 bytes | BROKEN — truncated "Adab Index.md" |
| `04_Subjects/Aqidah` | 0 bytes | BROKEN — truncated "Aqidah Index.md" |
| `04_Subjects/Fiqh` | 0 bytes | BROKEN — truncated "Fiqh Index.md" |
| `04_Subjects/Hadith` | 0 bytes | BROKEN — truncated "Hadith Index.md" |
| `04_Subjects/Tafsir` | 0 bytes | BROKEN — truncated "Tafsir Index.md" |
| **`05_Lessons/README.md`** | **26 lines** | **HAS CONTENT** — Lesson folder instructions with frontmatter schema example |
| **`06_Daily/README.md`** | **8 lines** | **HAS CONTENT** — Daily notes folder instructions |
| `90-Day` | 0 bytes | BROKEN — truncated root-level fragment |
| `and` | 0 bytes | BROKEN — truncated fragment |
| `Anki` | 0 bytes | BROKEN — truncated fragment |
| `Automation.md` | 0 bytes | Empty file |
| `Builder.md` | 0 bytes | Empty file |
| `Challenge.md` | 0 bytes | Empty file |
| `Dashboard.md` | 0 bytes | Empty file |
| `Engine` | 0 bytes | BROKEN — truncated fragment |
| `Framework` | 0 bytes | BROKEN — truncated fragment |
| `Gates` | 0 bytes | BROKEN — truncated fragment |
| `Hub.md` | 0 bytes | Empty file |
| `Index.md` | 0 bytes | Empty file |
| `Lesson` | 0 bytes | BROKEN — truncated fragment |
| `Log.md` | 0 bytes | Empty file |
| `Metadata` | 0 bytes | BROKEN — truncated fragment |
| `Modules.md` | 0 bytes | Empty file |
| `Paper-Digital` | 0 bytes | BROKEN — truncated fragment |
| `Pathway.md` | 0 bytes | Empty file |
| `Protocol.md` | 0 bytes | Empty file |
| **`README.md`** | **90 lines** | **HAS CONTENT** — References "v5" framework. Describes intended vault structure. |
| `Register.md` | 0 bytes | Empty file |
| `Registry.md` | 0 bytes | Empty file |
| `Review` | 0 bytes | BROKEN — truncated fragment |
| `Schema.md` | 0 bytes | Empty file |
| `Science` | 0 bytes | BROKEN — truncated fragment |
| `Session` | 0 bytes | BROKEN — truncated fragment |
| `Setup` | 0 bytes | BROKEN — truncated fragment |
| `Shubuhat` | 0 bytes | BROKEN — truncated fragment |
| `SOP.md` | 0 bytes | Empty file |
| `Study` | 0 bytes | BROKEN — truncated fragment |
| `Subjects` | 0 bytes | BROKEN — truncated fragment |
| `System.md` | 0 bytes | Empty file |
| `Tahqiq` | 0 bytes | BROKEN — truncated fragment |
| `Technical` | 0 bytes | BROKEN — truncated fragment |
| `Template.md` | 0 bytes | Empty file |
| `Texts` | 0 bytes | BROKEN — truncated fragment |
| `Vocabulary` | 0 bytes | BROKEN — truncated fragment |
| `Workflow.md` | 0 bytes | Empty file |

### v8 .obsidian/ Config (VALID — these work)
- `app.json` — Wiki links, relative paths, line numbers enabled
- `community-plugins.json` — dataview, templater, calendar, tasks
- `core-plugins.json` — 16 core plugins enabled
- `daily-notes.json` — Points to `06_Daily/` with template from `02_Templates/`
- `templates.json` — Template folder: `02_Templates/`
- `plugins/calendar/data.json` — Calendar config
- `plugins/dataview/data.json` — Dataview config (inline enabled, JS disabled)
- `plugins/obsidian-tasks-plugin/data.json` — Tasks config
- `plugins/templater-obsidian/data.json` — Templater config with folder templates for `05_Lessons` and `06_Daily`

### v8 Issues Summary
1. **99% of files are empty/broken** — filename truncation at spaces
2. **Version reference:** README says "v5" not "v8"
3. **Only 3 files have content:** root README.md, 05_Lessons/README.md, 06_Daily/README.md
4. **Obsidian configs are valid** and provide useful plugin setup (Dataview, Templater, Calendar, Tasks)
5. **Templater folder templates** — good idea to auto-apply lesson template in lesson folder

### v8 Content Worth Preserving
- The `.obsidian/` plugin configurations (community plugins setup)
- The Templater folder-template mapping concept
- The frontmatter schema from `05_Lessons/README.md`:
  ```yaml
  type: lesson
  subject: aqidah
  level: madkhal
  lesson_no: 1
  study_date: 2026-03-08
  mode: first-study
  fahm: 1
  status: active
  next_review: 2026-03-09
  ```

---

## 2. /tmp/v8b/ — FILE-BY-FILE ANALYSIS

### Overview
v8b is a **substantially complete vault** with ~35 properly-written markdown files, 9 templates, and valid Obsidian configuration. It also suffers from the same filename truncation issue, creating ~60 empty 0-byte fragment files alongside the real content.

### CONTENT FILES (Non-Empty)

---

#### `00 - Home.md` (98 lines)
**Map of Content / Hub page.** Well-structured with sections for Getting Started, Dashboard, Daily Engine, Recommended Texts, Sanad & Vocabulary, Lesson Notes, Logs, Advancement, Weekly Reviews, and Templates table. Uses wiki-links with display aliases (e.g., `[[Aqidah Texts|ʿAqīdah Texts]]`). Has YAML frontmatter with `cssclass: wide-page` and `tags: [home, moc]`.

**Issues:** None — this is clean.

---

#### `01 - Framework Guide/How This Framework Works.md` (50 lines)
**Explains the 5 Laws** (Retrieval Practice, Spaced Repetition, Elaborative Interrogation, Interleaving, Feynman Gate) and provides a 9-step "How to Use This Vault" guide. Uses Obsidian callouts correctly.

**Issues:** None.

---

#### `01 - Framework Guide/Functional Color System.md` (79 lines)
**Complete color reference system** — 7 colors (🔴🟡🟢🔵🟠🟣⚫), each with meaning, "use for," and "never for." Includes quick reference table. Uses Obsidian callout types correctly (danger, warning, tip, info, caution, abstract, quote).

**Issues:** None.

---

#### `01 - Framework Guide/Brain-Download Protocols.md` (69 lines)
**Three retention protocols:** Feynman Method (4 steps), Teach-Back Protocol (3 options), Concept Map technique. Well-structured with tables and callouts.

**Issues:** None.

---

#### `01 - Framework Guide/Hybrid Physical + Digital Guide.md` (60 lines)
**Paper vs. digital guide** — what goes where and why. Includes sync protocol checklist (paper → digital transfer within 24 hours). Backup protocol callout.

**Issues:** None.

---

#### `02 - Dashboard/Master Learning Dashboard.md` (62 lines)
**Central tracking page** with Subject Progress table (5 subjects, columns for text/lesson/fahm/date), This Week's Priority Lessons, Open Issues, and Quick Links. Empty template rows ready for user input.

**Issues:** None — clean template.

---

#### `02 - Dashboard/Weekly Priority Lessons.md` (50 lines)
**Weekly planning tracker** with 5 priority slots, Mode Key (🟢 First Study / 🟡 Rapid Review / ⚫ Deep Dive), and Previous Weeks Archive (collapsible).

**Issues:** None.

---

#### `02 - Dashboard/Open Issues.md` (42 lines)
**Issue tracker** for Shubhāt/Conflicts/Gaps with resolution workflow (6 steps) and archive section.

**Issues:** None.

---

#### `02 - Dashboard/90-Day Mastery Challenge.md` (143 lines)
**Habit tracker** — 90 daily checkboxes organized in week ranges, plus 8 milestone gates with behavioral targets.

**Issues:** None.

---

#### `03 - Daily Engine/Daily Study Engine.md` (51 lines)
**Daily 20-minute routine** (4 time blocks), Weekly Architecture (7-day schedule assigning subjects to days), Murājaʿah schedule (Day 1/3/7/14/30).

**Issues:** None.

---

#### `03 - Daily Engine/Anki Card System.md` (86 lines)
**5-tier card system** (Speed Spine, Dalīl→Ruling, Masʾalah→Masāʾil, Error Detection, Feynman Card), card creation rules (5 rules), and card tracking table.

**Issues:** None.

---

#### `04 - Recommended Texts/Aqidah Texts.md` (40 lines)
**ʿAqīdah text pathway** — 4 levels (Madkhal→Advanced) with specific recommended texts per level. Includes aliases in YAML. Links to vocabulary and lesson folder.

**Issues:** None.

---

#### `04 - Recommended Texts/Fiqh Texts.md` (39 lines)
**Fiqh text pathway** — same structure. Missing `aliases` in YAML (unlike Aqidah/Tafsir/Hadith/Adab).

**Issues:** Missing YAML alias.

---

#### `04 - Recommended Texts/Tafsir Texts.md` (40 lines)
**Tafsīr text pathway** — same structure with aliases.

**Issues:** None.

---

#### `04 - Recommended Texts/Hadith Texts.md` (40 lines)
**Ḥadīth text pathway** — same structure with aliases.

**Issues:** None.

---

#### `04 - Recommended Texts/Adab Texts.md` (40 lines)
**Ādāb text pathway** — same structure with aliases.

**Issues:** None.

---

#### `05 - Sanad Registry/Sanad al-Ilm Registry.md` (80 lines)
**Chain of knowledge records** — 5 subject sections, each with fields for teacher, their teacher, text, method, start date, notes. Includes the Ibn Sīrīn quote. Has YAML aliases.

**Issues:** None.

---

#### `06 - Vocabulary/Aqidah Vocabulary.md` (41 lines)
**10 core ʿAqīdah terms** (Tawḥīd, Rubūbiyyah, Ulūhiyyah, etc.) with Arabic, transliteration, definition, example, lesson ref, and mastery checkbox. Plus 5 blank "Additional Terms" rows.

**Issues:** None.

---

#### `06 - Vocabulary/Fiqh Vocabulary.md` (40 lines)
**10 core Fiqh terms** (Farḍ ʿAyn, Farḍ Kifāyah, Sunnah, etc.). Missing YAML alias (unlike Aqidah/Tafsir/Hadith/Adab).

**Issues:** Missing YAML alias for `Fiqh Vocabulary`.

---

#### `06 - Vocabulary/Tafsir Vocabulary.md` (41 lines)
**10 core Tafsīr terms** (Asbāb al-Nuzūl, Makkan/Madanī, Naskh, etc.). Has aliases.

**Issues:** None.

---

#### `06 - Vocabulary/Hadith Vocabulary.md` (41 lines)
**10 core Ḥadīth terms** (Isnād, Matn, Ṣaḥīḥ, etc.). Has aliases.

**Issues:** None.

---

#### `06 - Vocabulary/Adab Vocabulary.md` (41 lines)
**10 core Ādāb terms** (Maqām, Ikhlāṣ, Tawāḍuʿ, etc.). Has aliases.

**Issues:** None.

---

#### `07 - Lessons/Aqidah/Aqidah Lessons.md` (35 lines)
**Lesson index** — instructions for creating lessons (5 steps), empty 5-row lesson table with Fahm and Murājaʿah tracking. Has YAML aliases.

**Issues:** None.

---

#### `07 - Lessons/Fiqh/Fiqh Lessons.md` (34 lines)
**Lesson index** — same structure. Missing YAML alias.

**Issues:** Missing YAML alias for `Fiqh Lessons`.

---

#### `07 - Lessons/Tafsir/Tafsir Lessons.md` (35 lines)
**Lesson index** — same structure with aliases.

**Issues:** None.

---

#### `07 - Lessons/Hadith/Hadith Lessons.md` (35 lines)
**Lesson index** — same structure with aliases.

**Issues:** None.

---

#### `07 - Lessons/Adab/Adab Lessons.md` (35 lines)
**Lesson index** — same structure with aliases.

**Issues:** None.

---

#### `08 - Logs/Conflict Register.md` (40 lines)
**Conflict tracking** — 3 conflict types explained, 8 empty entry rows, 4 resolution methods (Jamʿ, Tarjīḥ, Naskh, Tawaqquf).

**Issues:** None.

---

#### `08 - Logs/Khata Log.md` (54 lines)
**Mistake log** with root cause analysis (M/A/C/D/T system), 12 empty rows, monthly pattern analysis section. Has aliases.

**Issues:** None.

---

#### `08 - Logs/Master Shubhat Log.md` (82 lines)
**Shubhāt (doubt) tracker** — organized by subject (5 sections), 5 entries per subject. Includes usage instructions. Has aliases.

**Issues:** SH-XXX refs repeat within each subject (SH-001 used in all 5 subjects = ambiguous). Should use subject-prefixed codes (e.g., AQ-SH-001, FQ-SH-001).

---

#### `09 - Level Gates/Level Transition Gates.md` (64 lines)
**3 gate levels** (Madkhal→Beginner: 10 checkboxes, Beginner→Intermediate: 10 checkboxes, Intermediate→Advanced: 9 checkboxes). Each with behavioral performance tests.

**Issues:** No Advanced→ completion gate defined (perhaps intentional — advanced is open-ended).

---

#### `10 - Weekly Reviews/Weekly Reviews.md` (27 lines)
**Review index** — instructions for creating weekly reviews, empty archive list. Short and functional.

**Issues:** None.

---

### TEMPLATE FILES

---

#### `Templates/Template - New Lesson.md` (240 lines) ⭐ KEY FILE
**The master template** — combines Pre-Lesson Protocol + Core Lesson Template in one file. Sections:
1. Pre-Lesson Protocol (Niyyah, Mode Selector, Muqaddimāt)
2. Core Lesson Template (Header, Ustādh Signals, Tasawwur, Masāʾil, Speed Spine, Dalīl, Taṭbīq [4 scenarios], Fahm Spectrum, Athar al-Qalb, Shubhāt flag, Conflict flag, Rawābiṭ, Murājaʿah schedule, Ḥasb al-Nafs)

**Issues:**
- YAML frontmatter uses `{{subject}}` and `{{level}}` Templater variables but no Templater-specific syntax (`<% %>`)
- The `{{date}}` in lesson header is a Templater variable — needs Templater plugin installed
- Tags include `lesson` — correct for generated lessons, but THIS is a template file. When used via Obsidian's core template system (not Templater), the tags get inserted literally including `{{subject}}`

---

#### `Templates/Template - Aqidah Module.md` (39 lines)
**ʿAqīdah subject extension** — Tawḥīd coordinate (5 categories), Deviation Map (6 sect rows), cross-links.

**Issues:** None.

---

#### `Templates/Template - Fiqh Module.md` (45 lines)
**Fiqh subject extension** — Fiqh coordinates, 4-Madhhab comparison table + rājiḥ row, ʿAmal implementation section.

**Issues:** None.

---

#### `Templates/Template - Tafsir Module.md` (53 lines)
**Tafsīr subject extension** — Āyah capture, Asbāb al-Nuzūl, Munāsabah, Wujūh al-Tafsīr (4 approaches).

**Issues:** None.

---

#### `Templates/Template - Hadith Module.md` (45 lines)
**Ḥadīth subject extension** — Ḥadīth text capture, Isnād analysis (4 fields), Furūʿ min al-Ḥadīth (4 domains).

**Issues:** None.

---

#### `Templates/Template - Adab Module.md` (51 lines)
**Ādāb subject extension** — Maqām identification, ʿAlāmāt al-Ḥuṣūl (5 behavioral signs table), Al-Bāqī (deficiency tracking).

**Issues:** None.

---

#### `Templates/Template - Intermediate Additions.md` (72 lines)
**Khilāf analysis framework** — Maḥall al-Khilāf, 3 positions map, Tarjīḥ section, Uṣūlī extraction.

**Issues:** None.

---

#### `Templates/Template - Advanced Additions.md` (91 lines)
**Taḥqīq architecture** — Taḥrīr al-Nizāʿ, Steelmanning, 3 Muʿāraḍāt (objections), Naẓar fī al-Adillah, Qawāʿid al-Tarjīḥ, Taḥqīq al-Rājiḥ, Dhakhīrah.

**Issues:** None.

---

#### `Templates/Template - Weekly Review.md` (62 lines)
**Friday review template** — Lessons covered table, Red Flags (5 areas), Spiritual Check (4 checkboxes), Next Week planning.

**Issues:** Uses `{{date}}` Templater variable.

---

### BROKEN/EMPTY FILES IN v8b (filename truncation artifacts)

All 0 bytes — these are fragments of filenames where spaces caused truncation:

**Root-level fragments:**
`+`, `-`, `00`, `01`, `02`, `03`, `04`, `05`, `06`, `07`, `08`, `09`, `10`,
`Adab`, `Additions.md`, `Advanced`, `al-Ilm`, `Aqidah`, `Card`, `Challenge.md`,
`Color`, `Daily`, `Digital`, `Fiqh`, `Framework`, `Hadith`, `Home.md` (empty duplicate),
`Intermediate`, `Issues.md`, `Learning`, `Lesson.md`, `Lessons.md`, `Level`,
`Log.md`, `Mastery`, `Module.md`, `New`, `Physical`, `Priority`, `Protocols.md`,
`Recommended`, `Register.md`, `Registry.md`, `Review.md`, `Reviews.md`, `Sanad`,
`Shubhat`, `Study`, `System.md`, `Tafsir`, `Texts.md`, `This`, `Transition`,
`Vocabulary.md`, `Weekly`, `Works.md`

**Duplicate subfolder fragments:**
`Dashboard/90-Day`, `Dashboard/Master`, `Dashboard/Open`, `Dashboard/Weekly`,
`Engine/Anki`, `Engine/Daily`,
`Gates/Level`, `Gates.md`,
`Guide/Brain-Download`, `Guide/Functional`, `Guide/How`, `Guide/Hybrid`, `Guide.md`,
`Lessons/Adab/Adab`, `Lessons/Aqidah/Aqidah`, `Lessons/Fiqh/Fiqh`, `Lessons/Hadith/Hadith`, `Lessons/Tafsir/Tafsir`,
`Logs/Conflict`, `Logs/Khata`, `Logs/Master`,
`Registry/Sanad`,
`Reviews/Weekly`,
`Templates/Template`,
`Texts/Adab`, `Texts/Aqidah`, `Texts/Fiqh`, `Texts/Hadith`, `Texts/Tafsir`,
`Vocabulary/Adab`, `Vocabulary/Aqidah`, `Vocabulary/Fiqh`, `Vocabulary/Hadith`, `Vocabulary/Tafsir`

### v8b .obsidian/ Config
- `app.json` — New files go to `07 - Lessons`, attachments to `Attachments`, live preview enabled
- `core-plugins.json` — 18 core plugins (includes word-count and file-recovery, no community plugins listed)
- `core-plugins-migration.json` — All 18 plugins set to true
- `templates.json` — Template folder: `Templates`, date format: `DD/MM/YYYY`
- `appearance.json` — Accent color #1a7335 (Islamic green), font sizes 16/14
- `hotkeys.json` — Empty

**Missing from v8b .obsidian:** No community-plugins.json → Dataview, Templater, Calendar, Tasks not configured. v8 had these.

---

## 3. COMPARISON — v8 vs v8b

| Dimension | v8 | v8b | Winner |
|---|---|---|---|
| **Content files with actual markdown** | 3 | 35+ | **v8b** |
| **Total content lines** | 124 | ~2,500 | **v8b** |
| **Templates** | 0 (all empty) | 9 complete | **v8b** |
| **Folder structure** | 7 folders (numbered prefix) | 11+ folders (human-readable) | **v8b** |
| **Community plugin config** | ✅ (Dataview, Templater, Calendar, Tasks) | ❌ (not configured) | **v8** |
| **Templater folder templates** | ✅ (auto-apply in 05_Lessons, 06_Daily) | ❌ | **v8** |
| **Frontmatter schema (Dataview-ready)** | ✅ (documented in 05_Lessons/README.md) | ❌ (template uses {{}} vars but no schema) | **v8** |
| **Broken/empty files** | ~60 | ~60 | Tie (both broken) |
| **Version reference** | "v5" | "v5.0" (in README & Home) | Tie |

---

## 4. GAP ANALYSIS — What v9 Needs

### From v8b (keep)
- All 35 content files — well-written, consistent, thorough
- All 9 templates — the 240-line New Lesson template is excellent
- Folder structure (but reorganize to match target)
- `.obsidian/appearance.json` theming

### From v8 (integrate)
- Community plugin configuration (Dataview, Templater, Calendar, Tasks)
- Templater folder-template auto-application
- Dataview-ready frontmatter schema
- Daily notes configuration

### Neither has (must create for v9)
1. **Proper folder structure matching target:**
   ```
   vault/
   ├── 🏠 Home.md
   ├── Dashboard/
   │   ├── Master Dashboard.md
   │   ├── Daily Study Engine.md
   │   └── Obsidian Upkeep.md      ← MISSING from both
   ├── 01 - Aqidah/
   │   ├── Aqidah Index.md
   │   ├── Sanad - Aqidah.md       ← v8b has single combined Sanad
   │   ├── Shubhat - Aqidah.md     ← v8b has single combined Shubhat Log
   │   └── Lessons/
   ├── 02 - Fiqh/                  (same pattern)
   ├── 03 - Tafsir/
   ├── 04 - Hadith/
   ├── 05 - Adab/
   ├── Templates/
   ├── Logs and Registers/
   └── Reference/
   ```

2. **Subject-specific Sanad files** (v8b has one combined registry — target wants per-subject)
3. **Subject-specific Shubhat files** (v8b has one combined log — target wants per-subject)
4. **Obsidian Upkeep page** (not in either version)
5. **Proper frontmatter on templates** using Templater `<% %>` syntax instead of `{{ }}`
6. **Dataview queries** in dashboard/index pages (v8 had Dataview configured but no queries exist)
7. **Version bumped to v9** (both currently say v5.0)
8. **Cleanup of all 0-byte truncated filename artifacts**
9. **Consistent YAML aliases** (Fiqh files missing aliases in v8b)
10. **Subject-numbered folder scheme** (target uses `01 - Aqidah/` not `07 - Lessons/Aqidah/`)

### Specific Issues to Fix in v9
- Shubhat Log SH-XXX codes are ambiguous (same codes reused per subject)
- Template uses `{{}}` variables but no Templater plugin configured in v8b
- No daily notes folder or configuration in v8b
- Missing community plugins in v8b
- Home.md references v5.0 — should be v9
- README.md references v5.0 — should be v9
- Lesson index link format `[[07 - Lessons/Aqidah/|...]]` links to folder not file — won't work in all Obsidian versions
