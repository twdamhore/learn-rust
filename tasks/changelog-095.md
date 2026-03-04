# Changelog - Lesson 095: Project 1 - CLI tool (file processor with clap, serde, error handling)

## Section 21: Capstone Projects

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: CLI tool architecture design, clap derive API argument parsing with subcommands, serde config file loading with defaults, file reading and data processing, thiserror/anyhow error handling
- **Exercises added**: Build fileproc CLI tool with CSV processing and TOML config, validate subcommand for schema checking, stats subcommand for numeric column statistics, comprehensive error handling with thiserror and anyhow

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Requires a `csv` crate never mentioned in the curriculum
  - Filter conditions ('age > 30') imply building a mini expression evaluator
  - Exercise format uses unnumbered bullets (formatting inconsistency)
  - Implicitly depends on lessons 086 (serde), 088 (clap), 032 (thiserror/anyhow)
- **Recommendations**:
  - Make csv crate dependency explicit
  - Simplify filter conditions to avoid expression parsing
  - List prerequisite lessons explicitly
  - Standardize exercise format

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~2+ hr) for 1-2 hour target
- **Changes noted**: CSV processor with TOML config, 3 subcommands, filter conditions ("age > 30" implies expression parsing), and error handling is extremely ambitious. csv crate never introduced in curriculum. No prerequisite listing. Exercise format inconsistency.
- **Why**: Filter condition implies mini expression evaluator -- far too complex.
- **v4 recommendations status**: Not yet applied -- v4 flagged csv crate gap, filter complexity, and missing prerequisites. Gradual progression: Heavy capstone start.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~2.5-3.5 hours
- **Pacing verdict**: OVERLOADED - split required
- **Split needed**: Yes - split into 095a/095b
- **Key issues**:
  - csv crate never introduced in curriculum
  - Filter condition "age > 30" implies building a mini expression evaluator
  - 3 subcommands each with substantial logic
  - Prerequisite dependencies not listed
- **Action taken**: Split into task-095a.md (CLI Tool Setup and Core Processing -- project setup, config loading, stats subcommand) and task-095b.md (Processing Pipeline and Validation -- process subcommand, validation, testing). Removed expression-evaluator filter condition. csv crate usage made optional (can work with plain text files). Each part is now ~1-1.5 hours.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Already split in v6 into 095a/095b
- **Status**: No changes needed
- Prior split was adequate under relaxed threshold; no additional changes required

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 095a/095b at v6. Original was ~150-210 min.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~150-210 min
- **Pacing**: OVERLOADED
- **Needs split**: Already split into 095a/095b
- **Issues**: Removed expression-evaluator filter condition, made CSV optional.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 095a/095b
- **Time estimate**: 150-210 minutes (Overloaded -- original)
- **Needs splitting**: Already split into 095a/095b at v6
- **Pacing context**: CSV removed, text files used instead. Expression-evaluator filter condition removed. Split was correct.
- **Unresolved from prior reviews**: None (issues resolved by split)
- **New findings**: None
- **Recommendation**: No action needed on original; see 095a and 095b changelogs

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: N/A (SUPERSEDED)
- **Needs split**: N/A
- **Progression**: SUPERSEDED by 095a/095b. Split was correct. CSV dependency removed, simplified to text.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No action needed on original; see 095a and 095b changelogs

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 095a/095b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 095a/095b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
