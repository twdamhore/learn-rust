# Changelog - Lesson 072: Streams, async iterators, async channels

## Section 14: Async Rust

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Stream trait as async Iterator, tokio-stream utilities, mpsc channels for async producer-consumer, backpressure concepts
- **Exercises added**: Channel-to-stream conversion, stream processing pipeline with filter/map/take, rate-limited consumer with backpressure, multi-producer async pipeline with statistics

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Streams are conceptually dense with tokio-stream as additional dependency
  - Exercise 4 (multi-producer pipeline with statistics) is essentially a mini-project
- **Recommendations**:
  - Simplify Exercise 4 or make it a stretch goal

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: tokio-stream adds dependency complexity. Exercise 4 (3 producers, 1 consumer, statistics) is a mini-project. Backpressure needs experimentation time
- **Why**: Additional crate dependency + mini-project exercise
- **v4 recommendations status**: Not yet applied -- v4 recommended simplifying Exercise 4 or making it stretch. Gradual progression: Heavy continuation

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hours
- **Pacing verdict**: Heavy - borderline 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise 4 (3 producers, merge, statistics) is a mini-project
  - Backpressure needs experimentation time
- **Action taken**: No split required. Previous v4 recommendation to simplify Exercise 4 or make it stretch should be applied when lesson is started

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr borderline)
- **Status**: No changes needed under relaxed threshold
- Exercise 4 (3-producer pipeline) still flagged as heavy but within the 2hr limit

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-110 min (Heavy, borderline 2hr)
- **Needs split**: No
- **Issues**: Exercise 4 (3-producer pipeline) should be marked [STRETCH] (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-110 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 4 (3 producers, 1 consumer, merge, statistics) is a mini-project. Should be marked [STRETCH]. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90-110 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Streams and async channels are conceptually dense. tokio-stream adds dependency complexity. Borderline but under 2hr threshold.
- **Unresolved from prior reviews**: Exercise 4 (3 producers, merge, statistics) should be [STRETCH]. Flagged 6 consecutive times since v4, still unresolved.
- **New findings**: None
- **Recommendation**: Mark Exercise 4 as [STRETCH] when lesson is started -- this is the most-flagged unresolved item in this range

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-100min (Heavy)
- **Needs split**: No
- **Progression**: Streams and async channels are conceptually dense but cohesive
- **Changelog reconciliation**: "Exercise 4 should be [STRETCH]" flagged 6 consecutive times since v4 — already in task file. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No action needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-100min
- **Pacing**: Heavy
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 65-80min
- **Pacing**: Good
- **Issues**: tokio-stream crate introduced without prior mention — add brief setup note for Cargo.toml dependency
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 65-80min
- **Pacing**: Moderate-Heavy
- **Issues**: Added tokio-stream dependency note at top of Exercises section
- **Changes made**: Task file updated — added setup instruction for `cargo add tokio-stream --features sync`

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-85min. **Pacing**: Medium-Heavy. **Changes**: Added stream creation hint (`tokio_stream::iter(1..=100)`) to Exercise 2. **Why**: Learner has no prior stream creation experience and needs the API hint to avoid getting stuck.
