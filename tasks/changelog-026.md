# Changelog - Lesson 026: Advanced patterns - guards, bindings, nested patterns, @

## Section 5: Structuring Data

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Match guards with if conditions, @ bindings for capture-and-test, nested enum/struct matching, or-patterns with |, pattern matching on references
- **Exercises added**: Grade letter function with guards and tuple matching, categorize_age with @ bindings, nested Config/DbConfig/ConnectionType destructuring, recursive Expr evaluator with eval and simplify using Box<Expr>

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 4 uses `Box<T>` for recursive types -- Box is covered in lesson 058
  - Exercise 4 (evaluator + simplifier) could take 20-30 minutes alone
- **Recommendations**:
  - Provide brief Box<T> explanation inline or acknowledge it as a preview
  - Consider making the simplify() portion of Exercise 4 optional

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Exercise 4 introduces Box<T> (not taught until lesson 54 -- 30 lessons later) for recursive Expr. Requires recursive enum + eval() + simplify() with pattern guards.
- **Why**: Box<T> is a major forward reference; simplify() is too ambitious as required.
- **v4 recommendations status**: Not yet applied -- v4 recommended making simplify() optional and noting Box<T> preview. Gradual progression: Heavy spike; Exercise 4 needs trimming.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hr
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise 4 uses Box<T> (not taught until lesson 54 - major forward reference)
  - simplify() is too ambitious as required
  - v4 recommendation to make simplify() optional not applied
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- No changes needed under relaxed threshold. Expression evaluator exercise (Box<T> forward ref) still flagged but within limit.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-120 min (Heavy)
- **Needs split**: No
- **Progression**: Exercises 1-3 are well-calibrated. Exercise 4 is the problem.
- **Issues**: Exercise 4 uses Box<T> (not taught until lesson 058 -- 30-lesson forward reference). simplify() should be marked [STRETCH] (both flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-120 min
- **Pacing**: Heavy
- **Needs split**: No (upper edge)
- **Issues**: PREREQUISITE VIOLATION — Exercise 4 uses Box<T> for recursive Expr enum (Box not taught until lesson 54, 30 lessons away). Exercise 4 simplify() should be [STRETCH]. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90-120 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Exercises 1-3 are well-calibrated. Exercise 4 (recursive Expr with Box<T>) is the problem child.
- **Unresolved from prior reviews**: (1) PREREQUISITE VIOLATION - Exercise 4 uses Box<T> (not taught until lesson 54), needs inline explanation. (2) simplify() portion should be marked [STRETCH]. Both flagged since v4, never applied.
- **New findings**: None
- **Recommendation**: Add brief Box<T> explanation inline and mark simplify() as [STRETCH] when lesson begins

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy, upper edge)
- **Needs split**: No
- **Progression**: Exercises 1-3 well-calibrated; Exercise 4 is the heavy hitter.
- **Changelog reconciliation**: (1) "simplify() should be [STRETCH]" -- Exercise 4 IS already marked [STRETCH] in task file. Resolved. (2) Box<T> prerequisite violation (lesson 058) -- mitigated by inline preview note and [STRETCH] tag. Acceptable.
- **Genuinely unresolved**: None
- **Recommendation**: No changes needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy
- **Issues**: Ex 4 uses Box<T> (lesson 058) but marked [STRETCH] with preview note.
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good
- **Issues**: Exercise 4 (STRETCH) uses Box<T> (lesson 54) for recursive types — preview note provided. Objective 5 `ref` pattern is largely obsoleted by Rust 2018+ match ergonomics
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-90min
- **Pacing**: Medium-Heavy
- **Issues**: None (v13 concerns resolved)
- **Changes made**: Clarified range patterns vs match guards in Exercise 1 (90..=100 is a range pattern, `if` is a guard); noted `ref` as legacy in Objective 5, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-90min. **Pacing**: Medium-Heavy. **Issues**: None — Exercises 1-3 well-scoped, Ex 4 STRETCH with Box preview. **Changes**: Changelog only.
