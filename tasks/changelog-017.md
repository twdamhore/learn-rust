# Changelog - Lesson 017: Building with Ownership

## Section 3: Ownership System

### v6 - Created from task-016 split (2026-03-03)
- Split from original task-016 which was critically overloaded (~3-4 hr estimated)
- Part B covers advanced ownership refactoring with structs and methods (previews lessons 19-20)
- **Estimated time**: ~1.5 hr
- **Pacing verdict**: OK - under 2hr threshold
- **Split needed**: N/A (this IS the split result)
- **Key issues**:
  - Previews structs and impl blocks (lessons 19-20) -- scaffolding code provided
  - Exercise 3 previews lifetime annotations (lesson 46) -- pattern provided with explanation
- **Action taken**: Created task-017.md with 3 objectives and 3 exercises; all forward references have scaffolding code and explanatory notes

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate-Heavy (~1.5 hr)
- **Status**: No changes needed

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~75-90 min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Previews structs/impl blocks with full scaffolding.
- **Issues**: Exercise 3 (ConfigView with lifetime annotations) is a significant forward reference to lesson 46. Consider making it optional/bonus.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~75-90 min
- **Pacing**: Heavy (lower end)
- **Needs split**: No
- **Issues**: Minor: Exercise 3 (ConfigView with lifetime 'a) is a significant forward reference to lesson 46. Consider marking optional/bonus.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Aligned (split from 016, previews structs/impl with scaffolding)
- **Time estimate**: 75-100 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Previews structs/impl blocks with full scaffolding provided. Heavier than 016 but within limits.
- **Unresolved from prior reviews**: Exercise 3 (ConfigView with lifetime `'a`) is a significant forward reference to lesson 46. Should be marked [OPTIONAL/BONUS]. Flagged since v2 (017), unresolved.
- **New findings**: None beyond prior reviews
- **Recommendation**: Mark Exercise 3 as [OPTIONAL/BONUS] before teaching

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-110min (Heavy)
- **Needs split**: No
- **Progression**: Exercise 3 lifetime preview correctly marked [OPTIONAL]. Previews structs/impl blocks with full scaffolding — appropriate. Consider adding note to lessons 021-020 about struct preview in 017.
- **Changelog reconciliation**: Exercise 3 lifetime forward reference flagged since v2 (017) — task file now correctly marks it [OPTIONAL]. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: Consider adding a note to lessons 021-020 acknowledging struct preview in 017.

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-110min
- **Pacing**: Heavy
- **Issues**: Previews structs/impl (019-020) with scaffolding; Ex 3 previews lifetimes (046) but correctly marked [OPTIONAL]
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: Exercise 2 references 'working code with 3 unnecessary .clone() calls (provided below)' but no code is actually provided in the task file — this needs to be fixed in a future update
- **Changes made**: Changelog updated only

### v13-fix - Applied pending task file fixes (2026-03-04)
- Added missing code snippet to Exercise 2 — the exercise referenced "working code with 3 unnecessary .clone() calls (provided below)" but no code was present
- **Why**: Exercise is impossible without the starter code to refactor
- **Resolves**: v13 finding (concrete bug)

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-95min
- **Pacing**: Heavy
- **Issues**: Exercise 2 clones lack variety (low priority, not fixed)
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 70-95min
- **Pacing**: Heavy
- **Changes made**: Added inline note to Exercise 2 clone 3 explaining iterator/closure syntax (.iter().map(|n| ...).collect()) and pointing to lessons 37/51
- **Why**: Provided starter code uses iterator/closure patterns not taught until lessons 37 and 51

### v16 (2026-03-04) — Full curriculum review (119 lessons)
- Fixed stale lesson references: 'lessons 19-20' → 'lessons 021-022', 'lessons 37 and 51' → 'lessons 039 and 055', 'lesson 46' → 'lesson 048'

### v17 (2026-03-04) — Human-learning clarity pass
- Reworked Exercise 3 to avoid premature lifetime syntax (removed `ConfigView<'a>` preview) and replaced it with an owned-vs-borrowed API design exercise.
- Simplified Exercise 2 starter code to avoid introducing iterator/closure-heavy syntax before those lessons.
- Updated wording to keep this lesson focused on ownership decisions, not lifetime mechanics.
