# Changelog - Lesson 009: Control flow - if/else, loop, while, for, labels, break with values

## Section 2: Language Basics

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: if/else as expressions (contrast with Java/Go), loop/while/for and idiomatic usage, loop labels ('label) with break/continue, break with values from loops, for with ranges and iterators (.iter(), .enumerate())
- **Exercises added**: if as expression (grade assignment), loop with break value (retry counter), nested loops with labels (find pair where i*j==42), FizzBuzz (range + match with tuple pattern), number guessing loop (simulated guesses)

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - 5 exercises (every other task has 4) -- most exercises in the 001-020 range
  - Exercise 4 asks for `match` with tuple patterns, but `match` is formally taught in lesson 23
  - Exercise 5 (number guessing loop) combined with the rest could push over 1 hour
- **Recommendations**:
  - Make Exercise 5 optional or combine with Exercise 4
  - Note that `match` usage in Exercise 4 is a preview

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: 5 exercises (only task in 001-020 with this many). Exercise 4 uses match with tuple patterns before match is taught (lesson 23).
- **Why**: Too many exercises; match forward reference.
- **v4 recommendations status**: Not yet applied -- v4 recommended making Exercise 5 optional and noting match as preview. Gradual progression: Heavy spike; should trim to 4 exercises.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.25-1.75 hr
- **Pacing verdict**: Heavy but under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - 5 exercises (only task with 5 in 001-020)
  - Exercise 4 uses match before it's taught (lesson 23)
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.25-1.75 hr)
- **Status**: No changes needed
- 5 exercises and match preview acceptable

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~75-105 min (Heavy)
- **Needs split**: No
- **Progression**: Control flow is familiar, but 5 exercises and a match forward reference add friction.
- **Issues**: Exercise 5 should be marked optional (flagged since v4). Exercise 4's match rewrite previews lesson 23 -- should be noted as preview.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~75-105 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Only task in 001-020 with 5 exercises — Exercise 5 should be optional. Exercise 4 uses match with tuple pattern (lesson 23 topic). Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Good match with issues
- **Time estimate**: 75-105 minutes (Heavy)
- **Needs splitting**: No (all under 2 hours)
- **Pacing context**: Heavy alongside lesson 6; control flow is familiar but exercise count pushes timing
- **Unresolved from prior reviews**: (1) Exercise 5 should be marked [OPTIONAL], (2) Exercise 4's match usage needs "preview of lesson 23" note (both flagged since v4, never applied)
- **New findings**: None beyond prior reviews
- **Recommendation**: Mark Exercise 5 as optional and add "preview" note to Exercise 4's match usage before starting

## v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 70-100min (Heavy)
- **Needs split**: No
- **Progression**: Heavy alongside lesson 6; with Ex 5 optional, realistic time is 60-90min
- **Changelog reconciliation**: (1) Exercise 5 "should be [OPTIONAL]" — already marked [OPTIONAL] in task file. Resolved. (2) Exercise 4 match on tuple "needs preview note" — task file already includes "(preview of lesson 23)". Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: Ready as-is

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-100min
- **Pacing**: Heavy (Good without optional Ex 5)
- **Issues**: 5 exercises (1 optional); `match` preview from lesson 23
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 65-80min
- **Pacing**: Good
- **Issues**: Exercise 4 match preview needs code template/hint for syntax
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 65-90min
- **Pacing**: Heavy
- **Issues**: Exercise 4 needed match template for tuple pattern syntax
- **Changes made**: Task file updated — added match tuple pattern code template to Exercise 4 with note that it previews lesson 023

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 65-95min
- **Pacing**: Heavy
- **Issues**: None. Match template in Ex 4 and Ex 5 [OPTIONAL] keep pacing reasonable
- **Changes made**: Changelog updated only
