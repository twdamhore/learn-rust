# Changelog - Lesson 099: Clap - CLI argument parsing, subcommands, derive API

## Section 19: Ecosystem & Tooling

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Clap derive API with #[derive(Parser)], subcommands with #[derive(Subcommand)], argument types/validation/constraints, help text and shell completions, comparison to Go's cobra/flag
- **Exercises added**: file-stats CLI with flags, task-manager with 4 subcommands and JSON storage, input validation with ValueEnum and conflicts_with, shell completion generation

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 2 (task-manager with 4 subcommands + JSON persistence) is a complete mini-application
  - Exercise 4 (shell completions) involves system-specific installation steps
- **Recommendations**:
  - Scope down Exercise 2 to 2 subcommands
  - Or make Exercise 4 optional

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: Exercise 2 (task-manager with 4 subcommands + JSON persistence) is a complete mini-application. Exercise 4 involves system-specific shell installation steps.
- **Why**: Exercise 2 too large for one exercise
- **v4 recommendations status**: Not yet applied -- v4 recommended scoping Exercise 2 to 2 subcommands or making Exercise 4 optional. Gradual progression: Heavy.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hours
- **Pacing verdict**: Heavy - borderline under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise 2 (task-manager with 4 subcommands + JSON persistence) is a complete mini-app
  - Exercise 4 (shell completions) involves platform-specific steps
- **Action taken**: No split needed. Exercise 2 should be scoped down to 2 subcommands, or Exercise 4 should be marked optional, when task content is updated.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- Within relaxed threshold. Task-manager mini-project still flagged as heavy. Exercise 4 (shell completions) could be optional.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-110 min (Heavy, borderline 2hr)
- **Needs split**: No
- **Issues**: Exercise 2 (4 subcommands + JSON persistence) too large -- scope to 2 subcommands. Exercise 4 (shell completions) should be [STRETCH]. Both flagged since v4, unresolved.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-110 min
- **Pacing**: Heavy
- **Needs split**: No, but needs trimming
- **Issues**: Exercise 2 (task-manager with 4 subcommands + JSON persistence) is a complete mini-app. Should scope to 2 subcommands. Exercise 4 (shell completions with system installation) should be [STRETCH/OPTIONAL]. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90-110 minutes (Heavy)
- **Needs splitting**: No (if trimmed)
- **Pacing context**: Clap concepts transfer from Go's cobra/flag. Heavy but manageable with trimming.
- **Unresolved from prior reviews**: (1) Exercise 2 scope down to 2 subcommands from 4, (2) Exercise 4 shell completions should be [STRETCH]
- **New findings**: None
- **Recommendation**: Scope Exercise 2 to 2 subcommands and mark Exercise 4 [STRETCH] before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy)
- **Needs split**: No
- **Progression**: Clap concepts transfer from Go's cobra/flag. Heavy but manageable with trimming.
- **Changelog reconciliation**: "Exercise 2 has 4 subcommands" — task file only defines 2 (add, list). Prior reviews miscounted. Resolved. Exercise 4 already [STRETCH].
- **Genuinely unresolved**: None
- **Recommendation**: No action needed — Exercise 2 scope and Exercise 4 [STRETCH] already correct in task file

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy
- **Issues**: None. Ex 4 correctly [STRETCH].
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Good
- **Issues**: Exercise 2 requires serde (lesson 86) for JSON persistence but serde is not listed as explicit prerequisite
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-90min
- **Pacing**: Good/Heavy
- **Issues**: Exercise 2 requires serde (lesson 097) for JSON persistence but serde not listed as explicit prerequisite
- **Changes made**: Added serde prerequisite, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-90min. **Pacing**: Good/Heavy. **Issues**: None — serde prerequisite and STRETCH verified. **Changes**: Changelog only.
