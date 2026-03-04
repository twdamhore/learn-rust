# Changelog - Lesson 056: move closures, closures as parameters and return values

## Section 11: Closures & Functional Patterns

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: `move` keyword for ownership transfer, closures as parameters (generic and trait object), returning closures with `impl Fn`, `Box<dyn Fn>` storage, Java effectively-final comparison
- **Exercises added**: Move closure for thread spawning, `make_adder`/`make_greeter` returning closures, EventEmitter callback system with `Box<dyn Fn>`, closure trait hierarchy demonstration

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 1 uses `std::thread::spawn` -- not taught until lesson 063 (forward reference)
  - make_adder exercise duplicates task 042 exercise 4
  - Exercise 3 (EventEmitter) is a substantial mini-project
- **Recommendations**:
  - Note the thread::spawn forward reference explicitly
  - Differentiate from task 042's make_adder or remove duplication

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Exercise 1 uses std::thread::spawn before taught (lesson 58). make_adder duplicates task 042 Exercise 4. EventEmitter (Exercise 3) combining Vec<Box<dyn Fn>>, 'static bounds, and callback registration is ambitious.
- **Why**: Forward reference and duplication issues.
- **v4 recommendations status**: Not yet applied -- v4 flagged thread::spawn forward reference and make_adder duplication. Gradual progression: Heavy spike from moderate lesson 51.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise 1 uses thread::spawn (not taught until lesson 58)
  - make_adder duplicates task 042
  - EventEmitter (Exercise 3) is a substantial mini-project
- **Action taken**: No structural changes. Heavy but within 2hr threshold.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed under relaxed threshold
- Thread::spawn forward reference and EventEmitter mini-project still flagged.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy)
- **Needs split**: No
- **Issues**: (1) Exercise 1 uses thread::spawn before lesson 063 -- replace with non-threading move motivation. (2) Exercise 2 make_adder duplicates task 042 Ex4. (3) Exercise 3 EventEmitter should be marked [STRETCH]. All flagged since v4, unresolved.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: PREREQUISITE VIOLATION (minor) — Exercise 1 uses std::thread::spawn (not taught until lesson 58). Replace with non-threading move motivation. DUPLICATE EXERCISE — Exercise 2 (make_adder) duplicates task 042 Exercise 4. Change to make_multiplier. Exercise 3 (EventEmitter) should be [STRETCH]. Flagged since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Heavy spike from moderate lesson 055
- **Unresolved from prior reviews**: (1) Exercise 1 uses thread::spawn (not taught until 058) -- use non-threading move motivation instead, (2) Exercise 2 make_adder duplicates task 042 -- rename to avoid duplication, (3) Exercise 3 EventEmitter should be marked [STRETCH]. All flagged since v4.
- **New findings**: None
- **Recommendation**: Apply three content fixes at lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-100min (Heavy)
- **Needs split**: No
- **Progression**: Heavy spike from moderate lesson 055
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: 3 issues from v4: (1) Exercise 1 uses thread::spawn not taught until 058 -- replace with non-threading move motivation, (2) make_adder duplicates task 042 -- rename, (3) EventEmitter already [STRETCH] -- OK
- **Recommendation**: Apply three content fixes at lesson start

### v11-fix - Fixed thread::spawn forward reference and naming duplication (2026-03-04)
- Exercise 1: replaced thread::spawn with returning-closure-from-function pattern
- Exercise 2: renamed to avoid duplication with task 042
- **Why**: thread::spawn not taught until lesson 063; naming duplication with lesson 044
- **Resolves**: MODERATE priority items from v11 (flagged since v4)

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Minor — verify v11-fix was applied to task file. Ex 3 EventEmitter correctly [STRETCH].
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: Uses Box<dyn Fn> (lesson 54 covers Box in depth, but trait objects with Box covered in 43). Add reference to lesson 43 for context
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-90min
- **Pacing**: Heavy lower end
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-90min. **Pacing**: Heavy lower end. **Issues**: None — forward reference violations resolved. **Changes**: Changelog only.
