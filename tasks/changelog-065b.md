# Changelog - Lesson 065b: Async I/O Part B: Async Networking
## Section 14: Async Rust

### v1 - Created from split (2026-03-03)
- Split from original lesson 065 which was rated HEAVY (~2+ hrs)
- **Reason for split**: Original lesson 065 combined async file I/O, TCP networking, timeouts, and a concurrent file processor into 4 exercises. The TCP echo server alone is a substantial mini-project (binding, accepting, spawning per connection, line-based read/write, testing). Networking deserves its own focused lesson to build the server properly and extend it into something more interesting (chat or protocol).
- **Scope**: Async TCP echo server with `tokio::net`, per-connection task spawning, line-based framing, extension to multi-client chat or command protocol
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~70-90 min (Moderate-Heavy)
- **Needs split**: No
- **Issues**: Echo server involves many new APIs for someone with no C/systems background. Recommend providing step-by-step hints or partial skeleton.
- **Changes made**: None (scaffolding deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~70-100 min
- **Pacing**: Good to Heavy
- **Needs split**: No
- **Issues**: Echo server involves many new APIs. Step-by-step hints or partial skeleton would help. Exercise 2 (chat server or protocol extension) is well-designed as choose-one.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Correct split from original 065
- **Time estimate**: 70-100 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: TCP echo server is a substantial exercise involving bind, accept, spawn, framing, and testing. Many new APIs for non-systems learner.
- **Unresolved from prior reviews**: Echo server needs step-by-step hints or partial skeleton provided (flagged since v2)
- **New findings**: None
- **Recommendation**: Provide partial skeleton or step-by-step build guide when lesson is started

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: ~90min (Heavy)
- **Needs split**: No
- **Progression**: TCP echo server is substantial but cohesive
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: TCP echo server needs step-by-step build guide (1. bind, 2. accept, 3. spawn, 4. BufReader, 5. echo back)
- **Recommendation**: Provide step-by-step TCP echo server build guide at lesson start

### v11-fix - Added TCP echo server step-by-step guide (2026-03-04)
- Added 7-step build guide for Exercise 1 TCP echo server
- **Why**: Learner has no C/systems networking background; step-by-step reduces trial-and-error
- **Resolves**: MODERATE priority item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-90min
- **Pacing**: Heavy lower end
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-95min. **Pacing**: Heavy. **Issues**: None — step-by-step guide and choose-one extension well-designed. **Changes**: Changelog only.
