# Changelog - Lesson 099: Project 3 - Systems tool (async runtime piece OR parser OR custom data structure)

## Section 21: Capstone Projects

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Choose from 3 project options (executor/parser/B-tree), architecture design before implementation, core logic with advanced Rust features, justified unsafe with safe wrappers, TDD with thorough testing
- **Exercises added**: Option A (single-threaded async executor with Waker), Option B (recursive descent parser with AST and evaluator), Option C (generic B-tree with insert/get/remove/iteration), property-based tests with proptest for all options

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Overloaded for 1-hour lesson
- **Issues found**:
  - Each of the three project options is a multi-hour implementation on its own
  - Option A (async executor with Waker) is arguably one of the hardest possible Rust exercises
  - Option C (B-tree with node splitting/merging) is notoriously difficult
  - Expectation of 15+ tests AND proptest on top of core implementation is very ambitious
  - Exercise format uses unnumbered bullets (formatting inconsistency)
- **Recommendations**:
  - Reduce test requirement from 15+ to 8-10
  - Provide more detailed architecture guidance for each option
  - Consider that this is a 2-hour project (099+100), scope accordingly
  - Standardize exercise format

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: OVERLOADED (~3-4+ hr for any option) for 1-2 hour target
- **Changes noted**: Each option (async executor, parser, B-tree) is multi-hour on its own. Option A (executor with Waker) is arguably one of hardest Rust exercises possible. Option C (B-tree with splitting/merging) is notoriously complex. 15+ tests plus proptest on top is unrealistic. No architecture guidance or scaffolding. Exercise format inconsistency.
- **Why**: Multi-hour projects with unrealistic test expectations.
- **v4 recommendations status**: Not yet applied -- v4 recommended reducing tests to 8-10, more architecture guidance, scoping for 2-hour total. Gradual progression: Extremely heavy capstone.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~3-5 hours
- **Pacing verdict**: OVERLOADED - split required
- **Split needed**: Yes - split into 099a/099b
- **Key issues**:
  - Each of the 3 project options is multi-hour on its own
  - Option A (async executor) is one of the hardest Rust exercises possible
  - Option C (B-tree with splitting/merging) is notoriously difficult
  - 15+ tests with proptest is unrealistic on top of core implementation
  - No architecture guidance provided
- **Action taken**: Split into task-099a.md (Architecture and Core Implementation -- design, core types, basic operations, initial tests) and task-099b.md (Completion and Polish -- finish implementation, error handling, comprehensive tests). Reduced test requirement from 15+ to 5-8 in Part A and 3-5 more in Part B. Architecture guidance now explicitly provided. Each option scoped to be achievable in ~2 hours across both parts.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Already split in v6 into 099a/099b
- **Status**: No changes needed
- Prior split was adequate under relaxed threshold; no additional changes required

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 099a/099b at v6. Original was ~180-300 min.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~180-300 min
- **Pacing**: OVERLOADED
- **Needs split**: Already split into 099a/099b
- **Issues**: Each project option is multi-hour.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 099a/099b
- **Time estimate**: 180-300 minutes (Overloaded -- original)
- **Needs splitting**: Already split into 099a/099b at v6
- **Pacing context**: Original 3-5 hours. Each project option (executor, parser, B-tree) is multi-hour on its own. Correctly split.
- **Unresolved from prior reviews**: None (issues resolved by split)
- **New findings**: None
- **Recommendation**: No action needed on original; see 099a and 099b changelogs

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: N/A (SUPERSEDED)
- **Needs split**: N/A
- **Progression**: SUPERSEDED by 099a/099b. Split was correct. Design-first approach was good.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No action needed on original; see 099a and 099b changelogs

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 099a/099b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 099a/099b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
