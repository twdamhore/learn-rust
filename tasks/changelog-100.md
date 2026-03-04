# Changelog - Lesson 100: Networking - reqwest, hyper, raw TCP/UDP

## Section 19: Ecosystem & Tooling

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: HTTP requests with reqwest (sync/async), hyper as lower-level HTTP library, raw TCP client/server with std::net, UDP datagrams, custom HTTP client configuration with headers/timeouts
- **Exercises added**: Fetch from public API with reqwest, build TCP echo server with threads, UDP sender/receiver demonstrating unreliability, HTTP client with custom headers and retry logic

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Covers 4 distinct networking topics (HTTP client, TCP server, UDP, HTTP client config)
  - Exercise format uses unnumbered bullets instead of 'Exercise N -- Title' (formatting inconsistency with tasks 001-088)
  - Exercise 1 requires internet access
- **Recommendations**:
  - Standardize exercise format to 'Exercise N -- Title'
  - Consider reducing scope to 3 topics (drop UDP or HTTP config)

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: Four distinct networking paradigms (HTTP client, TCP, UDP, HTTP config) too broad. Exercise format inconsistency (unnumbered bullets instead of Exercise N format). TCP echo server alone involves server + client + multithreading. Exercise 1 requires internet access.
- **Why**: Too many paradigms; format inconsistency
- **v4 recommendations status**: Not yet applied -- v4 flagged format issue and recommended reducing to 3 topics. Gradual progression: Heavy; format break.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2.5 hours
- **Pacing verdict**: Heavy - TRIM (not split)
- **Split needed**: No
- **Key issues**:
  - Four networking paradigms (reqwest, TCP, UDP, custom HTTP client) too broad
  - TCP echo server alone is substantial (server + client + multithreading)
  - Exercise format inconsistent (unnumbered bullets instead of Exercise N format)
- **Action taken**: Recommend reducing to 3 topics (drop UDP or HTTP config) and fixing exercise format when task content is updated. No split needed -- trimming scope brings pacing within range.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- Within relaxed threshold. 4 networking paradigms still flagged. Exercise format inconsistency noted.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-110 min (Heavy, borderline 2hr)
- **Needs split**: No
- **Issues**: Exercise format uses unnumbered bullets (must standardize). Four networking paradigms too broad -- recommend dropping UDP exercise. Exercise 1 requires internet access.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-110 min
- **Pacing**: Heavy
- **Needs split**: No, but needs trimming
- **Issues**: Exercise format uses unnumbered bullets — must standardize to "Exercise N — Title". Four networking paradigms (reqwest HTTP, TCP, UDP, custom HTTP client) too broad — drop UDP exercise. Exercise 1 requires internet access. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90-110 minutes (Heavy)
- **Needs splitting**: No (if trimmed)
- **Pacing context**: Networking concepts transfer from Go's net/http. Heavy but familiar territory.
- **Unresolved from prior reviews**: (1) Exercise format uses unnumbered bullets — must standardize, (2) Drop UDP exercise or mark [STRETCH], (3) Exercise 1 needs internet access note
- **New findings**: None
- **Recommendation**: Standardize exercise format, drop/mark UDP exercise, add internet access note before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy)
- **Needs split**: No
- **Progression**: Networking concepts transfer from Go's net/http. Heavy but familiar territory.
- **Changelog reconciliation**: "Exercises use unnumbered bullets" — task file uses proper "Exercise N" format. Resolved. Exercise 3 (UDP) already [STRETCH]. Internet required for Ex 1.
- **Genuinely unresolved**: None
- **Recommendation**: No action needed — exercise format and [STRETCH] marking already correct in task file

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy
- **Issues**: (1) Ex 1 requires internet access — not noted. (2) TCP echo server (Ex 2) is substantial — 30-40min alone.
- **Recommendations**: Add internet access note; consider providing server skeleton for Ex 2
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Added internet access note in Notes section warning that Exercise 1 requires a working connection to reach a public API

### v13-fix - Applied pending fixes (2026-03-04)
- Added TCP echo server skeleton code to Exercise 2
- **Why**: Building a TCP server from scratch is ~30-40 min without guidance; skeleton reduces friction
- **Resolves**: v12 recommendation

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Covers too many networking paradigms (blocking HTTP, async HTTP, TCP, UDP, HTTP config). Exercise 3 (UDP) or Exercise 4 (retries) should be STRETCH. Exercise 4 also implicitly requires clap (lesson 88)
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Exercise 4 (HTTP client with retries) adds too much scope on top of already-heavy networking paradigms
- **Changes made**: Marked Exercise 4 STRETCH, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-100min. **Pacing**: Heavy. **Issues**: Core is 2 exercises (HTTP client + TCP echo server), adequate since Ex 2 is substantial. Two STRETCH exercises provide depth. **Changes**: Changelog only.

### v16 (2026-03-04) — Full curriculum review (119 lessons)
- No changes needed — reviewed for pacing, progression, and forward references

### v17 (2026-03-04) — Human-learning clarity pass
- Reduced core scope by making HTTP async-first and moving UDP objective to optional.
- Updated Exercise 1 to async-first with blocking version as optional comparison.
- Added explicit session scope note: complete Exercises 1-2 as core and pick at most one stretch item.
