# Changelog - Lesson 011: Memory in Rust vs Java/Go - why no GC, RAII, the mental model shift

## Section 3: Ownership System

### v1 - Initial creation
- Lesson added to curriculum
- **NEW**: Bridging lesson added after gap analysis

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and bridging lesson tag all align with curriculum
- Correctly tagged as [NEW - bridging lesson] matching CLAUDE.md [NEW] designation
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Why no GC (Java/Go contrast), RAII and Drop trait, stack vs heap mental model, compile-time safety guarantees (use-after-free/double-free), drop ordering rules
- **Exercises added**: Memory model diagram (Java vs Rust), RAII file handling + custom Drop impl, drop order exploration with named structs, compile-time safety comparison (move vs GC vs copy)

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 2 uses `impl Drop for X` -- trait implementation syntax not taught until lesson 40
  - Exercise 2 uses `std::fs::File::create` which returns `Result`, not taught until lesson 30
  - Conceptually dense: entire mental model shift from GC to ownership in one lesson
- **Recommendations**:
  - Provide verbatim code for the Drop implementation and File handling since syntax is not yet taught
  - Frame as guided demonstration rather than independent coding

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5+ hr) for 1-2 hour target
- **Changes noted**: CRITICAL forward dependencies -- uses impl Drop for X (lesson 40 concept) and std::fs::File::create returning Result (lesson 30). Conceptually dense -- entire GC-to-ownership mental model shift.
- **Why**: Bridging lesson for Java/Go devs needs to work within current knowledge; forward references undermine learning.
- **v4 recommendations status**: Not yet applied -- v4 recommended verbatim code and guided demonstration framing. Gradual progression: Necessary lesson but exercises outrun taught concepts.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hr
- **Pacing verdict**: Heavy borderline
- **Split needed**: No
- **Key issues**:
  - CRITICAL forward dependencies on impl Drop (lesson 40) and File/Result (lesson 30)
  - Conceptually dense -- entire mental model shift from GC to ownership
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- CRITICAL forward dependencies (impl Drop, Result) still flagged but borderline acceptable

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-120 min (Heavy borderline)
- **Needs split**: No
- **Progression**: Critical mental model shift for Java/Go developers. Conceptually dense but essential.
- **Issues**: Exercise 2 uses impl Drop (lesson 40) and File::create returning Result (lesson 30) without scaffolding (flagged since v4, unresolved). Should be framed as guided demonstration with verbatim code provided.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-120 min
- **Pacing**: Heavy (borderline)
- **Needs split**: No
- **Issues**: CRITICAL: Exercise 2 uses `impl Drop for X` (trait impl not taught until lesson 40) and `std::fs::File::create` (returns Result, lesson 30). Must provide verbatim scaffolding code. Unresolved since v4.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Aligned with CLAUDE.md Section 3 (Ownership System)
- **Time estimate**: 90-120 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Ownership section starts here -- hardest stretch for Java/Go devs. Conceptually dense but essential bridge lesson.
- **Unresolved from prior reviews**: CRITICAL forward deps -- Exercise 2 uses `impl Drop` (lesson 40) and `File::create` returning `Result` (lesson 30). Must provide verbatim scaffolding code. Flagged since v4.
- **New findings**: None beyond prior reviews
- **Recommendation**: Before teaching, add verbatim scaffolding code for Drop impl and File handling so learner copies rather than writes from scratch

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy-Borderline)
- **Needs split**: No
- **Progression**: Forward dependency on Result (`File::create`) needs explicit `.expect()` scaffolding — genuinely unresolved. Drop template is adequate. Bridging lesson placement excellent.
- **Changelog reconciliation**: All prior findings consistent — no stale flags
- **Genuinely unresolved**: Forward dependency on Result (`File::create`) needs explicit `.expect()` scaffolding added to the task file
- **Recommendation**: No split needed. Add `.expect()` scaffolding for `File::create` before teaching.

### v11-fix - Added File::create scaffolding with .expect() (2026-03-04)
- Added inline code showing .expect() for Result handling in Exercise 2
- **Why**: Result type not taught until lesson 29; learner needs concrete pattern to follow
- **Resolves**: Genuinely unresolved item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy
- **Issues**: Conceptually dense memory model shift; right at 2hr boundary
- **Recommendations**: Add note suggesting learner read all objectives first, then exercises
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Heavy
- **Issues**: Drop impl exercise uses trait syntax not taught until lesson 40; templates provided but still heavy. Drop order exploration with Vec could be simplified
- **Changes made**: Changelog updated only

### v13-fix - Applied pending task file fixes (2026-03-04)
- Added "read objectives first" tip above exercises section
- **Why**: Memory model concepts need to be internalized before hands-on exercises make sense
- **Resolves**: v12 and v13 recommendation

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-100min
- **Pacing**: Heavy
- **Issues**: Minor Exercise 3 efficiency concern (low priority, not fixed)
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 75-100min
- **Pacing**: Heavy
- **Changes made**: Simplified Exercise 3 to reuse MyStruct template from Exercise 2 with three instances instead of requiring three new struct types (reduces boilerplate)
- **Why**: Exercise 3 duplicated Exercise 2's Drop exploration with unnecessary boilerplate
