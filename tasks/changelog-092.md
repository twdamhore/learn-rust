# Changelog - Lesson 092: WebAssembly - wasm-pack, wasm-bindgen, browser integration

## Section 20: Special Targets

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: wasm-pack toolchain setup, wasm-bindgen for JS interop, data types across WASM boundary, browser deployment, WASM limitations and web-sys/js-sys bridges
- **Exercises added**: GCD function compiled to WASM called from JS, Markdown-to-HTML struct across WASM boundary, interactive Caesar cipher web page, Vec sorting benchmark comparing WASM vs native JS

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Overloaded for 1-hour lesson
- **Issues found**:
  - Requires JavaScript and HTML knowledge, a browser environment, and a local HTTP server -- outside Rust scope
  - Exercise 3 (interactive Caesar cipher web page) is a full-stack web development exercise
  - Exercise 2 (markdown parser) is non-trivial implementation on its own
  - Exercise format uses unnumbered bullets (formatting inconsistency)
  - **Likely exceeds 1 hour**
- **Recommendations**:
  - Simplify exercises to focus on Rust-to-WASM compilation and basic JS interop
  - Make Exercise 3 (interactive web page) and Exercise 4 (benchmark) optional
  - Standardize exercise format

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: OVERLOADED (~2-3 hr) for 1-2 hour target
- **Changes noted**: Requires JS/HTML knowledge, browser environment, and local HTTP server -- all outside Rust scope. Exercise 3 (interactive web page) is full-stack web development. Exercise 2 (markdown parser) is non-trivial on its own. Toolchain setup (wasm-pack, wasm32 target) adds overhead. Most overloaded in Section 20.
- **Why**: Three exercises require non-Rust skills not taught in curriculum.
- **v4 recommendations status**: Not yet applied -- v4 recommended simplifying to Rust-to-WASM focus and making Exercises 3-4 optional. Gradual progression: CRITICAL -- requires skills outside curriculum scope.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~2.5-3.5 hours
- **Pacing verdict**: OVERLOADED - split required
- **Split needed**: Yes - split into 092a/092b
- **Key issues**:
  - Requires JavaScript/HTML/browser knowledge outside curriculum scope
  - Toolchain setup (wasm-pack, wasm32 target) is significant overhead
  - Exercise 2 (markdown parser) is non-trivial on its own
  - Exercise 3 (interactive web page) is full-stack development
  - Most overloaded lesson in Section 20
- **Action taken**: Split into task-092a.md (Rust to WASM Basics -- toolchain, build, test from Rust side) and task-092b.md (Browser Integration -- wasm-bindgen, JS interop, HTML UI). Exercises requiring deep JS/HTML knowledge simplified in 092b. Each part is now ~1-1.5 hours.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Already split in v6 into 092a/092b
- **Status**: No changes needed
- Prior split was adequate under relaxed threshold; no additional changes required

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 092a/092b at v6. Original was ~150-210 min.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~150-210 min
- **Pacing**: OVERLOADED
- **Needs split**: Already split into 092a/092b
- **Issues**: Original required JS/HTML/browser knowledge outside curriculum scope.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 092a/092b
- **Time estimate**: 150-210 minutes (Overloaded -- original)
- **Needs splitting**: Already split into 092a/092b at v6
- **Pacing context**: Original required JS/HTML/browser knowledge outside curriculum scope. Split was correct and well-executed.
- **Unresolved from prior reviews**: None (issues resolved by split)
- **New findings**: None
- **Recommendation**: No action needed on original; see 092a and 092b changelogs

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: N/A (SUPERSEDED)
- **Needs split**: N/A
- **Progression**: SUPERSEDED by 092a/092b. Split was correct (Rust-side WASM vs browser integration).
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No action needed on original; see 092a and 092b changelogs

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 092a/092b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 092a/092b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
