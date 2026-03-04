# Changelog - Lesson 038: Custom iterators, IntoIterator, lazy evaluation

## Section 8: Collections & Iterators

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: implementing Iterator for custom structs, IntoIterator for for-loop support, iter/iter_mut/into_iter convention, zero-cost abstraction
- **Exercises added**: Fibonacci iterator, custom Playlist collection with IntoIterator, prime number iterator, iterator vs loop benchmark

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - **Structural ordering issue**: Requires `impl Iterator for Type` before trait implementation syntax taught (lesson 040)
  - Exercise 3 (prime iterator) is algorithmically complex on top of the Rust concepts
- **Recommendations**:
  - Provide scaffolding/template code for the Iterator trait implementation
  - Consider making Exercise 3 (primes) optional or providing the algorithm

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: SIGNIFICANT prerequisite ordering issue -- requires impl Iterator for Type syntax not formally taught until lesson 40 (2 lessons later). Exercise 3 (prime iterator) combines algorithmic complexity with unfamiliar syntax. Exercise 4 (benchmark) adds scope.
- **Why**: Implementing a trait you've only seen via derive is confusing.
- **v4 recommendations status**: Not yet applied -- v4 recommended scaffolding/template code and making prime iterator optional.
- **Gradual progression**: Third heavy lesson in a row (036-037-038); learner fatigue risk.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hr
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - SIGNIFICANT prerequisite ordering - requires impl Iterator for Type before traits taught (lesson 40)
  - Exercise 3 (prime iterator) combines algorithmic complexity with unfamiliar syntax
  - THIRD heavy lesson in a row (036-037-038) - learner fatigue risk
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- No changes needed under relaxed threshold. impl Iterator forward reference still flagged. Note: THIRD heavy in a row — learner fatigue risk flagged. Consider taking a break after this cluster.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-120 min (Heavy, upper edge of 2hr limit)
- **Needs split**: No (barely)
- **Progression**: Third consecutive heavy lesson. SIGNIFICANT prerequisite gap: impl Iterator for Type requires trait knowledge not taught until lesson 040.
- **Issues**: Must provide complete scaffolding/template code for impl Iterator (flagged since v4, CRITICAL). Exercise 3 (Primes) should provide the trial-division algorithm. Exercise 4 (benchmark) should be marked optional. Notes section should advise taking a break after 036-037.
- **Changes made**: None (content fix deferred to lesson start -- HIGH PRIORITY)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-120 min
- **Pacing**: Heavy (upper edge of 2hr)
- **Needs split**: No (barely)
- **Issues**: SIGNIFICANT PREREQUISITE VIOLATION: Requires impl Iterator for Type before trait impl taught in lesson 40 (2 lessons later). Exercise 3 (prime iterator) combines algorithmic complexity with unfamiliar syntax. Exercise 4 (benchmark) adds more scope. Must provide scaffolding for impl Iterator. Exercise 3 should provide trial-division algorithm. Exercise 4 should be [STRETCH]. FATIGUE WARNING — third consecutive heavy lesson (036-037-038). Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Good match
- **Time estimate**: 90-120 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Third consecutive heavy lesson (036-037-038). Highest fatigue risk in Section 8.
- **Unresolved from prior reviews**: (1) SIGNIFICANT: impl Iterator for Type before traits taught (lesson 040) -- must provide template code. (2) Exercise 3 (Primes) combines algorithm + Rust complexity -- provide trial-division algorithm. (3) Exercise 4 should be marked [STRETCH]. All unresolved since v4.
- **New findings**: None
- **Recommendation**: Provide complete impl Iterator scaffold. Supply algorithm for Exercise 3. Mark Exercise 4 as [STRETCH]. Consider adding a "take a break" note after this lesson.

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 100-120min (Heavy, borderline)
- **Needs split**: No
- **Progression**: Third consecutive heavy lesson. Template/scaffold for Iterator impl has been added (partially resolved).
- **Changelog reconciliation**: impl Iterator scaffold flagged since v4 -- template has been added to task file (partially resolved)
- **Genuinely unresolved**: (1) Exercise 3 should provide trial-division algorithm for primes. (2) Exercise 4 should be marked [STRETCH].
- **Recommendation**: Supply trial-division algorithm in Exercise 3 and mark Exercise 4 as [STRETCH] before lesson start

### v11-fix - Added prime algorithm scaffold and marked Exercise 4 [STRETCH] (2026-03-04)
- Provided is_prime() helper function for Exercise 3
- Marked Exercise 4 as [STRETCH]
- **Why**: Exercise combined algorithmic complexity with unfamiliar Iterator syntax; Exercise 4 was an unnecessary time burden
- **Resolves**: Genuinely unresolved items from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 100-120min
- **Pacing**: Heavy (borderline OVERLOADED)
- **Issues**: SIGNIFICANT prerequisite — impl Iterator for Type before traits taught in lesson 040. Scaffold helps but conceptual gap remains structural.
- **Recommendations**: Add 2-paragraph "mini-intro to trait implementation" at lesson top; consider making IntoIterator for both &Playlist and Playlist a stretch goal.
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Added a 2-paragraph "Prerequisite Note: Implementing a Trait" section after Objectives, before the template code
- Explains the `impl TraitName for TypeName { ... }` syntax pattern and connects it to the derive attribute from lesson 021
- Notes that traits are formally taught in lesson 040 and directs the learner to follow the template
- **Why**: Addresses the SIGNIFICANT prerequisite gap flagged since v4 -- learner needs to understand trait implementation syntax to complete Iterator exercises, but traits are not formally taught until 2 lessons later. The mini-intro bridges this gap without duplicating lesson 040 content.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-95min
- **Pacing**: Good-Heavy
- **Issues**: Exercise 2 IntoIterator for &Playlist requires lifetime annotations not yet taught (lessons 46-50) — consider simplifying to consuming IntoIterator only, or provide borrowing impl as starter code
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-100min
- **Pacing**: Heavy
- **Issues**: Exercise 2 required implementing `IntoIterator for &Playlist` with lifetime annotations not taught until lessons 046-050
- **Changes made**: Simplified Exercise 2 to only require implementing consuming `IntoIterator for Playlist`. The borrowed `IntoIterator for &Playlist` variant is now provided as read-only sample code with a note that lifetime syntax is covered in lesson 046.

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-100min. **Pacing**: Heavy. **Issues**: None — all prior concerns well-mitigated. Third heavy in 036-038 cluster. **Changes**: Changelog only.
