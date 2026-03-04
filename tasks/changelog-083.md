# Changelog - Lesson 083: Property-based testing (proptest), fuzzing (cargo-fuzz)

## Section 18: Testing & Quality

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Property-based testing philosophy, proptest strategies and generation, meaningful property invariants, cargo-fuzz setup, shrinking and failure reproduction
- **Exercises added**: Proptest sort function properties, roundtrip encode/decode testing, custom strategies with prop_compose!, fuzzing a key-value parser

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Introduces two entirely new crate ecosystems (proptest and cargo-fuzz) in one lesson
  - Exercise 4 (cargo-fuzz) requires nightly Rust -- should be explicitly noted
  - Custom strategy exercise (Exercise 3) is particularly involved
- **Recommendations**:
  - Make Exercise 4 (fuzzing) optional
  - Note nightly Rust requirement for cargo-fuzz

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: Two entirely new tool ecosystems (proptest + cargo-fuzz). proptest learning curve is significant (strategies, shrinking, configuration). Exercise 3 (custom strategy with prop_compose!) is involved. Exercise 4 requires nightly Rust.
- **Why**: Two new crate ecosystems in one lesson is too much
- **v4 recommendations status**: Not yet applied -- v4 recommended making Exercise 4 optional and noting nightly requirement. Gradual progression: Heavy spike.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.75-2.5 hours
- **Pacing verdict**: OVERLOADED - split required
- **Split needed**: Yes - split into 083a/083b
- **Key issues**:
  - Two entirely new crate ecosystems (proptest AND cargo-fuzz) in one lesson
  - proptest alone has significant learning curve (strategies, shrinking, prop_compose!)
  - Exercise 4 (cargo-fuzz) requires nightly Rust (not stated in original)
- **Action taken**: Split into task-083a.md (Property-Based Testing with proptest) and task-083b.md (Fuzzing with cargo-fuzz). Each part is now ~1-1.5 hours. Nightly requirement explicitly noted in 083b.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Already split in v6 into 083a/083b
- **Status**: No changes needed
- Prior split was adequate under relaxed threshold; no additional changes required

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 083a/083b at v6. Original was ~105-150 min.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~105-150 min (original)
- **Pacing**: OVERLOADED
- **Needs split**: Yes (already split into 083a/083b). Two different tool ecosystems (proptest, cargo-fuzz) separated cleanly.
- **Issues**: None (split resolved the overload)
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 083a/083b
- **Time estimate**: 105-150 minutes (original, before split)
- **Needs splitting**: Already split into 083a/083b at v6
- **Pacing context**: Original correctly identified as overloaded. Split cleanly separates proptest and cargo-fuzz.
- **Unresolved from prior reviews**: None
- **New findings**: None
- **Recommendation**: No changes needed — see 083a/083b changelogs

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: SUPERSEDED by 083a/083b
- **Needs split**: No (already split)
- **Progression**: SUPERSEDED by 083a/083b. Split was correct.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None (see 083a/083b)
- **Recommendation**: No action on this file; see 083a and 083b changelogs

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 083a/083b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 083a/083b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
