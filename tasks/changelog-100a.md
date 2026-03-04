# Changelog - Lesson 100a: Project 3 Part C: Benchmarking and Optimization
## Section 21: Capstone Projects

### v1 - Created from split (2026-03-03)
- Split from original lesson 100 which was assessed as >2 hrs during v7 pacing review
- **Reason for split**: Benchmarking, profiling, and unsafe auditing are each time-consuming activities; combining them with documentation and a retrospective exceeded the 2-hour target
- **Scope**: Set up criterion benchmarks for 3+ operations at multiple input sizes, generate flamegraph to identify hot paths, apply at least one profiling-driven optimization, document before/after measurements. Comparison against std lib equivalents included.
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~75-90 min (Moderate-Heavy)
- **Needs split**: No
- **Issues**: Prerequisites should reference 084a AND 084b specifically. Clarify comparison targets for each project option.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~75-90 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Minor: Prerequisites should reference 084a AND 084b specifically. Should clarify comparison targets for each project option.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match (split sub-part)
- **Time estimate**: 75-90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Benchmarking and optimization phase. Requires criterion familiarity from earlier lessons.
- **Unresolved from prior reviews**: None
- **New findings**: Minor -- reference 084a/084b specifically as prerequisites. Clarify comparison targets per project option (e.g., Option A vs tokio, Option B vs nom, Option C vs BTreeMap).
- **Recommendation**: Update prerequisite references and add per-option comparison targets when task content is next updated

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 75-95min (Heavy)
- **Needs split**: No
- **Progression**: Benchmarking and optimization phase. Requires criterion familiarity from earlier lessons.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Minor: clarify per-option benchmark comparison targets (A vs tokio, B vs nom, C vs BTreeMap)
- **Recommendation**: Add per-option comparison targets when task content is next updated

### v11-fix - Added per-option benchmark comparison targets (2026-03-04)
- Added specific comparison targets for each project option (tokio, nom, BTreeMap)
- **Resolves**: Minor item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: perf installation may need guidance
- **Recommendations**: Add `sudo apt install linux-tools-generic` note and perf_event_paranoid hint
- **Changes made**: Changelog updated only

### v13-fix - Applied pending fixes (2026-03-04)
- Added Linux perf installation guidance (linux-tools-generic, perf_event_paranoid, cargo install flamegraph) and macOS note
- **Why**: Profiling tools require platform-specific setup that can block progress
- **Resolves**: v12 recommendation

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-90min
- **Pacing**: Good/Heavy
- **Issues**: Prerequisite reference to "Lesson 084" should specify split parts
- **Changes made**: Updated prerequisite reference to Lessons 084a/084b, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-90min. **Pacing**: Good/Heavy. **Issues**: None — prerequisites, comparison targets, and setup notes verified. **Changes**: Changelog only.
