# Changelog - Lesson 095: Benchmarking Part B: Profiling and Optimization

## Section 18: Testing & Quality

### v1 - Created from task-094 split (2026-03-03)
- Split from original task-094 which was assessed as >2 hr due to too many distinct tools/topics
- Part B covers flamegraph generation, profiling-driven optimization cycle, and interpreting profiling results
- Exercises: flamegraph of HashMap program with optimization comparison, iterative profiling-driven optimization of word frequency counter
- **Estimated time**: ~1-1.5 hr
- **Pacing verdict**: OK - under 2hr threshold
- **Split needed**: N/A (this IS the split result)
- **Key issues**: Platform-specific tooling requirements noted in task Notes section; Exercise 2 is iterative but scoped to 2-3 rounds
- **Action taken**: Created task-095.md with 4 objectives and 2 exercises from the original task-094; added platform-specific tooling notes

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~75-90 min (Moderate-Heavy)
- **Needs split**: No
- **Issues**: Exercise 1 uses FxHashMap from rustc-hash crate -- mention this dependency explicitly.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~75-90 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Minor: Exercise 1 references FxHashMap from rustc-hash crate — should be mentioned explicitly in Notes.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Correct (split from 084)
- **Time estimate**: 75-90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Profiling and flamegraphs well-scoped after split. Platform-specific notes in place.
- **Unresolved from prior reviews**: None
- **New findings**: Minor: Exercise 1 should note that FxHashMap comes from the rustc-hash crate (add to Notes or exercise text)
- **Recommendation**: Add rustc-hash crate note to Exercise 1 before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-100min (Heavy)
- **Needs split**: No
- **Progression**: Profiling and flamegraphs well-scoped. Platform-specific tooling notes present.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: Minor: FxHashMap (`rustc-hash` crate) should be noted in exercise text

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-100min
- **Pacing**: Heavy
- **Issues**: Minor — Ex 1 references FxHashMap without naming rustc-hash crate
- **Recommendations**: Add note that FxHashMap comes from `rustc-hash` crate
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good
- **Issues**: FxHashMap from rustc-hash crate not introduced — add brief explanation when first mentioned in Exercise 1
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: Added FxHashMap/rustc-hash crate note to Exercise 1 (was referenced without introduction)
- **Changes made**: Added rustc-hash crate installation and import instructions to Exercise 1 in task file

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-95min. **Pacing**: Heavy. **Issues**: None — FxHashMap note and platform notes verified. **Changes**: Changelog only.
