# Changelog - Lesson 084: Benchmarking - criterion, profiling, flamegraphs

## Section 18: Testing & Quality

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Criterion setup and statistical approach, interpreting benchmark results, flamegraph generation with cargo-flamegraph, hot spot identification, optimization levels and compiler settings impact
- **Exercises added**: Benchmark O(n^2) vs O(n) duplicate detection, flamegraph for HashMap program, iterative optimization from profiling, debug vs release comparison table

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Covers criterion, flamegraphs, profiling, AND compiler optimization settings
  - Flamegraph tooling setup can be tricky (requires perf on Linux, dtrace on macOS)
  - Exercise 4 (optimization settings table) is an entire investigation
- **Recommendations**:
  - Make Exercise 4 optional
  - Note platform-specific tooling requirements for flamegraphs

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: criterion setup + flamegraph tooling + platform-specific issues + Exercise 4 (optimization settings table). Too broad for 1 hour. Platform-specific setup not mentioned.
- **Why**: Too many distinct tools/topics
- **v4 recommendations status**: Not yet applied -- v4 recommended making Exercise 4 optional and noting platform requirements. Gradual progression: Heavy continuation.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hours
- **Pacing verdict**: Heavy - borderline under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Too many tools covered (criterion, flamegraphs, profiling, optimization settings)
  - Exercise 4 (optimization settings investigation) adds too much scope
  - Platform-specific tooling requirements for flamegraphs not mentioned (requires perf on Linux, dtrace on macOS)
- **Action taken**: No split, but Exercise 4 should be marked as optional/stretch when task content is updated. Platform-specific notes for flamegraph tooling should be added.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: OVERLOADED (~2+ hr)
- **Status**: Changes noted below
- **SPLIT into 084a and 084b**: 084a covers criterion benchmarks and measurement. 084b covers profiling with flamegraphs and optimization cycles.

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 084a/084b at v7. Original was ~120+ min.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~120+ min (original)
- **Pacing**: OVERLOADED
- **Needs split**: Yes (already split into 084a/084b). Well-executed split.
- **Issues**: None (split resolved the overload)
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 084a/084b
- **Time estimate**: 120+ minutes (original, before split)
- **Needs splitting**: Already split into 084a/084b at v7
- **Pacing context**: Original correctly identified as overloaded. Split separates criterion benchmarking from profiling/flamegraphs.
- **Unresolved from prior reviews**: None
- **New findings**: None
- **Recommendation**: No changes needed — see 084a/084b changelogs

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: SUPERSEDED by 084a/084b
- **Needs split**: No (already split)
- **Progression**: SUPERSEDED by 084a/084b. Split was correct.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None (see 084a/084b)
- **Recommendation**: No action on this file; see 084a and 084b changelogs

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 084a/084b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 084a/084b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
