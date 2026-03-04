# Changelog - Lesson 084: Exposing Rust to C (cdylib, cbindgen)
## Section 16: Unsafe & FFI

### v1 - Created from split (2026-03-03)
- Split from original lesson 084 which was rated OVERLOADED (~2-3 hrs)
- **Reason for split**: Three distinct tool ecosystems (cdylib, cbindgen, PyO3/maturin) each with significant setup overhead. PyO3+maturin setup alone takes 20+ minutes and Python installation is an unstated prerequisite. Separating C and Python FFI gives each ecosystem proper coverage
- **Scope**: Building cdylib, extern "C" with #[no_mangle], cbindgen header generation, calling Rust from C, string FFI boundary handling
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~70-90 min (Moderate-Heavy)
- **Needs split**: No
- **Issues**: Exercise 2 requires C compilation with linker flags -- provide step-by-step gcc instructions for learner with no C background.
- **Changes made**: None (scaffolding deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~70-90 min
- **Pacing**: Good to Heavy
- **Needs split**: No
- **Issues**: Exercise 2 requires compiling C code with correct linker flags. For non-C background, step-by-step gcc instructions essential.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Correct (cdylib + cbindgen + C caller)
- **Time estimate**: 70-90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Heavy; C compilation step is unfamiliar for non-C background
- **Unresolved from prior reviews**: Needs gcc compilation instructions and Prerequisites section (build-essential). Exercise 2 requires linker flags the learner has never seen. Flagged since v2, still unresolved.
- **New findings**: None
- **Recommendation**: Add Prerequisites section (sudo apt install build-essential) and step-by-step gcc compilation instructions to task file before teaching

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-100min (Heavy)
- **Needs split**: No
- **Progression**: Heavy but manageable C-focused FFI lesson
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 2 needs explicit gcc compilation command with linker flags (`-L`, `-l`, `-Wl,-rpath`).
- **Recommendation**: Add explicit gcc compilation command with linker flags to Exercise 2 before teaching

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-100min
- **Pacing**: Heavy
- **Issues**: Ex 2 needs explicit gcc compilation command with linker flags. UNRESOLVED.
- **Recommendations**: MUST provide gcc command: `gcc -o main main.c -L target/release -l my_math_lib -Wl,-rpath,./target/release`
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Added explicit gcc compilation commands to Exercise 2 (cbindgen header generation) in task-084.md
- Commands cover: `cargo build --release`, `gcc` with `-L`, `-l`, and `-Wl,-rpath` flags, and running the binary
- Added note explaining crate name substitution (hyphens to underscores)
- **Resolves** issue flagged since v2 (6+ review rounds) requesting step-by-step gcc compilation instructions with linker flags

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
- **Pacing**: Good
- **Issues**: Missing 'cargo install cbindgen' in prerequisites section
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 60-80min
- **Pacing**: Moderate
- **Issues**: Added `cargo install cbindgen` to prerequisites (was missing)
- **Changes made**: Added cbindgen installation command to Prerequisites section in task file

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 65-80min. **Pacing**: Moderate. **Issues**: None — prerequisites and gcc commands in place. **Changes**: Changelog only.

### v16 (2026-03-04) — Full curriculum review (119 lessons)
- No changes needed — reviewed for pacing, progression, and forward references

### v17 (2026-03-04) — Human-learning clarity pass
- Expanded prerequisites to include Linux/macOS/Windows setup paths instead of Linux-only commands.
- Added platform note for compilation tools (`clang` on macOS, `cl.exe`/WSL option on Windows).
