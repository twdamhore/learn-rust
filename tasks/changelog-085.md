# Changelog - Lesson 085: Exposing Rust to Python (PyO3)
## Section 16: Unsafe & FFI

### v1 - Created from split (2026-03-03)
- Split from original lesson 084 which was rated OVERLOADED (~2-3 hrs)
- **Reason for split**: PyO3+maturin is an entirely separate ecosystem from cdylib/cbindgen with its own significant setup overhead (20+ min). Python 3 and pip are prerequisites. Giving PyO3 its own lesson ensures proper coverage of #[pyfunction], #[pyclass], and #[pymethods] without rushing
- **Scope**: PyO3+maturin setup, exposing Rust functions to Python, exposing Rust structs as Python classes, performance comparison
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60-90 min (Moderate)
- **Needs split**: No
- **Issues**: Recommend noting python virtual environment setup (python -m venv .venv).
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~60-90 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Should note python -m venv .venv for virtual environment setup. Prerequisites (Python 3, pip) already noted.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Correct (PyO3 + maturin)
- **Time estimate**: 60-90 minutes (Moderate-Heavy)
- **Needs splitting**: No
- **Pacing context**: Moderate; Prerequisites section already present (good)
- **Unresolved from prior reviews**: None
- **New findings**: Minor: add `python -m venv .venv` note for virtual environment setup to avoid polluting system Python
- **Recommendation**: Add venv setup note to task file before teaching

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 60-80min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Better half of the split. PyO3 well-scoped.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: Minor: add `python -m venv` setup to Prerequisites

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-80min
- **Pacing**: Good
- **Issues**: Minor — add python venv setup note
- **Recommendations**: Add `python -m venv .venv` to Prerequisites
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 60-75min
- **Pacing**: Moderate
- **Issues**: Added python venv setup to prerequisites (avoids polluting system Python)
- **Changes made**: Added virtual environment creation instructions to Prerequisites section in task file

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 60-75min. **Pacing**: Moderate. **Issues**: None — well-scoped with good prerequisites. **Changes**: Changelog only.
