# Changelog - Lesson 067: Advanced async - Pin/Unpin in depth, writing a mini executor, cancellation

## Section 14: Async Rust

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Pin<T> guarantees, Unpin marker trait, self-referential futures and pinning, async cancellation and drop, minimal executor loop walkthrough
- **Exercises added**: Hand-implement a Countdown Future, cancellation observation with Drop guard, manual poll loop with no-op waker, Pin/Unpin exploration with compile-error demonstration

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Pin/Unpin is one of the most conceptually difficult topics in Rust
  - Hand-implementing Future + manual poll loop + cancellation is very ambitious
  - **Hardest lesson in the async section**
- **Recommendations**:
  - Keep Future implementation and cancellation as core exercises
  - Make the manual poll loop or Pin/Unpin exploration a stretch goal

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: VERY HEAVY (~2-3 hr) for 1-2 hour target
- **Changes noted**: Likely hardest single lesson in entire curriculum. Pin/Unpin is notoriously most difficult Rust concept. Combines: hand-implementing Future + building manual poll loop + understanding cancellation + Pin/Unpin -- 4 major topics. For learner with no C/C++ background, this is unrealistic in any timeframe under 2 hours
- **Why**: Too much for one lesson; Pin/Unpin + Future impl + manual executor + cancellation = 4 distinct hard topics
- **v4 recommendations status**: Not yet applied -- v4 recommended making poll loop or Pin/Unpin a stretch goal. Gradual progression: CRITICAL -- hardest lesson in async section; consider splitting

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~2-3 hours
- **Pacing verdict**: OVERLOADED - split required
- **Split needed**: Yes - split into 067a/067b
- **Key issues**:
  - Likely hardest single lesson in entire curriculum
  - Combines Future trait impl, manual poll loop, Pin/Unpin, and cancellation
  - Four major hard topics for someone with no C/C++ background
- **Action taken**: Split into two lessons:
  - **067a**: "Advanced Async - Part A: The Future Trait and Cancellation" -- Future trait, hand-implementing futures, cancellation/drop semantics
  - **067b**: "Advanced Async - Part B: Pin, Unpin, and Executor Internals" -- Pin/Unpin, self-referential futures, mini executor. Pin content from lesson 057 consolidated here where it has proper async context
  - Original task-067.md preserved as-is for reference; new task-067a.md and task-067b.md created

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: N/A (already split in v6)
- **Status**: No changes needed
- The v6 split into 067a/067b was already the right call -- no additional changes needed under relaxed threshold

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 067a/067b at v6. Original was ~2.5-3 hrs (hardest single lesson in curriculum).
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~150-180 min
- **Pacing**: OVERLOADED
- **Needs split**: Yes (already split into 067a/067b)
- **Issues**: Hardest single lesson in entire curriculum. Future trait + cancellation vs Pin/Unpin + executor was right division.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 067a/067b
- **Time estimate**: 150-180 minutes (original, before split)
- **Needs splitting**: Already split correctly at v6. Hardest single lesson in entire curriculum.
- **Pacing context**: Combined Future trait impl, manual poll loop, Pin/Unpin, and cancellation -- four major hard topics for non-C/C++ learner.
- **Unresolved from prior reviews**: None (issues tracked in 067a/067b changelogs)
- **New findings**: None
- **Recommendation**: No action on this file; see changelog-067a.md and changelog-067b.md

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: N/A (SUPERSEDED)
- **Needs split**: N/A
- **Progression**: SUPERSEDED by 067a/067b. Split at v6 was correct. Hardest single lesson in curriculum before split.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None (tracked in 067a/067b)
- **Recommendation**: No action on this file; see changelog-067a.md and changelog-067b.md

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 067a/067b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 067a/067b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded by 067a/067b. **Changes**: Changelog only.
