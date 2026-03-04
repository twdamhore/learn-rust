# Changelog - Lesson 094: Benchmarking Part A: Criterion and Measurement

## Section 18: Testing & Quality

### v1 - Created from task-094 split (2026-03-03)
- Split from original task-094 which was assessed as >2 hr due to too many distinct tools/topics
- Part A covers criterion benchmarks, comparing algorithms, debug vs release comparison, and compiler flags (LTO, codegen-units, opt-level)
- Exercises: criterion benchmark comparing O(n^2) vs O(n) duplicate detection, debug vs release comparison table with compiler settings
- **Estimated time**: ~1-1.5 hr
- **Pacing verdict**: OK - under 2hr threshold
- **Split needed**: N/A (this IS the split result)
- **Key issues**: None -- Exercise 2 builds on Exercise 1 for natural flow; compiler flags investigation is scoped to a single table
- **Action taken**: Created task-094.md with 4 objectives and 2 exercises from the original task-094

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~70-80 min (Moderate-Heavy)
- **Needs split**: No
- **Issues**: Exercise 2 (compiler settings table) could expand unboundedly. Specify exactly which settings to test.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~70-80 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Minor: Exercise 2 (compiler settings table) could expand unboundedly. Should specify exactly which 3-4 settings to test.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Correct (split from 084)
- **Time estimate**: 70-80 minutes (Moderate-Heavy)
- **Needs splitting**: No
- **Pacing context**: Criterion benchmarking well-scoped after split. Builds naturally on testing section.
- **Unresolved from prior reviews**: None
- **New findings**: Minor: Exercise 2 should specify exactly which 3-4 compiler settings to test (e.g., opt-level, LTO, codegen-units, target-cpu) to prevent unbounded investigation
- **Recommendation**: Scope Exercise 2 compiler settings list before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 70-90min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Criterion benchmarking well-scoped after split
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 2 should explicitly list exact settings to test (opt-level=3, lto=true, codegen-units=1).
- **Recommendation**: Scope Exercise 2 to explicit settings list before teaching

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good
- **Issues**: Ex 2 should explicitly list 3-4 compiler settings to test
- **Recommendations**: Scope Ex 2 to: opt-level=3, lto=true, codegen-units=1, target-cpu=native
- **Changes made**: Changelog updated only

### v13-fix - Applied pending fixes (2026-03-04)
- Added explicit compiler settings list (opt-level, lto, codegen-units, target-cpu) with TOML example to Exercise 2
- **Why**: Learners need exact settings to test rather than vague references
- **Resolves**: v11/v12 recommendation (high priority)

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-80min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 65-80min
- **Pacing**: Moderate
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 65-80min. **Pacing**: Moderate. **Issues**: None — compiler settings verified. **Changes**: Changelog only.
