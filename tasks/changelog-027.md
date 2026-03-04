# Changelog - Lesson 027: Modules - mod, file structure, visibility (pub)

## Section 6: Project Organization

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Inline modules with mod, file-based module structure (mod.rs vs filename.rs), visibility with pub/pub(crate)/pub(super), module tree navigation with crate::/super::/self::, per-field struct visibility
- **Exercises added**: Refactor inline modules to files, nested shapes library with circle/rectangle sub-modules, visibility controls with private fields and pub(crate)/pub(super), calculator project with operations/input/display module hierarchy

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 4 introduces `pub use` re-exports (lesson 028 topic)
  - Exercises require creating substantial file structures, which takes more time than code-writing
- **Recommendations**:
  - Note the pub use preview explicitly, or move that part to lesson 028

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Module exercises require creating substantial directory/file structures (mechanically slow). Exercise 4 introduces pub use re-exports (lesson 26 topic). Rust module system is very different from Java packages and Go packages.
- **Why**: File structure creation is time-consuming; pub use bleeds into lesson 26.
- **v4 recommendations status**: Not yet applied -- v4 recommended skeleton directory structure and noting pub use as preview. Gradual progression: Heavy; module system requires significant adjustment.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hr
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - File structure creation is mechanically slow
  - Exercise 4 introduces pub use re-exports (lesson 028 topic)
  - v4 recommendation to provide skeleton directory structures not applied
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed
- No changes needed under relaxed threshold.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-90 min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Module system is fundamentally different from Java/Go packages. Mechanical file creation eats clock time.
- **Issues**: Exercise 4 introduces pub use re-exports (lesson 028 topic). Providing skeleton directory structures would save time (both flagged since v4).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 4 introduces pub use re-exports (lesson 26 topic — topic bleed). Exercises require creating substantial file/directory structures, mechanically slow. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 80-90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Rust module system is fundamentally different from Java packages and Go packages. Mechanical file/directory creation eats clock time.
- **Unresolved from prior reviews**: (1) Exercise 4 introduces pub use re-exports (lesson 028 topic -- topic bleed). (2) Exercises require substantial file structure creation -- provide skeleton structures. Both flagged since v4, never applied.
- **New findings**: None
- **Recommendation**: Provide skeleton directory structures and note pub use as preview when lesson begins

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-100min (Heavy)
- **Needs split**: No
- **Progression**: Exercise 4 `pub use` topic bleed partially addressed with inline preview note. Providing skeleton directory structures would save 15-20min.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 4 pub use topic bleed (partially mitigated); skeleton directory structures not yet provided
- **Recommendation**: Provide skeleton directory structures at lesson start to reduce mechanical overhead

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Mechanical dir/file creation eats time; Ex 4 `pub use` topic bleed with lesson 028.
- **Recommendations**: Provide skeleton directory structures to save 15-20min.
- **Changes made**: Changelog updated only

### v13-fix - Applied pending fixes (2026-03-04)
- Added skeleton directory structures for Exercise 2 and Exercise 4
- **Why**: Creating module directory structures manually consumes 15-20 min of mechanical overhead
- **Resolves**: v11/v12 recommendation (high priority)

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: Exercises 2 and 4 both require creating multi-file project structures from scratch — significant file-system setup overhead. Exercise 4 is essentially a mini-project (calculator with 5 modules)
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: None (skeleton structures already present from v13)
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-95min. **Pacing**: Heavy. **Issues**: None — skeleton structures significantly improve pacing. **Changes**: Changelog only.
