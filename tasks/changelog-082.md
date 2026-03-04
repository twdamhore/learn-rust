# Changelog - Lesson 082: Unsafe functions, unsafe traits, unsafe impl

## Section 16: Unsafe & FFI

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Unsafe functions with # Safety docs, unsafe traits and unsafe impl, safe wrapper pattern (unsafe sandwich), safety documentation conventions, studying unsafe in std
- **Exercises added**: get_unchecked with documented invariants, ZeroInitializable unsafe trait, SafeBuffer with raw pointer internals and safe API, std source study of Vec::push and String::from_utf8_unchecked

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 3 (SafeBuffer with raw pointer heap allocation) is disproportionately large -- essentially 'write your own Vec'
- **Recommendations**:
  - Provide a skeleton for SafeBuffer or reduce scope to fixed-capacity buffer

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Exercise 3 (SafeBuffer with raw pointer heap allocation using std::alloc::alloc) is essentially "write your own mini-Vec" -- could take 30-40 min alone.
- **Why**: SafeBuffer exercise disproportionately large.
- **v4 recommendations status**: Not yet applied -- v4 recommended skeleton or fixed-capacity scope. Gradual progression: Heavy spike.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - SafeBuffer exercise (Exercise 3) is essentially "write your own mini-Vec" with raw heap allocation
  - Could take 30-40 min alone
  - v4 recommended skeleton or fixed-capacity scope
- **Action taken**: No split required. Previous v4 recommendation to provide skeleton or reduce to fixed-capacity buffer should be applied when lesson is started

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed under relaxed threshold
- SafeBuffer (mini-Vec) exercise still flagged as substantial -- recommend fixed-capacity version or skeleton code when lesson is started

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-110 min (Heavy)
- **Needs split**: No
- **Issues**: Exercise 3 (SafeBuffer with std::alloc) is too hard for a learner with no C background. Provide alloc/dealloc/Layout boilerplate OR switch to fixed-capacity [u8; N] buffer (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-110 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 3 (SafeBuffer with std::alloc::alloc) is disproportionately large — essentially "write your own mini-Vec" with raw heap allocation. For non-C/C++ background, this is hardest in 073-076 range. Provide alloc/dealloc/Layout boilerplate or switch to fixed-capacity [u8; N] buffer. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match with CLAUDE.md
- **Time estimate**: 80-110 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Heavy but within 2hr limit
- **Unresolved from prior reviews**: Exercise 3 (SafeBuffer using std::alloc) too hard for non-C background learner. Must provide alloc/dealloc/Layout boilerplate OR switch to fixed-capacity [u8; N] buffer. Flagged since v4, still unresolved.
- **New findings**: None
- **Recommendation**: Provide alloc boilerplate or switch Exercise 3 to fixed-capacity [u8; N] buffer before teaching

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy)
- **Needs split**: No
- **Progression**: Genuinely unresolved since v4 (7 rounds)
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 3 SafeBuffer with `std::alloc::alloc` too hard for non-C background. Fix: switch to fixed-capacity `[u8; N]` buffer or provide complete alloc/dealloc boilerplate.
- **Recommendation**: Switch Exercise 3 to fixed-capacity `[u8; N]` buffer or provide complete alloc/dealloc boilerplate before teaching

### v11-fix - Simplified SafeBuffer to fixed-capacity buffer (2026-03-04)
- Replaced std::alloc::alloc/dealloc with fixed-capacity [u8; N] stack buffer
- Exercise still demonstrates safe wrappers over unsafe internals (get_unchecked)
- **Why**: std::alloc::alloc is too foreign for learners with no C/C++ background
- **Resolves**: HIGH priority item from v11 (flagged since v4, 7 review rounds)

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Minor — uses const generics (lesson 089) as light forward ref
- **Recommendations**: Add brief inline note about const generics
- **Changes made**: Changelog updated only

### v13-fix - Applied pending fixes (2026-03-04)
- Added inline note explaining const generics `<const N: usize>` in SafeBuffer exercise
- **Why**: Const generics not formally taught until lesson 089; brief explanation prevents confusion
- **Resolves**: v12 recommendation

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Good
- **Issues**: Const generics used here before formal introduction in lesson 80 — inline explanation mitigates but ordering inconsistency exists
- **Changes made**: Changelog updated only

### v13-fix - Applied pending task file fixes (2026-03-04)
- Added const generics cross-reference note pointing to lesson 089
- **Why**: Const generics used before formal introduction — explicit preview note reduces confusion
- **Resolves**: v13 prerequisite finding

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: Const generics forward ref documented (uses const generics before formal introduction in lesson 089 — inline explanation and cross-reference mitigate)
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-95min. **Pacing**: Heavy. **Changes**: Added safety contract reinforcement note to Exercise 2 asking why String/bool should not implement ZeroInitializable. **Why**: Understanding which types violate invariants with zeroed bytes is core to unsafe safety contracts.
