# Changelog - Lesson 052: Lifetime Practice Part B: Lifetime Design Patterns
## Section 10: Lifetimes

### v1 - Created from split (2026-03-03)
- Split from original lesson 051 which was rated Heavy-to-Overloaded (~2-2.5 hrs) during v7 pacing review
- **Reason for split**: The original lesson packed 4 exercises spanning two distinct skill areas (diagnosing errors vs design patterns) into one session. Splitting lets each half breathe and stay within the 1-hour target.
- **Scope**: The design-patterns half -- simplifying over-annotated lifetimes using elision rules and clippy, plus building a Cache struct that encounters and resolves the "cannot borrow as mutable because it is also borrowed as immutable" pattern. Focus is on knowing when to annotate vs restructure, and handling common borrow-conflict design challenges.
- **Other half (051)**: Diagnosing Lifetime Errors -- the 5-program lifetime puzzle set and the borrowed-to-owned Tokenizer refactor. Focus is on reading compiler errors and applying fix strategies.
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60 min (Moderate)
- **Needs split**: No
- **Issues**: None. Well-scoped after split.
- **Changes made**: None

### v3 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~60 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: None
- **Changes made**: Changelog updated only

## v4 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Part of bridging lesson 051 (split)
- **Time estimate**: 60 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Design-patterns half of original 049; well-scoped after split
- **Unresolved from prior reviews**: None
- **New findings**: None
- **Recommendation**: No changes needed

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 50-70min (Moderate)
- **Needs split**: No
- **Progression**: Well-scoped after split
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No changes needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 50-70min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 45-60min
- **Pacing**: Good
- **Issues**: Cache exercise may need RefCell (not taught until lesson 56) to resolve borrow conflict — add resolution hint clarifying expected approach (restructuring, not RefCell)
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 45-60min
- **Pacing**: Light-Medium
- **Issues**: Cache exercise borrow conflict could lead learner toward RefCell (not taught until lesson 060)
- **Changes made**: Added resolution hint to Cache exercise clarifying to use `contains_key` + `insert` pattern rather than `RefCell`, which is taught in lesson 060.

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 45-60min. **Pacing**: Light-Medium. **Issues**: None — good breathing room before advanced lifetimes. **Changes**: Changelog only.
