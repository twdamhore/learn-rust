# Changelog - Lesson 076: FFI - exposing Rust to C/Python, cbindgen, PyO3

## Section 16: Unsafe & FFI

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: #[no_mangle] and extern "C" for exporting, cbindgen for C header generation, PyO3 for Python bindings, FFI memory ownership rules
- **Exercises added**: Export Rust functions as cdylib, generate C header with cbindgen, PyO3 Python module with fibonacci and Counter, FFI memory ownership with into_raw/from_raw

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Overloaded for 1-hour lesson
- **Issues found**:
  - Three distinct ecosystems (cdylib, cbindgen, PyO3) with significant setup overhead
  - PyO3 + maturin setup alone can take 20+ minutes
  - **Too much content for 1 hour**
- **Recommendations**:
  - Make PyO3 exercise a stretch goal or separate exploration
  - Focus core lesson on cdylib + cbindgen only

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: OVERLOADED (~2-3 hr) for 1-2 hour target
- **Changes noted**: Three distinct ecosystems (cdylib, cbindgen, PyO3/maturin) each with significant setup. PyO3 + maturin setup alone can take 20+ min. Python installation and maturin are prerequisites not mentioned.
- **Why**: Three tool ecosystems in one hour is not feasible.
- **v4 recommendations status**: Not yet applied -- v4 recommended making PyO3 a stretch goal. Gradual progression: CRITICAL -- second overloaded lesson after 071.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~2-3 hours
- **Pacing verdict**: OVERLOADED - split required
- **Split needed**: Yes - split into 076a/076b
- **Key issues**:
  - Three distinct tool ecosystems (cdylib, cbindgen, PyO3/maturin) each with significant setup overhead
  - PyO3+maturin setup alone takes 20+ min
  - Python installation is an unstated prerequisite
- **Action taken**: Split into two lessons:
  - **076a**: "FFI - Part A: Exposing Rust to C (cdylib, cbindgen)" -- cdylib build, extern "C" with #[no_mangle], cbindgen header generation, C caller, string FFI
  - **076b**: "FFI - Part B: Exposing Rust to Python (PyO3)" -- PyO3+maturin setup, exposing functions and structs to Python, performance comparison
  - Original task-076.md preserved as-is for reference; new task-076a.md and task-076b.md created

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: N/A (already split in v6)
- **Status**: No changes needed
- The v6 split into 076a/076b was already the right call -- no additional changes needed under relaxed threshold

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 076a/076b at v6. Original was ~2.5-3 hrs.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~150-180 min
- **Pacing**: OVERLOADED
- **Needs split**: No (already split into 076a/076b)
- **Issues**: Three tool ecosystems (cdylib, cbindgen, PyO3/maturin) in one lesson was untenable.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 076a/076b
- **Time estimate**: 150-180 minutes (Overloaded)
- **Needs splitting**: No (already split into 076a/076b at v6)
- **Pacing context**: Original was 2.5-3 hours; correctly split
- **Unresolved from prior reviews**: None (split resolved the overload)
- **New findings**: None
- **Recommendation**: No action on this file; see 076a and 076b changelogs

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: SUPERSEDED by 076a/076b
- **Needs split**: No (already split)
- **Progression**: SUPERSEDED by 076a/076b. Split at v6 was correct.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None (see 076a/076b)
- **Recommendation**: No action on this file; see 076a and 076b changelogs

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 076a/076b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 076a/076b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded by 076a/076b. **Changes**: Changelog only.
