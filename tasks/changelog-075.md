# Changelog - Lesson 075: FFI - calling C from Rust (extern C, bindgen)

## Section 16: Unsafe & FFI

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: extern "C" for foreign function declarations, linking C libraries, bindgen for auto-generating bindings, C-compatible types (CString/CStr/c_int), unsafe FFI boundary
- **Exercises added**: Call libc abs/sqrt/strlen, bindgen with custom C header, safe wrapper for getenv, C string conversion patterns module

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Requires system-level tooling (C compiler, libclang for bindgen)
  - Setup steps could eat into lesson time significantly
- **Recommendations**:
  - Note prerequisite installations clearly at the top of the lesson

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Requires system-level tooling (C compiler, libclang for bindgen). Setup could consume 15-20 min. bindgen exercise requires writing C header + configuring build.rs.
- **Why**: System tooling prerequisites not documented.
- **v4 recommendations status**: Not yet applied -- v4 recommended noting prerequisites clearly. Gradual progression: Heavy; setup overhead significant.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - System tooling prerequisites (C compiler, libclang for bindgen) not documented
  - Setup can take 15-20 min
- **Action taken**: No split required. Previous v4 recommendation to document prerequisites clearly at the top should be applied when lesson is started

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed under relaxed threshold
- System tooling prerequisites (C compiler, libclang) still flagged -- learner has no C background so setup overhead remains a concern

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-110 min (Heavy)
- **Needs split**: No
- **Issues**: Prerequisites (C compiler, libclang for bindgen) not documented in task file (flagged since v4). Learner has no C background. Add: "sudo apt install libclang-dev".
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-110 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Requires C compiler (gcc), libclang for bindgen. System prerequisites MUST be documented (sudo apt install libclang-dev build-essential). Exercise 2 (bindgen with custom C header + build.rs) has significant setup overhead. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match with CLAUDE.md
- **Time estimate**: 80-110 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Heavy; system tooling setup can consume 15-20 min
- **Unresolved from prior reviews**: System prerequisites (libclang-dev, build-essential) not documented in task file. Must add Prerequisites section with `sudo apt install libclang-dev build-essential`. Flagged since v4, still unresolved.
- **New findings**: None
- **Recommendation**: Add Prerequisites section to task file with system package install commands before teaching

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy, borderline)
- **Needs split**: No
- **Progression**: Heavy but within threshold
- **Changelog reconciliation**: "System prerequisites missing" -- Prerequisites section with `sudo apt install libclang-dev build-essential` has been added. Resolved.
- **Genuinely unresolved**: Exercise 2 bindgen needs template build.rs and Cargo.toml snippet.
- **Recommendation**: Provide template build.rs and Cargo.toml snippet for Exercise 2 before teaching

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy
- **Issues**: Ex 2 needs template build.rs and Cargo.toml snippet for bindgen. UNRESOLVED.
- **Recommendations**: MUST provide build.rs template
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Added starter build.rs template to Exercise 2 (bindgen basics) in task-075.md
- Added Cargo.toml `[build-dependencies]` snippet showing `bindgen = "0.69"`
- Added `include!` macro usage for main.rs/lib.rs to consume generated bindings
- **Resolves** issue flagged since v11 requesting template build.rs and Cargo.toml snippet for bindgen exercise

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-110min
- **Pacing**: Heavy
- **Issues**: build.rs not formally taught anywhere in curriculum — this is first encounter. System dependency setup (libclang-dev) adds friction. Consider adding build.rs primer to objectives and making Exercise 4 (C string conversions) STRETCH
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 90-110min
- **Pacing**: Heavy
- **Issues**: Added build.rs explanation (first encounter in curriculum) and marked Exercise 4 (C string conversions) as STRETCH to keep core content within time budget
- **Changes made**: Added build.rs primer note before first mention; marked Exercise 4 as [STRETCH] in task file

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 90-105min. **Pacing**: Heavy. **Changes**: Added explanatory comment for cargo:rerun-if-changed directive in build.rs primer. **Why**: First encounter with build scripts; the directive communication protocol should be explained.
