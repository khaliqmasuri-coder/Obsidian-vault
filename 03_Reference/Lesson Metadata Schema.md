---
title: Lesson Metadata Schema
type: reference
tags:
  - metadata
  - schema
  - dashboard
---

# Lesson Metadata Schema

Use this frontmatter in every lesson note for full dashboard compatibility.

```yaml
---
title:
type: lesson
subject: aqidah        # aqidah|fiqh|tafsir|hadith|adab
level: madkhal         # madkhal|beginner|intermediate|advanced
lesson_no: 1
teacher:
text:
study_date: 2026-03-08
mode: first-study      # first-study|rapid-review|deep-dive
fahm: 1                # 1..4
status: active         # active|needs-restudy|ready-to-advance|complete
next_review: 2026-03-09
review_d1: 2026-03-08
review_d3: 2026-03-10
review_d7: 2026-03-14
review_d14: 2026-03-21
review_d30: 2026-04-07
shubuhat_refs: []
conflict_refs: []
anki_cards_created: 0
hasb_al_nafs_done: false
---
```

## Operational Rules

- Update `fahm` after every review.
- Update `next_review` immediately after each completed gate.
- If `fahm < 3`, set `status: needs-restudy`.
- Only set `status: ready-to-advance` once all gates are passed.

