# Changelog - Lesson 067b: Advanced Async - Part B: Pin, Unpin, and Executor Internals
## Section 14: Async Rust

### v1 - Created from split (2026-03-03)
- Split from original lesson 067 which was rated OVERLOADED (~2-3 hrs)
- **Reason for split**: Pin/Unpin is notoriously the most difficult Rust concept. Combined with building a mini executor, this needed its own dedicated lesson. Pin content from lesson 057 also consolidated here where it has proper async context
- **Scope**: Why Pin exists (self-referential futures), Pin<&mut T> vs Pin<Box<T>>, Unpin marker trait, building a minimal single-threaded executor (stretch goal)
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-110 min (Heavy -- hardest lesson in 063-080 range even after split)
- **Needs split**: No
- **Issues**: Pin/Unpin is the hardest Rust concept. Learner has no C/C++ background. Exercise 2 (block_on with RawWaker) needs Waker boilerplate provided.
- **Changes made**: None (scaffolding deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-120 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Hardest lesson in 063-080 range even after split. Pin/Unpin most conceptually difficult Rust topic for non-C/C++ learner. Exercise 2 (simple block_on with RawWaker) requires RawWaker/RawWakerVTable -- boilerplate MUST be provided. Exercise 3 (task queue executor) correctly marked stretch.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Correct split from original 067
- **Time estimate**: 80-120 minutes (Very Heavy)
- **Needs splitting**: No (but hardest lesson in 063-080 range even after split)
- **Pacing context**: Pin/Unpin is the most conceptually difficult Rust topic. For non-C/C++ learner this is the steepest cliff in the curriculum.
- **Unresolved from prior reviews**: Exercise 2 needs RawWaker/RawWakerVTable boilerplate provided -- learner should not have to discover this API from scratch (flagged since v2)
- **New findings**: None
- **Recommendation**: Provide complete RawWaker/RawWakerVTable boilerplate for Exercise 2 when lesson is started

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 100-120min (Very Heavy)
- **Needs split**: No
- **Progression**: Hardest lesson in curriculum even after split
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: **CRITICAL** — Exercise 2 RawWaker/RawWakerVTable boilerplate MUST be provided before teaching. Without it, lesson breaks 2hr threshold.
- **Recommendation**: Provide complete RawWaker/RawWakerVTable boilerplate for Exercise 2 before lesson start — this is a blocking prerequisite

### v11-fix - Applied RawWaker boilerplate scaffold (2026-03-04)
- Added complete RawWaker/RawWakerVTable boilerplate to Exercise 2
- **Why**: RawWaker API is arcane; learner should focus on block_on logic, not Waker construction
- **Resolves**: CRITICAL item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 100-120min
- **Pacing**: Heavy (borderline OVERLOADED)
- **Issues**: Hardest lesson in curriculum. Pin/Unpin notoriously difficult.
- **Recommendations**: Add "mental model" analogy section at top (e.g., pinning note to corkboard)
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Added "Mental Model for Pin" section between Objectives and Exercises
- Uses desk/document analogy: pinned document can be read/modified but not moved to another desk
- Covers why Pin exists (self-referential futures), what it prevents (swap/replace), and what Unpin means (opt-out for types without self-references)
- **Why**: Pin/Unpin is the hardest concept in the curriculum; a concrete analogy before exercises helps build intuition
- **Resolves**: Recommendation from v12

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: PREREQUISITE VIOLATION: block_on exercise requires unsafe { Waker::from_raw(dummy_raw_waker()) } with RawWaker/RawWakerVTable — unsafe not taught until lesson 73. Scaffold provides the unsafe code. Add prominent note: learner should focus on block_on logic, not the unsafe parts
- **Changes made**: Changelog updated only

### v13-fix - Applied pending task file fixes (2026-03-04)
- Added prominent "focus on logic, not unsafe" disclaimer to block_on exercise
- **Why**: Exercise requires unsafe Waker construction (lesson 73) — learner should focus on executor polling logic, not the unsafe scaffolding
- **Resolves**: v13 prerequisite finding

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: Added concrete self-referential struct example to Exercise 1 to give learners a starting point
- **Changes made**: Task file updated — added SelfRef struct example, explanation of why self-referential structs fail in Rust, and guidance on exploring Pin with Box::pin() and Pin::as_mut()

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-100min. **Pacing**: Heavy (hardest lesson in curriculum). **Changes**: Reworded Exercise 1 description from misleading "use Pin to fix it" to "explore how Pin prevents moving pinned values, understanding why this matters for async futures." **Why**: Pin does not fix self-referential structs; the original phrasing was misleading about what Pin actually does.
