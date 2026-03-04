# Changelog - Lesson 058: Box<T> - heap allocation, recursive types

## Section 12: Smart Pointers & Interior Mutability

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Heap allocation with Box, recursive types (linked list, tree), Deref/Drop smart pointer traits, Box<dyn Trait> for dynamic dispatch, comparison with Java's `new` and Go pointers
- **Exercises added**: Singly linked list with Cons/Nil, binary search tree with insert/contains/in_order, large struct boxing with size_of_val, Shape trait with Box<dyn Shape> heterogeneous collection

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 2 (BST) could take 20-30 minutes alone for someone unfamiliar with recursive Rust types
  - Exercise 4 (Box<dyn Shape>) repeats nearly identical pattern from task 043
- **Recommendations**:
  - Make BST exercise optional or reduce scope (e.g., insert + contains only, skip in_order)
  - Differentiate or remove the Shape exercise to avoid duplication with task 043

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: BST exercise (insert + contains + in_order traversal) could take 20-30 min alone for recursive Rust types. Vec<Box<dyn Shape>> duplicates task 043. Deref/Drop overlap with lesson 047.
- **Why**: BST too ambitious; duplication with 043.
- **v4 recommendations status**: Not yet applied -- v4 recommended scoping down BST, differentiating Shape exercise. Gradual progression: Starting smart pointers with heavy lesson.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - BST exercise could take 20-30 min alone
  - Vec<Box<dyn Shape>> duplicates task 043
  - Deref/Drop overlaps lesson 047
- **Action taken**: No structural changes. Heavy but within 2hr threshold.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed under relaxed threshold
- BST exercise still substantial. First of heavy cluster (054-057).

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy)
- **Needs split**: No
- **Progression**: First of 4-lesson heavy cluster (054-055-056-057).
- **Issues**: Exercise 2 (BST) should reduce to insert+contains only -- drop in_order traversal (optional extension). Exercise 4 (Box<dyn Shape>) overlaps task 043. Both flagged since v4.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 2 (BST) too ambitious — insert+contains+in_order traversal. Reduce to insert+contains, make in_order optional. DUPLICATE EXERCISE — Exercise 4 (Vec<Box<dyn Shape>>) repeats pattern from task 043. Replace with different trait. Start of heavy cluster (058-059-060-061/062). Flagged since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Start of heavy cluster 054-057. Four consecutive heavy lessons risk burnout.
- **Unresolved from prior reviews**: (1) BST exercise -- reduce to insert+contains, make in_order [STRETCH], (2) Exercise 4 Vec<Box<dyn Shape>> duplicates task 043. Both flagged since v4.
- **New findings**: None
- **Recommendation**: Apply BST scope reduction and resolve Shape duplication at lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-100min (Heavy)
- **Needs split**: No
- **Progression**: BST exercise already [STRETCH]. Starts a heavy cluster (054-057).
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: in_order within BST stretch should be explicitly optional
- **Recommendation**: Make in_order explicitly optional within BST [STRETCH] at lesson start

### v11-fix - Marked in_order as optional within BST stretch (2026-03-04)
- Added [OPTIONAL] tag to in_order traversal within the BST [STRETCH] exercise
- **Why**: BST insert + contains is sufficient for the learning goal
- **Resolves**: Minor item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Ex 4 (Box<dyn Animal>) nearly identical to lesson 045 trait object pattern — should use different domain. UNRESOLVED from v4.
- **Recommendations**: Change to different trait domain (e.g., FileSystem with size/name)
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Changed Exercise 4 domain from `Animal` (speak/name with Dog/Cat) to `Logger` (log/level with ConsoleLogger/FileLogger/JsonLogger)
- **Why**: Box<dyn Animal> pattern was nearly identical to task 043's trait object exercise (flagged since v4). Task 054 now uses a Logger system while task 043 uses a Widget UI system, giving each lesson a distinct domain.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-85min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-85min
- **Pacing**: Heavy lower end
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-85min. **Pacing**: Heavy lower end. **Issues**: None — BST scoping and domain differentiation good. **Changes**: Changelog only.
