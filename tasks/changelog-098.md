# Changelog - Lesson 098: Logging and tracing - log, tracing, structured logging

## Section 19: Ecosystem & Tooling

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: log crate with env_logger, tracing with structured fields and spans, #[instrument] and hierarchical context, RUST_LOG filtering by module, JSON structured logging for production
- **Exercises added**: Multi-module log+env_logger app, tracing spans and structured events, EnvFilter with layered subscribers, JSON formatted output compared to Go's slog/zap

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate-to-Heavy for 1-hour lesson
- **Issues found**:
  - Covers 5 crates total (log, env_logger, tracing, tracing-subscriber, tracing-appender)
  - Exercise 3 introduces tracing_appender -- not mentioned in objectives
- **Recommendations**:
  - Add tracing-appender to objectives or simplify Exercise 3

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate-to-Heavy (~1-1.25 hr) for 1-2 hour target
- **Changes noted**: Covers 5 crates (log, env_logger, tracing, tracing-subscriber, tracing-appender). Exercise 3 uses tracing_appender not mentioned in objectives. Concepts translate from Java/Go logging.
- **Why**: Many crates but familiar concepts
- **v4 recommendations status**: Not yet applied -- v4 flagged tracing_appender gap. Gradual progression: Manageable.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1-1.25 hours
- **Pacing verdict**: Moderate - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - tracing_appender used in Exercise 3 but not covered in objectives
- **Action taken**: No changes needed. Minor gap (tracing_appender) should be addressed when task content is updated. Concepts translate from Java/Go logging experience.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~1-1.25 hr)
- **Status**: No changes needed

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~70-80 min (Moderate)
- **Needs split**: No
- **Issues**: Exercise 3 uses tracing_appender not covered in objectives (flagged since v4). Either add objective or simplify exercise.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~70-80 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercise 3 uses tracing_appender not covered in any objective. Either add objective or simplify exercise. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 70-80 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Logging concepts transfer well from Java/Go (slog, zap, logback).
- **Unresolved from prior reviews**: Exercise 3 uses tracing_appender not mentioned in any objective — add objective or simplify exercise
- **New findings**: None
- **Recommendation**: Either add tracing_appender to objectives or simplify Exercise 3 before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 70-90min (Moderate)
- **Needs split**: No
- **Progression**: Logging concepts transfer well from Java/Go. Well-paced within section.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Minor: Exercise 3 uses tracing_appender not covered in objectives — add one objective line or simplify exercise
- **Recommendation**: Add tracing_appender to objectives or simplify Exercise 3 before lesson start

### v11-fix - Added tracing_appender to objectives (2026-03-04)
- Exercise 3 uses tracing_appender; now reflected in objectives
- **Resolves**: Minor item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: 6 objectives and 4 exercises covering 5+ crates is dense. Exercise 4 (JSON structured logging) should be marked STRETCH to bring core content under 90min
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: Exercise 4 (JSON structured logging) too dense for core content
- **Changes made**: Marked Exercise 4 STRETCH, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-95min. **Pacing**: Heavy. **Issues**: Six objectives dense but mitigated by Java/Go transfer and STRETCH on Ex 4. **Changes**: Changelog only.
