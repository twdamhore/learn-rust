# Changelog - Lesson 070: Async I/O Part A: Files and Timeouts
## Section 14: Async Rust

### v1 - Created from split (2026-03-03)
- Split from original lesson 070 which was rated HEAVY (~2+ hrs)
- **Reason for split**: Original lesson 070 combined async file I/O, TCP networking, timeouts, and a concurrent file processor into 4 exercises. The TCP echo server alone is a substantial mini-project (binding, accepting, spawning per connection, line-based read/write, testing). Combined with 3 other exercises this significantly exceeds the 1-2 hour target. File I/O and networking are also distinct enough topics to teach separately.
- **Scope**: Async file I/O with `tokio::fs`, timeout wrapping with `tokio::time::timeout`, concurrent file processing with `join_all`/`JoinSet`
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60-80 min (Moderate)
- **Needs split**: No
- **Issues**: Exercise 3 overlaps with Exercise 1 (both concurrent file reading). Consider marking Exercise 3 as optional if time is tight.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~60-80 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercise 3 partially overlaps Exercise 1 (file processing). Consider marking Exercise 3 optional if time tight.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Correct split from original 065
- **Time estimate**: 60-80 minutes (Moderate-Heavy)
- **Needs splitting**: No
- **Pacing context**: File I/O and timeouts are well-scoped for a single lesson. Good first half of the original 065.
- **Unresolved from prior reviews**: Exercise 3 overlaps with Exercise 1 (both concurrent file reading) -- consider marking Exercise 3 [OPTIONAL] (flagged since v2)
- **New findings**: None
- **Recommendation**: Mark Exercise 3 as [OPTIONAL] when lesson is started

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: ~70min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: File I/O and timeouts well-scoped for single lesson
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 3 overlaps Exercise 1 — should mark Ex 3 [OPTIONAL]
- **Recommendation**: Mark Exercise 3 as [OPTIONAL] at lesson start

### v11-fix - Marked Exercise 3 as [OPTIONAL] (2026-03-04)
- Exercise 3 overlaps Exercise 1 (both are concurrent file processing)
- **Resolves**: Minor item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 45-60min
- **Pacing**: Good (slightly light)
- **Issues**: Only 2 required exercises. Could absorb additional exercise combining file I/O with timeout
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 45-60min
- **Pacing**: Light-Moderate
- **Issues**: Lighter pacing acceptable
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 50-60min. **Pacing**: Light-Moderate. **Issues**: Slightly light (2 required exercises), acceptable as breathing room before heavy 071. **Changes**: Changelog only.
