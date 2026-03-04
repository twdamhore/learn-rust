# Changelog - Lesson 096: Project 1 - continued (testing, publishing)

## Section 21: Capstone Projects

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Comprehensive unit tests for all modules, integration tests with assert_cmd, documentation with doc-tested examples, GitHub Actions CI workflow, CLI polish with progress indicators and colored output
- **Exercises added**: Unit tests for config module with tempfile, integration tests with assert_cmd for end-to-end CLI behavior, doc comments with tested examples and cargo doc, GitHub Actions CI workflow file

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Introduces 5 new crates never previously taught (assert_cmd, predicates, tempfile, indicatif, colored)
  - Objective 5 (CLI polish with indicatif/colored) has no corresponding exercise
  - Exercise 4 (CI workflow) overlaps with lesson 085
  - Curriculum title says 'publishing' but no exercise covers actual `cargo publish`
  - Exercise format uses unnumbered bullets (formatting inconsistency)
- **Recommendations**:
  - Add exercise for Objective 5 or remove the objective
  - Reference lesson 085 CI workflow rather than duplicating
  - Add a publish preparation exercise to match curriculum title
  - Standardize exercise format

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: Introduces 5 new crates never taught (assert_cmd, predicates, tempfile, indicatif, colored). "Publishing" in title but no exercise covers cargo publish. Objective 5 (CLI polish) has no exercise. CI exercise overlaps lesson 085. Exercise format inconsistency.
- **Why**: Too many new crates; title doesn't match content.
- **v4 recommendations status**: Not yet applied -- v4 flagged all issues. Gradual progression: Heavy continuation.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hours
- **Pacing verdict**: Heavy - borderline under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Introduces 5 untaught crates (assert_cmd, predicates, tempfile, indicatif, colored)
  - Objective 5 (CLI polish) has no corresponding exercise
  - Title says "publishing" but no exercise covers cargo publish
  - CI exercise overlaps lesson 085
- **Action taken**: No split needed. Issues should be addressed when task content is updated: add exercise for Objective 5 or remove it, add publish preparation exercise to match title, reference lesson 085 for CI instead of duplicating.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- Within relaxed threshold. 5 untaught crates and CI overlap with lesson 085 still flagged.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-110 min (Heavy)
- **Needs split**: No
- **Issues (CRITICAL accumulation)**:
  1. Exercise references are STALE -- mention "config module" and "filter syntax" removed in 095 split
  2. Five untaught crates (assert_cmd, predicates, tempfile, indicatif, colored) need intro notes
  3. Title says "publishing" but no exercise covers cargo publish
  4. Objective 5 (CLI polish) has no exercise
  5. Exercise 4 (CI workflow) substantially overlaps lesson 085
- **Changes made**: None (content fixes deferred to lesson start -- HIGH PRIORITY)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-110 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: CRITICAL: Exercise references are STALE — mention "config module" and "filter syntax" removed in 095 split. Must update to match simplified text-processing project. Also: Introduces 5 untaught crates (assert_cmd, predicates, tempfile, indicatif, colored) — need intro notes. Title says "publishing" but no exercise covers cargo publish. Objective 5 (CLI polish with indicatif/colored) has no exercise. Exercise 4 (CI workflow) overlaps lesson 85. Highest accumulation of unresolved issues in 081-100. Unresolved since v4/v8.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Partial match -- multiple stale references and content gaps
- **Time estimate**: 90-110 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Most accumulated issues in 091-100 range. Requires significant content fixes before execution.
- **Unresolved from prior reviews**: (1) Stale exercise references to "config module" and "filter syntax" removed in 095 split, (2) Title says "publishing" but no cargo publish exercise, (3) 5 untaught crates introduced without notes, (4) Objective 5 has no exercise, (5) CI exercise overlaps lesson 085. All flagged since v4/v8.
- **New findings**: None -- all issues previously identified but remain unresolved
- **Recommendation**: HIGH PRIORITY content fix needed before lesson execution. Update exercise references to match 095a/095b text-processing project.

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 100-120min (Heavy)
- **Needs split**: No
- **Progression**: Capstone testing and publishing continuation. Requires significant content fixes before execution.
- **Changelog reconciliation**: All prior findings consistent. Stale references confirmed still present.
- **Genuinely unresolved**: **HIGHEST PRIORITY** genuinely unresolved: Stale references to "config module" and "CSV processing" from pre-split 095. Exercises must be updated to match text-processing project from 095a/095b. Also: 5 untaught crates (assert_cmd, predicates, tempfile, indicatif, colored) need intro notes. CI exercise overlaps lesson 085.
- **Recommendation**: HIGH PRIORITY — update exercise references to match 095a/095b text-processing project, add intro notes for 5 untaught crates, differentiate CI exercise from lesson 085

### v11-fix - Fixed stale references and added crate introductions (2026-03-04)
- Updated all exercise references from CSV/config to text-processing project matching 095a/095b
- Added brief intro notes for assert_cmd, predicates, tempfile, indicatif, colored
- Added differentiation note for CI exercise vs lesson 085
- **Why**: Exercises referenced project structure that no longer exists after 095 split
- **Resolves**: HIGHEST PRIORITY item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 100-120min
- **Pacing**: Heavy
- **Issues**: (1) 5 exercises is a lot. (2) Objective 5 (CLI polish with indicatif/colored) has no dedicated exercise.
- **Recommendations**: Make Ex 5 (dry-run publish) or Ex 4 (CI) stretch; either add CLI polish exercise or remove Objective 5
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing review and split (2026-03-04)
- Reviewed all 100+ tasks for realistic human pacing (1-2hr OK, split if >2hr)
- **Estimated time**: ~2-2.5 hours
- **Decision**: SPLIT into task-096a.md and task-096b.md
- **Rationale**: 5 exercises (most of any lesson), introduces 5 new crates, rated Heavy since v4. Testing (unit + integration) is distinct from documentation/CI/publishing. 12 prior reviews flagged accumulated issues.
- **096a covers**: Unit tests + integration tests with assert_cmd (2 exercises, crates: assert_cmd, predicates, tempfile)
- **096b covers**: Documentation, CI workflow, dry-run publish (3 exercises, crates: indicatif, colored)
- **Key improvement**: Testing separated from polish/publishing; new crate introductions split across the two parts
- **Status**: SUPERSEDED -- see task-096a.md and task-096b.md

### v13-review - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 096a/096b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
