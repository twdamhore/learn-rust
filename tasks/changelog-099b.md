# Changelog - Lesson 099b: Capstone Project 3 - Part B: Completion and Polish
## Section 21: Capstone Projects

### v1 - Created from split (2026-03-03)
- Split from original lesson 099 which was rated OVERLOADED (~3-5 hrs)
- **Reason for split**: Original tried to cover architecture design, full implementation, unsafe code, and 15+ tests with proptest in one session
- **Scope**: Complete remaining implementation, add error handling, write 3-5 more tests for edge cases. Optional stretch goal: add one unsafe optimization with SAFETY comments, or add proptest for a key invariant. Builds on the architecture and core from 099a.
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~75-90 min for Options B/C; ~90-120 min for Option A
- **Needs split**: No
- **Issues**: Option A (spawn + block_on with Waker) is the hardest exercise in the entire curriculum. Provide partial Waker implementation/skeleton. Clarify Option B evaluator scope (integers + arithmetic only).
- **Changes made**: None (scaffolding deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~75-90 min (Options B/C), ~90-120 min (Option A)
- **Pacing**: Good to Heavy
- **Needs split**: No
- **Issues**: Option A (spawn + block_on with Waker) is hardest exercise in entire curriculum — provide partial Waker skeleton. Option B evaluator scope should be clarified (integers + arithmetic only).
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match (split sub-part)
- **Time estimate**: 75-120 minutes (Heavy to Very Heavy, option-dependent)
- **Needs splitting**: No
- **Pacing context**: Completion and polish phase. Time varies significantly by option: B/C ~75-90min, A ~90-120min.
- **Unresolved from prior reviews**: (1) Option A needs partial Waker skeleton -- hardest exercise in entire curriculum. (2) Option B evaluator scope should be integers + arithmetic only.
- **New findings**: None
- **Recommendation**: Provide Waker skeleton for Option A and clarify Option B evaluator scope when task content is next updated

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 75-130min (Heavy to Very Heavy, option-dependent)
- **Needs split**: No
- **Progression**: Completion and polish phase. Time varies significantly by option.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: (1) Option A Waker skeleton MUST be provided — hardest exercise in entire curriculum. (2) Option B evaluator scope must be clarified (integers + arithmetic only).
- **Recommendation**: Provide Waker skeleton for Option A and clarify Option B evaluator scope before lesson start

### v11-fix - Added Option A Waker skeleton and Option B scope clarification (2026-03-04)
- Added Arc<Signal>-based Waker scaffold for Option A (async executor)
- Added explicit evaluator scope for Option B: integers + arithmetic only
- **Why**: Option A Waker implementation is the hardest single exercise in the curriculum; Option B scope was ambiguous
- **Resolves**: HIGH priority item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-130min
- **Pacing**: Heavy (Option A borderline OVERLOADED)
- **Issues**: (1) Option A remains extremely ambitious. (2) Reference to "lesson 067b" may be broken — verify.
- **Recommendations**: Verify 067b reference; consider providing complete signal_waker implementation for Option A
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Verified "lesson 067b" reference in Exercise 1 Option A: task-067b.md exists and the reference is correct (no fix needed)

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-120min (varies by option)
- **Pacing**: Heavy
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-120min (option-dependent). **Pacing**: Heavy. **Changes**: Added RawWaker pattern reminder to Option A Waker scaffold. **Why**: todo!() references lesson 067b without a reminder of the pattern; adding key function names reduces back-and-forth.
