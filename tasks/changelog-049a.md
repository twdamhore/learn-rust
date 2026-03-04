# Changelog - Lesson 049a: Lifetime Practice Part A: Diagnosing Lifetime Errors
## Section 10: Lifetimes

### v1 - Created from split (2026-03-03)
- Split from original lesson 049 which was rated Heavy-to-Overloaded (~2-2.5 hrs) during v7 pacing review
- **Reason for split**: Exercise 1 alone contains 5 broken programs to debug and fix (25-50 min), and Exercise 2 (Tokenizer refactor) is a substantial code transformation. Combined with Exercises 3-4, the lesson far exceeded the 1-hour target. A "practice/consolidation" bridging lesson should not be one of the heaviest in the curriculum.
- **Scope**: The diagnostic/debugging half -- the 5-program lifetime puzzle set and the borrowed-to-owned Tokenizer refactor. Focus is on reading compiler errors, applying fix strategies, and building intuition for references vs owned data.
- **Other half (049b)**: Lifetime Design Patterns -- over-annotated simplification exercise and the Cache struct exercise. Focus is on when to annotate vs restructure, elision rules, and resolving mutable/immutable borrow conflicts.
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy)
- **Needs split**: No
- **Issues**: Should reduce puzzle programs from 5 to 3 (drop puzzles 4 and 5). Puzzle 4 is too advanced; puzzle 5 overlaps lesson 051.
- **Changes made**: None (content fix deferred to lesson start)

### v3 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 1 should be reduced from 5 to 3 puzzle programs. Puzzle 4 (cross-referencing structs) too advanced. Puzzle 5 (closure capturing reference) overlaps lesson 51. Flagged at v2.
- **Changes made**: Changelog updated only

## v4 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Part of bridging lesson 049 (split)
- **Time estimate**: 75-90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Diagnostic/debugging half of the original 049 bridging lesson
- **Unresolved from prior reviews**: Reduce puzzles from 5 to 3 -- drop puzzle 4 (too advanced) and puzzle 5 (overlaps lesson 051). Flagged since v2.
- **New findings**: None
- **Recommendation**: Remove puzzles 4 and 5 before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 75-100min (Heavy)
- **Needs split**: No
- **Progression**: Diagnostic/debugging half of original 049 bridging lesson
- **Changelog reconciliation**: "Reduce puzzles from 5 to 3" -- task file already shows 3 puzzles. Resolved.
- **Genuinely unresolved**: Tokenizer refactor (Ex 2) is the real time risk
- **Recommendation**: Monitor Exercise 2 time at lesson start; puzzle count issue is resolved

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-100min
- **Pacing**: Heavy
- **Issues**: Ex 2 (Tokenizer refactor) is the time risk
- **Recommendations**: Consider time-boxing Ex 2 or providing partial starter code
- **Changes made**: Changelog updated only

### v13-fix - Applied pending fixes (2026-03-04)
- Added time-box guidance (~30 min) and starter code skeleton for Exercise 2 (Tokenizer refactor)
- **Why**: Tokenizer refactor is the primary time risk; starter code reduces friction
- **Resolves**: v11/v12 recommendation (high priority)

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 50-65min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 50-70min
- **Pacing**: Medium
- **Issues**: No issues
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 50-70min. **Pacing**: Medium. **Issues**: None — well-paced after time-box additions. **Changes**: Changelog only.
