# Changelog - Lesson 100: Project 3 - continued (unsafe where needed, optimization, benchmarks)

## Section 21: Capstone Projects

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Criterion benchmarks for performance-critical operations, profiling with flamegraphs to identify bottlenecks, unsafe code audit with SAFETY comments, comprehensive documentation with crate/module/API docs, retrospective on the 100-lesson journey
- **Exercises added**: Criterion benchmarks at multiple input sizes with std lib comparison, flamegraph profiling with targeted optimization, unsafe block review with SAFETY comments and Miri testing, lessons-learned retrospective on Rust vs Java/Go

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate-to-Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 3 (Miri) requires nightly Rust -- should be noted
  - If learner chose Option B (parser) in lesson 099, Exercise 3 (unsafe audit) has limited applicability
  - Exercise 4 (retrospective) is non-coding reflection
  - Exercise format uses unnumbered bullets (formatting inconsistency)
- **Recommendations**:
  - Note nightly Rust requirement for Miri
  - Provide alternative for Exercise 3 when no unsafe code exists
  - Standardize exercise format

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate-to-Heavy (~1-1.5 hr, if 099 completed) for 1-2 hour target
- **Changes noted**: Exercise 3 (Miri) requires nightly Rust -- not stated. If learner chose Option B (parser) in 099, Exercise 3 (unsafe audit) has limited applicability. Exercise 4 (retrospective) is valuable non-coding reflection. Depends on 099 completion. Exercise format inconsistency.
- **Why**: Nightly requirement unstated; option-dependent relevance.
- **v4 recommendations status**: Not yet applied -- v4 noted nightly requirement and limited unsafe applicability for parser option. Gradual progression: Conclusion lesson; quality depends on 099.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1-1.5 hours (if lesson 099 completed)
- **Pacing verdict**: Moderate-Heavy - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Miri requires nightly Rust (not stated in task)
  - Unsafe audit has limited relevance if parser option chosen in lesson 099
- **Action taken**: No split needed. With lesson 099 split into 099a/099b, the predecessor is more achievable, improving this lesson's viability. Nightly requirement for Miri and option-dependent relevance should be noted in task content updates.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: OVERLOADED (~2+ hr)
- **Status**: Changes noted below
- **SPLIT into 100a and 100b**: 100a covers benchmarking and optimization. 100b covers polish and retrospective.

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 100a/100b at v7. Original was ~120+ min.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~120+ min
- **Pacing**: OVERLOADED
- **Needs split**: Already split into 100a/100b
- **Issues**: Benchmarking, profiling, unsafe auditing, documentation each time-consuming.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 100a/100b
- **Time estimate**: 120+ minutes (Overloaded -- original)
- **Needs splitting**: Already split into 100a/100b at v7
- **Pacing context**: Original 2+ hours combining benchmarking, profiling, unsafe audit, documentation, and retrospective. Correctly split.
- **Unresolved from prior reviews**: None (issues resolved by split)
- **New findings**: None
- **Recommendation**: No action needed on original; see 100a and 100b changelogs

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: N/A (SUPERSEDED)
- **Needs split**: N/A
- **Progression**: SUPERSEDED by 100a/100b. Split was correct.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No action needed on original; see 100a and 100b changelogs

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 100a/100b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 100a/100b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
