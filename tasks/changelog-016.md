# Changelog - Lesson 016: Thinking in ownership - refactoring patterns, borrow checker battles

## Section 3: Ownership System

### v1 - Initial creation
- Lesson added to curriculum
- **NEW**: Bridging lesson added after gap analysis

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and bridging lesson tag all align with curriculum
- Correctly tagged as [NEW - bridging lesson] matching CLAUDE.md [NEW] designation
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Common ownership patterns (constructors/borrowing/mutation/consumption), clone elimination strategy, borrow checker battle strategy, ownership-first design mindset vs Java/Go
- **Exercises added**: Refactor 5 ownership-broken snippets, build a Student Registry with proper borrow/own decisions, progressive clone elimination on a working program, ownership puzzle combining slices and references

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Overloaded for 1-hour lesson
- **Issues found**:
  - **CRITICAL**: Uses `Option<T>` (lesson 22), `impl` blocks (lesson 20), and iterator methods not yet taught
  - Student Registry exercise requires 2 structs + 4 methods including `Option<&Student>` -- far too advanced for this point
  - Exercise 3 (eliminate 6+ clones) is a multi-hour task, not a single exercise
  - **Likely cannot be completed in 1 hour**
- **Recommendations**:
  - Move Student Registry to after lesson 020 or simplify to standalone functions only
  - Reduce clone elimination from 6+ to 3-4 clones
  - Scale back all exercises to use only concepts from lessons 001-015

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: OVERLOADED (~3-4 hr) for 1-2 hour target
- **Changes noted**: Most problematic task in 001-020. Uses Option<T> (lesson 22), impl blocks (lesson 20), iterator methods not yet taught. Student Registry (2 structs + 4 methods + Option<&Student>) is a 1-hour task alone. "Eliminate 6+ clones" is multi-hour. Combined volume is 3-4 hours.
- **Why**: Bridging lesson intent is good but exercises massively exceed available knowledge and time.
- **v4 recommendations status**: Not yet applied -- v4 gave the most extensive recommendations of any task (move Student Registry, reduce clones, scale back to lesson 001-015 concepts). Gradual progression: CRITICAL -- must be rescoped before use.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~3-4 hr
- **Pacing verdict**: OVERLOADED - must split
- **Split needed**: Yes - split into 016a (Part A: ownership patterns and strategies, ~1.5 hr) and 016b (Part B: building with ownership, ~1.5 hr)
- **Key issues**:
  - Student Registry exercise alone is ~1 hr
  - Uses Option (lesson 22), impl blocks (lesson 20), iterators not yet taught
  - "Eliminate 6+ clones" is a multi-hour task
  - Combined volume is 3-4 hours, far exceeding 1-2 hr target
- **Action taken**: Task split into task-016a.md and task-016b.md; changelog-016a.md and changelog-016b.md created

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Already split into 016a/016b
- **Status**: No changes needed
- Original file retained as reference

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Status**: Original lesson correctly split into 016a/016b at v6. Original was ~3-4 hours.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~3-4 hrs
- **Pacing**: OVERLOADED
- **Needs split**: Already split into 016a/016b
- **Issues**: None. Retained as reference only.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 016a/016b (split at v6)
- **Time estimate**: 3-4 hours (original, OVERLOADED)
- **Needs splitting**: Already split into 016a and 016b
- **Pacing context**: Original was correctly identified as critically overloaded and split. Original task-016.md should be marked as superseded.
- **Unresolved from prior reviews**: None (issues addressed by the split)
- **New findings**: None beyond prior reviews
- **Recommendation**: Mark original task-016.md as superseded; refer to 016a/016b for active content

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: N/A (SUPERSEDED by 016a/016b)
- **Needs split**: Already split at v6. Split was the correct decision.
- **Progression**: N/A
- **Changelog reconciliation**: All prior findings consistent — no stale flags
- **Genuinely unresolved**: None (issues addressed by the split)
- **Recommendation**: No changes needed. Refer to 016a/016b for active content.

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: N/A
- **Issues**: SUPERSEDED by 016a/016b. No changes to parent.
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 016a/016b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Status**: Correctly superseded by 016a/016b
- **Changes made**: Changelog updated only
