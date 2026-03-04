# Changelog - Lesson 079: Function-Like and Advanced Derive
## Section 15: Macros

### v1 - Created from split (2026-03-03)
- Split from original lesson 078 which was rated OVERLOADED (~2-3 hrs)
- **Reason for split**: Function-like proc macros with custom parsing and the Builder derive macro each require significant time. The Builder derive alone is a mini-project. With the proc macro crate setup already learned in 078, this lesson can focus on more advanced patterns
- **Scope**: Function-like proc macros, custom syntax parsing with syn, error handling in proc macros, Builder derive macro as a guided exercise
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-110 min (Heavy)
- **Needs split**: No
- **Issues**: Exercise 2 (Builder derive) MUST provide the guided architecture in detail -- not just describe it. Without scaffolding this becomes a 2+ hour exercise.
- **Changes made**: None (scaffolding deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-110 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: CRITICAL issue: Exercise 2 (Builder derive) described as "guided" but task file does not include the actual guided architecture. Without scaffolding, this exercise alone exceeds 2 hours. Exercise 1 (make_struct! with custom syn::parse::Parse) introduces custom parsing.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Correct (function-like proc macro + Builder derive)
- **Time estimate**: 80-110 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Heavy but within 2hr limit; depends on 078 foundation
- **Unresolved from prior reviews**: CRITICAL: Exercise 2 (Builder derive) described as "guided" but task file contains NO scaffolding -- no step-by-step architecture, no struct outline, no field iteration hints. Without this, exercise alone exceeds 2 hours. Flagged since v2, still unresolved.
- **New findings**: None beyond confirming prior critical issue persists
- **Recommendation**: Must add step-by-step Builder derive architecture (struct parsing, field iteration, quote! template) to task file before teaching

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 100-110min (Heavy)
- **Needs split**: No
- **Progression**: Depends on 078 foundation; heavy but within 2hr threshold if scaffolding provided
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: **CRITICAL** — Exercise 2 (Builder derive) described as "guided" but contains NO scaffolding — no step-by-step architecture, no struct outline, no field iteration hints. Must be provided before teaching.
- **Recommendation**: Add complete Builder derive scaffolding (struct parsing, field iteration, quote! template, step-by-step architecture) to task file before lesson start — this is a blocking prerequisite

### v11-fix - Applied Builder derive macro scaffolding (2026-03-04)
- Added step-by-step architecture guide and starter code skeleton to Exercise 2
- **Why**: Builder derive requires parsing fields, generating builder struct, setters, and build() — too much to design from scratch
- **Resolves**: CRITICAL item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy
- **Issues**: At upper boundary of 2hr; custom syn::parse::Parse may push over
- **Recommendations**: Consider providing minimal Parse example as additional scaffolding
- **Changes made**: Changelog updated only

### v13-fix - Applied pending fixes (2026-03-04)
- Added minimal `syn::parse::Parse` example to Exercise 1 (make_struct!)
- **Why**: Custom Parse implementation is a new pattern; a concrete example reduces friction
- **Resolves**: v12 recommendation (high priority)

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-80min (required), up to 120min with STRETCH
- **Pacing**: Good (was OVERLOADED before change)
- **Issues**: Builder derive macro combined with make_struct! exceeded 2hr threshold. Builder is a mini-project even with scaffold (inspired by dtolnay proc-macro-workshop)
- **Changes made**: Marked Builder derive exercise as [STRETCH] with 90-minute time check note — brings required content to ~60-80min

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 60-80min core (Heavy with STRETCH)
- **Pacing**: Heavy with STRETCH
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 60-80min core. **Pacing**: Medium (up to 120 with STRETCH). **Changes**: Added hint to Exercise 1 showing how quote! generates derive attributes. **Why**: Generating attributes in quote! is a non-obvious pattern not demonstrated in 078.
