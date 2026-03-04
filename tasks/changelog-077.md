# Changelog - Lesson 077: Associated types, GATs (generic associated types)

## Section 17: Advanced Type System

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Associated types vs type parameters, the "one impl per type" rule, GATs for lending iterators and async traits, recognizing when GATs are needed
- **Exercises added**: Graph trait with associated types, refactor generic to associated, lending iterator with GATs, Iterator-like Summarizable trait

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Jump from associated types to GATs and lending iterators is steep
  - Lending iterator exercise (WindowsMut with overlapping mutable slices) is very advanced
- **Recommendations**:
  - Add more scaffolding for the lending iterator or provide a partial implementation

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Gap between associated types (basic) and lending iterators with GATs (very advanced) is too large. Exercise 3 (WindowsMut lending iterator) requires understanding GAT lifetime semantics and where Self: 'a bounds.
- **Why**: Jump from basic to very advanced within one lesson.
- **v4 recommendations status**: Not yet applied -- v4 recommended scaffolding for Exercise 3. Gradual progression: Heavy; steep difficulty curve within lesson.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Gap between basic associated types (accessible) and lending iterator with GATs (very advanced) is too large within one lesson
  - GAT lifetime semantics (where Self: 'a) not covered prior
- **Action taken**: No split required. Previous v4 recommendation to add scaffolding or partial implementation for lending iterator exercise should be applied when lesson is started

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed under relaxed threshold
- Lending iterator with GATs is challenging but within the 2hr limit -- scaffolding recommended when lesson is started

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-110 min (Heavy)
- **Needs split**: No
- **Issues**: Exercise 3 (WindowsMut lending iterator with GATs) is a sharp difficulty spike. Provide full trait definition as scaffolding. Consider simpler first GAT example before mutable windows (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-110 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 3 (lending iterator with GATs, WindowsMut with 'where Self: 'a') is extremely advanced. Needs simpler introductory GAT example first. Full LendingIterator trait definition should be provided as scaffolding. Within-lesson difficulty cliff between Exercise 1-2 (accessible) and Exercise 3 (extremely advanced). Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match with CLAUDE.md
- **Time estimate**: 80-110 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Heavy; internal difficulty cliff between Exercises 1-2 (accessible) and Exercise 3 (extremely advanced)
- **Unresolved from prior reviews**: Exercise 3 (lending iterator with GATs) needs full LendingIterator trait definition as scaffolding. Internal difficulty cliff. Consider reordering Exercise 4 before Exercise 3 to ease progression. Flagged since v4, still unresolved.
- **New findings**: None
- **Recommendation**: Provide LendingIterator trait definition scaffold and reorder Ex4 before Ex3 before teaching

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy)
- **Needs split**: No
- **Progression**: Internal difficulty cliff between Exercises 1-2 and Exercise 3
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: (1) Reorder exercises: 1->2->4->3 (easier before harder), (2) Provide LendingIterator trait definition as scaffold for Exercise 3, (3) Add simpler GAT "hello" example before WindowsMut.
- **Recommendation**: Reorder exercises 1->2->4->3, provide LendingIterator trait scaffold, and add simpler introductory GAT example before teaching

### v11-fix - Reordered exercises and added GAT scaffold (2026-03-04)
- Swapped Exercise 3 (lending iterator) and Exercise 4 (Summarizable) so simpler comes first
- Added LendingIterator trait definition as scaffold for the GAT exercise
- Added motivating note about when GATs appear in practice
- **Why**: Difficulty cliff between Exercises 1-2 and the GAT exercise was too steep
- **Resolves**: HIGH priority item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy
- **Issues**: GAT lending iterator exercise is extremely advanced even with scaffold
- **Recommendations**: Consider marking GAT exercise (Ex 4) as [STRETCH] or providing partial implementation
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Marked Exercise 4 (Lending iterator with GATs / WindowsMut) as [STRETCH] in task file
- **Why**: The GAT lending iterator exercise is extremely advanced even with the trait scaffold; marking it [STRETCH] sets realistic expectations and avoids derailing the lesson's 1-2hr target
- **Resolves**: v12 recommendation to mark GAT exercise as [STRETCH]

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-90min core (Heavy with STRETCH)
- **Pacing**: Heavy with STRETCH
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-100min. **Pacing**: Heavy. **Issues**: None — prior fixes verified. **Changes**: Changelog only.
