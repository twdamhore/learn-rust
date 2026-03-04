# Changelog - Lesson 072: Attribute macros, real-world macro patterns

## Section 15: Macros

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Attribute macros for transforming definitions, study of real-world macros (tokio::main, serde), helper attributes with derives, macros vs generics/traits decision guide
- **Exercises added**: #[log_calls] attribute macro, #[tokio::main] expansion study, #[validate_positive] attribute macro, macro vs trait comparison exercise

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Assumes strong comfort with proc macro crates from lesson 071
  - Exercise 2 (#[validate_positive]) requires parsing function signatures -- harder than it sounds
- **Recommendations**:
  - If lesson 071 is scaled back, ensure learner has enough proc macro experience before this lesson

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Depends heavily on lesson 071 comfort with proc macro setup. Exercise 3 (validate_positive) requires parsing function signatures -- harder than it appears due to syn API complexity. If 071 is reduced, 072 needs to accommodate.
- **Why**: Dependency chain on potentially-reduced lesson 071.
- **v4 recommendations status**: Not yet applied -- v4 flagged dependency and signature parsing difficulty. Gradual progression: Heavy following overloaded lesson.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Depends on lesson 071 being addressed (now split into 071a/071b)
  - validate_positive attribute requires syn API for function signatures (harder than it looks)
- **Action taken**: No split required. With lesson 071 now split into 071a/071b, learner will have proper proc macro foundation. validate_positive difficulty remains a concern -- consider providing syn parsing hints when lesson is started

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed under relaxed threshold
- Two attribute macros plus studying real-world macros is heavy but within the 2hr limit

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-110 min (Heavy)
- **Needs split**: No
- **Issues**: Exercise 3 (#[validate_positive]) requires parsing syn::ItemFn inputs -- harder than it appears. Provide parsing hints/skeleton. Consider reordering so lighter Exercise 4 comes last.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-110 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 3 (#[validate_positive]) requires parsing syn::ItemFn inputs — syn API more complex than it appears. Parsing hints/skeleton needed. Three heavy in a row (070, 071b, 072). Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match with CLAUDE.md
- **Time estimate**: 80-110 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Third heavy lesson in a row after 070 and 071b; learner fatigue risk
- **Unresolved from prior reviews**: Exercise 3 (#[validate_positive]) needs syn parsing hints for ItemFn signature inspection. Flagged since v4, still unresolved.
- **New findings**: None
- **Recommendation**: Add syn::ItemFn parsing skeleton/hints to Exercise 3 before teaching

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-100min (Heavy)
- **Needs split**: No
- **Progression**: Third heavy lesson in a row (070, 071b, 072) — fatigue risk
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 3 needs `syn::ItemFn` parsing hints/skeleton
- **Recommendation**: Add `syn::ItemFn` parsing hints/skeleton to Exercise 3 before lesson start. Monitor learner fatigue given three heavy lessons in a row.

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-110min
- **Pacing**: Heavy
- **Issues**: Ex 3 (#[validate_positive]) needs syn::ItemFn parsing skeleton. UNRESOLVED since v4 across 7+ review rounds.
- **Recommendations**: MUST add syn::ItemFn parsing skeleton showing FnArg extraction
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Added syn::ItemFn parsing scaffold (starter code) to Exercise 3 (#[validate_positive]) in task-072.md
- Scaffold demonstrates: parsing ItemFn, extracting signature details, iterating FnArg/PatType/Pat::Ident, generating runtime checks with quote!, and reconstructing the function
- Added note directing learner to refine the scaffold to only check numeric parameter types
- **Resolves** issue flagged since v4 (7+ review rounds) requesting syn parsing hints/skeleton

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-95min. **Pacing**: Heavy. **Issues**: Fourth heavy lesson in 070-072 run, mitigated by 071b STRETCH deferral. **Changes**: Changelog only.
