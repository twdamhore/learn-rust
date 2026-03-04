# Changelog - Lesson 060: RefCell<T>, Cell<T> - interior mutability, runtime borrow checking

## Section 12: Smart Pointers & Interior Mutability

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Interior mutability pattern, RefCell runtime borrow checking with borrow/borrow_mut, Cell for Copy types, Rc<RefCell<T>> combination, Java mutability comparison
- **Exercises added**: Shared Vec via Rc<RefCell<Vec>>, deliberate runtime borrow panic, Observer pattern with Rc<RefCell<dyn Observer>>, Cell-based invocation counter on &self methods

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 3 (Observer pattern) combines Rc, RefCell, dyn Observer, and the observer design pattern -- potentially overwhelming
- **Recommendations**:
  - Provide a skeleton/scaffold for Exercise 3 to guide the learner through the complex type composition

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Exercise 3 (Observer pattern) combines Rc + RefCell + dyn Observer + design pattern -- Vec<Rc<RefCell<dyn Observer>>> would intimidate intermediate Rust devs.
- **Why**: Overly complex type nesting.
- **v4 recommendations status**: Not yet applied -- v4 recommended providing skeleton/scaffold for Exercise 3. Gradual progression: Heavy; third heavy in a row (054-055-056).

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Observer pattern Exercise 3 requires Vec<Rc<RefCell<dyn Observer>>> - intimidating type
  - Third heavy lesson in a row (054-055-056)
- **Action taken**: No structural changes. Heavy but within 2hr threshold.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed under relaxed threshold
- Observer pattern exercise still flagged as complex. Third heavy in a row.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy)
- **Needs split**: No
- **Progression**: Third heavy lesson in a row. Learner burnout risk.
- **Issues**: Exercise 3 Observer pattern (Vec<Rc<RefCell<dyn Observer>>>) is overwhelmingly complex type nesting. Provide a code skeleton or simplify to Vec<Box<dyn Observer>> (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 3 (Observer pattern) type Vec<Rc<RefCell<dyn Observer>>> is overwhelmingly complex. Simplify to Vec<Box<dyn Observer>> with &mut self on notify, or provide skeleton. Third heavy in a row (054-055-056). Flagged since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Third heavy lesson in a row (054-055-056). Burnout risk.
- **Unresolved from prior reviews**: Exercise 3 Observer pattern type Vec<Rc<RefCell<dyn Observer>>> too complex -- simplify to Vec<Box<dyn Observer>> with &mut self. Flagged since v4.
- **New findings**: None
- **Recommendation**: Simplify Observer pattern type at lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-110min (Heavy)
- **Needs split**: No
- **Progression**: Third consecutive heavy lesson -- burnout risk
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 3 Observer pattern type `Vec<Rc<RefCell<dyn Observer>>>` is overwhelmingly complex -- simplify to `Vec<Box<dyn Observer>>` with `&mut self`
- **Recommendation**: Simplify Observer pattern type at lesson start; monitor learner fatigue in heavy cluster

### v11-fix - Simplified Observer pattern types (2026-03-04)
- Changed from Vec<Rc<RefCell<dyn Observer>>> to Vec<Box<dyn Observer>> with &mut self
- Rc<RefCell<>> pattern already demonstrated in Exercises 1-2; Exercise 3 now focuses on trait objects
- **Why**: Original type nesting was intimidating even for intermediate Rust developers
- **Resolves**: MODERATE priority item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-110min
- **Pacing**: Heavy
- **Issues**: Third consecutive heavy lesson (054-055-056) — burnout risk
- **Recommendations**: Add checkpoint note acknowledging heavy cluster
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-90min
- **Pacing**: Heavy lower end
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-90min. **Pacing**: Heavy lower end. **Issues**: Third consecutive heavy in 054-056 cluster. Burnout risk acknowledged but content progression logical. **Changes**: Changelog only.
