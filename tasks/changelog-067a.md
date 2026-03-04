# Changelog - Lesson 067a: Advanced Async - Part A: The Future Trait and Cancellation
## Section 14: Async Rust

### v1 - Created from split (2026-03-03)
- Split from original lesson 067 which was rated OVERLOADED (~2-3 hrs)
- **Reason for split**: Lesson 067 combined four major hard topics (Future trait impl, manual poll loop, Pin/Unpin, cancellation) -- likely the hardest single lesson in the entire curriculum. For a learner with no C/C++ background, this was unrealistic under 2 hours
- **Scope**: Future trait (poll, Context, Poll::Ready/Pending), hand-implementing futures, async cancellation and drop semantics, comparison to Java CompletableFuture and Go context cancellation
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~75-100 min (Moderate-Heavy)
- **Needs split**: No
- **Issues**: Exercise 3 (Timeout combinator implementing Future manually) is advanced. Recommend providing skeleton or step-by-step guide.
- **Changes made**: None (scaffolding deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~75-100 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 1 (TimerFuture with thread::sleep + Waker) is substantial. A simpler Countdown future might be better first exercise. Exercise 3 (Timeout combinator implementing Future manually) needs skeleton/step-by-step guidance.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Correct split from original 067
- **Time estimate**: 75-100 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Future trait and cancellation are substantial but cohesive. Heavy but within 2hr threshold.
- **Unresolved from prior reviews**: Exercise 3 Timeout combinator needs skeleton/step-by-step guide. Consider simpler Countdown future before TimerFuture as first exercise (flagged since v2/v9).
- **New findings**: None
- **Recommendation**: Provide skeleton for Exercise 3 and consider reordering exercises (Countdown first, then TimerFuture) when lesson is started

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-100min (Heavy)
- **Needs split**: No
- **Progression**: Future trait and cancellation are substantial but cohesive
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: (1) Exercise ordering should be Countdown -> TimerFuture -> Timeout (simpler first), (2) Exercise 3 Timeout combinator needs skeleton
- **Recommendation**: Reorder exercises and provide Timeout combinator skeleton at lesson start

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-110min
- **Pacing**: Heavy
- **Issues**: (1) Exercise ordering should be Countdown->TimerFuture->Timeout (simpler first). (2) Ex 3 Timeout combinator needs skeleton/step-by-step guide. BOTH UNRESOLVED from v2/v9.
- **Recommendations**: Reorder exercises; provide Timeout combinator skeleton
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Reordered exercises for progressive difficulty: (1) Countdown future (simplest, no threads), (2) TimerFuture (thread::sleep + Waker), (3) Timeout combinator (wrapping a future), (4) Cancellation observation (moved to last)
- Added new Countdown future as Exercise 1 -- counts polls, no threading, simplest possible hand-written Future
- Added skeleton struct and Future impl outline to Exercise 3 (Timeout combinator) with guided comments
- **Why**: Starting with TimerFuture (thread + Waker) was too steep as a first Future impl; Countdown lets the learner focus purely on poll/Ready/Pending mechanics. Timeout skeleton reduces boilerplate discovery time.
- **Resolves**: Unresolved items from v2/v9/v10/v11/v12

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Timeout combinator exercise uses Pin<Box<F>> and self: Pin<&mut Self> but Pin is not taught until 067b. Consider reordering 067a/067b or marking Timeout as STRETCH. 4 exercises is heavy — Countdown + TimerFuture + Cancellation alone are 70-80 min
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Marked Exercise 3 (Timeout combinator) as [STRETCH] — uses Pin<Box<F>> and Pin<&mut Self> which are not taught until lesson 067b
- **Changes made**: Task file updated — Exercise 3 header changed to [STRETCH] with note to attempt after completing 067b

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-95min. **Pacing**: Heavy. **Issues**: None — exercise ordering progressive, cross-lesson STRETCH deferral acceptable. **Changes**: Changelog only.
