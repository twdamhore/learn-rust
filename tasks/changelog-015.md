# Changelog - Lesson 015: Borrowing rules, the borrow checker, common errors

## Section 3: Ownership System

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Two borrowing rules (many &T XOR one &mut T), reading borrow checker errors, NLL in practice, common patterns and fixes (scopes/splitting/clone/reorder)
- **Exercises added**: Classic Vec invalidation (push while holding reference), fix broken borrow checker code (3 sub-problems), multiple mutable borrow fixes (3 approaches), struct field borrowing through methods vs direct access

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 2 has a sub-problem referencing `&mut self` and `&self` methods on structs -- but structs/impl blocks not taught until lessons 019-020
  - Effectively 10 coding tasks across 4 exercises (Exercise 2 has 3 sub-problems, Exercise 3 has 3 fix approaches)
- **Recommendations**:
  - Replace the struct method sub-problem in Exercise 2 with a standalone function equivalent
  - Consider reducing Exercise 3 from 3 fixes to 2

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Effectively ~10 coding tasks across 4 exercises. Exercise 2 uses &mut self/&self on structs (not taught until lessons 19-20). Exercise 4 requires struct knowledge.
- **Why**: Too many sub-problems; struct/impl forward reference.
- **v4 recommendations status**: Not yet applied -- v4 recommended replacing struct method sub-problem and reducing Exercise 3. Gradual progression: Heavy spike in the ownership section.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hr
- **Pacing verdict**: Heavy borderline
- **Split needed**: No
- **Key issues**:
  - ~10 coding tasks across 4 exercises
  - Exercise 2 uses &mut self/&self on structs before structs taught (lessons 19-20)
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- 10 coding tasks across 4 exercises still flagged but within limit

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-120 min (Heavy borderline)
- **Needs split**: No
- **Progression**: ~10 coding tasks is a lot. Exercise 2 and Exercise 4 use structs/impl blocks not taught until lessons 19-20.
- **Issues**: Forward dependency on structs (flagged since v4, unresolved). v4 recommended replacing struct method sub-problem with standalone function equivalent.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-120 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 2 has sub-problem referencing &mut self/&self on structs (not taught until 019-020). Exercise 4 explicitly requires structs. Should replace struct-dependent problems with standalone function equivalents. Unresolved since v4.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Aligned with CLAUDE.md Section 3 (Ownership System)
- **Time estimate**: 90-120 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: ~10 coding tasks across 4 exercises is a lot. Heavy spike in the ownership section.
- **Unresolved from prior reviews**: Exercise 2 sub-problem 2 and Exercise 4 use struct methods/fields before structs taught (lessons 19-20). Should be rewritten with standalone functions. Flagged since v4.
- **New findings**: None beyond prior reviews
- **Recommendation**: Before teaching, rewrite struct-dependent problems (Exercise 2 sub-problem 2 and Exercise 4) to use standalone functions only

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 100-130min (Heavy-Borderline)
- **Needs split**: No
- **Progression**: ~10 coding tasks across 4 exercises remains heavy but within 2hr limit.
- **Changelog reconciliation**: Exercise 2 "uses &mut self/&self on structs" flagged since v4 — but the task file actually uses standalone functions, not struct methods. Resolved.
- **Genuinely unresolved**: Exercise 2.3 uses HashMap (lesson 36) — should use Vec instead. Consider reducing Ex 3 from 3 fix approaches to 2.
- **Recommendation**: Replace HashMap usage in Exercise 2.3 with Vec. Optionally reduce Ex 3 fix approaches from 3 to 2.

### v11-fix - Replaced HashMap with Vec in Exercise 2.3 (2026-03-04)
- Changed mutate-while-iterating example from HashMap to Vec<i32>
- **Why**: HashMap not taught until lesson 36; Vec demonstrates same borrow checker concept
- **Resolves**: MODERATE priority item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 100-140min
- **Pacing**: OVERLOADED
- **Issues**: ~10 coding tasks across 4 exercises is too many; Exercises 3-4 each have 3 fix approaches
- **Recommendations**: Reduce Ex 3 from 3 fix approaches to 2 (drop block-scope approach); reduce Ex 4 from 3 to 2 fix approaches. This brings total to ~7 coding tasks and ~90-110min.
- **Changes made**: Changelog updated only — task file changes recommended but not yet applied

### v12-fix - Task file changes applied (2026-03-04)
- Reduced Exercise 3 from 3 fix approaches to 2: removed "use a block scope to limit the first borrow" (least common pattern in real code, and NLL makes it largely unnecessary)
- Reduced Exercise 4 from 3 fix approaches to 2: removed tuple field splitting approach (niche technique that adds complexity without proportional learning value at this stage)
- **Why**: Brings total from ~10 coding tasks down to ~7, fitting within the 1-2hr target. Implements v12 recommendation.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: Exercise 2 is very dense (3 broken programs to fix); Exercise 4 (split borrows) is subtle. Borderline at 2hr upper bound
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 80-110min
- **Pacing**: Heavy
- **Issues**: Exercise 2.2 description was ambiguous about the borrow conflict
- **Changes made**: Task file updated — clarified Exercise 2 sub-problem (2) to explicitly describe the `append_length` function receiving `s: &mut String` and the conflict when trying to create `&s` while mutably borrowed

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 80-110min
- **Pacing**: Heavy
- **Changes made**: Rewrote Exercise 2 sub-problem 2 — replaced `append_length` reborrow scenario with a genuine aliasing conflict (mutable element reference + push on Vec)
- **Why**: Original scenario (`&mut String` passed as `&String` to helper) would not actually trigger a borrow error due to Rust's implicit reborrowing semantics
