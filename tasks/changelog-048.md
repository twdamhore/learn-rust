# Changelog - Lesson 048: Struct lifetimes, 'static, lifetime bounds on generics

## Section 10: Lifetimes

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Lifetime params on structs, 'static lifetime, lifetime bounds on generic types (T: 'a), nested struct lifetime relationships, owned vs borrowed design decisions
- **Exercises added**: ImportantExcerpt struct borrowing, 3 "does not live long enough" debugging scenarios, 'static exploration with string literals, owned vs borrowed Config design comparison

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Three distinct sub-topics (struct lifetimes, 'static, lifetime bounds)
  - Exercise 2 has 3 sub-scenarios plus fixes, could consume significant time
  - `T: 'static` misconception deserves careful explanation time
- **Recommendations**:
  - Consider reducing Exercise 2 from 3 sub-scenarios to 2

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Three distinct sub-topics (struct lifetimes, 'static, lifetime bounds on generics). Exercise 2 has 3 sub-scenarios (effectively 6 mini-exercises). T: 'static misconception deserves careful time.
- **Why**: Too many sub-topics; Exercise 2 too large.
- **v4 recommendations status**: Not yet applied -- v4 recommended reducing Exercise 2 from 3 to 2 sub-scenarios. Gradual progression: Heavy spike after two moderate lessons.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Three sub-topics (struct lifetimes, 'static, lifetime bounds)
  - Exercise 2 has effectively 6 mini-exercises
  - T: 'static misconception needs careful time
- **Action taken**: No structural changes. Heavy but within 2hr threshold.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed under relaxed threshold
- Exercise 2's 6 mini-exercises still flagged.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy)
- **Needs split**: No
- **Progression**: Noticeable difficulty spike after two moderate lessons. Three sub-topics.
- **Issues**: Exercise 2 should be reduced from 3 to 2 sub-scenarios (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 2 has 3 sub-scenarios (6 mini-exercises effectively). Should reduce from 3 to 2 sub-scenarios — drop scenario c which overlaps scenario a. T:'static misconception deserves careful time. Flagged since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90-100 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Heavy spike after two moderate lessons (046-047); T:'static misconception needs careful time
- **Unresolved from prior reviews**: Exercise 2 should reduce from 3 to 2 sub-scenarios -- scenario c overlaps scenario a (flagged since v4)
- **New findings**: None
- **Recommendation**: Drop Exercise 2 scenario c before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-110min (Heavy)
- **Needs split**: No
- **Progression**: Heavy spike after two moderate lessons (046-047)
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 2 should reduce from 3 to 2 sub-scenarios (scenario c overlaps a). Flagged since v4 -- still unfixed after 7 review passes.
- **Recommendation**: Drop Exercise 2 scenario c before lesson start

### v11-fix - Trimmed Exercise 2 from 3 to 2 sub-scenarios (2026-03-04)
- Removed scenario c (overlapped with scenario a)
- **Why**: Reducing exercise volume; flagged since v4 across 7 review rounds
- **Resolves**: MODERATE priority item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-110min
- **Pacing**: Heavy
- **Issues**: Dense — 3 sub-topics. T:'static misconception needs extra emphasis
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: 'static is a notoriously confusing topic; T: 'a lifetime bound on generics is conceptually dense. Consider marking owned-vs-borrowed Config exercise as STRETCH if pacing becomes tight
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-90min
- **Pacing**: Heavy borderline
- **Issues**: Exercise 4 (owned vs borrowed Config) could consume excessive time on open-ended comparison
- **Changes made**: Added time-box note (~15-20 minutes) to Exercise 4, directing learner to focus on implementation differences rather than exhaustive comparison.

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-90min. **Pacing**: Heavy borderline. **Changes**: Added concrete `fn requires_static<T: 'static>` example to Exercise 3 demonstrating that String satisfies the bound but `&'a str` does not. **Why**: T:'static exercise was too vague; concrete example reinforces the "no non-static references" mental model.
