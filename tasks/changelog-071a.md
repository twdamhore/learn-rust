# Changelog - Lesson 071a: Procedural Macros - Part A: Setup and Derive Macros
## Section 15: Macros

### v1 - Created from split (2026-03-03)
- Split from original lesson 071 which was rated OVERLOADED (~2-3 hrs)
- **Reason for split**: Setting up a proc macro crate for the first time (separate crate, Cargo.toml with proc-macro = true, proc_macro2/quote/syn dependencies) is itself time-consuming. The original lesson had 4 exercises each requiring multi-crate setup, which was untenable in any single session. Most overloaded lesson in the 061-080 range
- **Scope**: Proc macro vs declarative macro, proc macro crate setup, HelloMacro derive, FieldNames derive, TokenStream fundamentals
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~70-90 min (Moderate-Heavy)
- **Needs split**: No
- **Issues**: First-time proc macro crate setup can take 20-30 min. Provide step-by-step setup checklist.
- **Changes made**: None (scaffolding deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~70-90 min
- **Pacing**: Good to Heavy
- **Needs split**: No
- **Issues**: First-time proc macro crate setup (separate crate, Cargo.toml with proc-macro=true, proc_macro2/syn/quote dependencies, workspace config) can take 20-30 min. Step-by-step setup checklist essential. Two exercises (HelloMacro, FieldNames) is right scope.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Correct (proc macro crate setup + two derive exercises)
- **Time estimate**: 70-90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: First-time proc macro crate setup can take 20-30 min; step-by-step checklist essential
- **Unresolved from prior reviews**: None
- **New findings**: Minor: setup checklist for proc macro crate (separate crate, Cargo.toml with proc-macro=true, workspace config) should be baked into task file before teaching
- **Recommendation**: Add step-by-step proc macro crate setup checklist to task file at lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-90min (Heavy)
- **Needs split**: No
- **Progression**: First-time proc macro crate setup is the bottleneck
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Step-by-step proc macro crate setup checklist is essential and missing from task file
- **Recommendation**: Add proc macro crate setup checklist (separate crate, Cargo.toml with proc-macro=true, proc_macro2/syn/quote deps, workspace config) to task file before lesson start

### v11-fix - Added proc macro crate setup checklist (2026-03-04)
- Added 7-step setup checklist for proc macro crate workspace
- **Why**: Proc macro crate configuration is error-prone; step-by-step prevents 30+ min of trial and error
- **Resolves**: Genuinely unresolved item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Heavy
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-90min
- **Pacing**: Heavy
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-90min. **Pacing**: Heavy. **Issues**: None — setup checklist and 2-exercise scope well-calibrated. **Changes**: Changelog only.
