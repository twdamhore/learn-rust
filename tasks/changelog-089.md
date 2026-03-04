# Changelog - Lesson 089: Sealed traits, marker traits, type-level programming

## Section 17: Advanced Type System

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Sealed traits with private module pattern, marker traits (Send/Sync/Unpin), type-level programming basics, const generics, complexity tradeoffs
- **Exercises added**: Sealed Primitive trait, custom unsafe marker trait, PhantomData permission levels, const-generic Matrix with dimension-checked multiply

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Four distinct topics (sealed traits, marker traits, type-level programming, const generics)
  - Matrix multiply with triple const generics (Exercise 4) is time-consuming
  - PhantomData (Exercise 3) overlaps with lesson 087 exercise 4
- **Recommendations**:
  - Acknowledge PhantomData overlap with lesson 087 or differentiate more clearly

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Four distinct topics (sealed traits, marker traits, type-level programming, const generics). Matrix multiply with triple const generics is time-consuming. PhantomData exercise (Exercise 3) overlaps with lesson 087 exercise 4.
- **Why**: Too many conceptual context switches.
- **v4 recommendations status**: Not yet applied -- v4 flagged PhantomData overlap and Matrix complexity. Gradual progression: Heavy section closer; long run of heavy lessons.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Four distinct concepts (sealed, marker, type-level, const generics) mean frequent context switches
  - Exercise 4 (const-generic Matrix) is time-consuming
  - Exercise 3 PhantomData overlaps with lesson 087
- **Action taken**: No split required. Previous v4 recommendations (acknowledge PhantomData overlap, manage Matrix complexity) should be applied when lesson is started

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed under relaxed threshold
- Four distinct topics but within the 2hr limit -- end of the heavy 077-080 cluster

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-110 min (Heavy)
- **Needs split**: No
- **Issues**: Four context switches (sealed, marker, PhantomData, const generics). Exercise 3 overlaps with 078 Exercise 4. Exercise 4 (const-generic Matrix multiply) needs impl signature scaffold. Consider reordering: simpler exercises first.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-110 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Four distinct topics (sealed traits, marker traits, PhantomData permissions, const generics) require context switching. Exercise 3 (PhantomData permissions) overlaps 078 Exercise 4 — differentiate and acknowledge 078 foundation. Exercise 4 (const-generic Matrix multiply) needs impl signature scaffold. Triple const generics (M, N, P) + matrix logic is 20-30 min alone. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match with CLAUDE.md
- **Time estimate**: 80-110 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Heavy section closer; four context switches (sealed, marker, PhantomData, const generics)
- **Unresolved from prior reviews**: (1) Exercise 3 (PhantomData permissions) overlaps with 078 Exercise 4 -- differentiate learning goals and acknowledge 078 foundation. (2) Exercise 4 (const-generic Matrix multiply) needs impl signature scaffold for triple-const-generic (M, N, P) multiply. Flagged since v4, still unresolved.
- **New findings**: None
- **Recommendation**: Differentiate Exercise 3 from 078 Ex4 and add impl signature scaffold to Exercise 4 before teaching

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-110min (Heavy)
- **Needs split**: No
- **Progression**: Heavy section closer; four context switches
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: (1) Exercise 3 PhantomData overlaps 078 Ex 4 -- should explicitly build on 078, (2) Exercise 4 const-generic matrix multiply needs impl signature scaffold.
- **Recommendation**: Differentiate Exercise 3 from 078 and add impl signature scaffold to Exercise 4 before teaching

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-110min
- **Pacing**: Heavy
- **Issues**: (1) Ex 3 PhantomData overlaps lesson 087 Ex 4 — should explicitly build on it. (2) Ex 4 (const-generic Matrix multiply) needs impl Mul signature scaffold. UNRESOLVED.
- **Recommendations**: Add cross-ref to 078 for Ex 3; MUST provide impl Mul scaffold
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Exercise 3 (PhantomData type-level tags): Added cross-reference note "Building on the `PhantomData` tagged types from lesson 087 Exercise 4..." to differentiate from 078 and set context
- Exercise 4 (Const generics): Added `impl Mul` scaffold showing the triple const generic signature `<const M: usize, const N: usize, const P: usize>` with `Mul<Matrix<f64, N, P>> for Matrix<f64, M, N>`, Output type, and multiplication comment
- Added explanatory note about the triple const generic being the key insight for compile-time dimension checking
- **Why**: (1) PhantomData overlap with 078 Ex 4 needed acknowledgment so learner sees it as progression, not repetition. (2) Triple const generic Mul signature is the hardest part of the matrix exercise; without it the learner would spend disproportionate time on the signature rather than the implementation.
- **Resolves**: Both unresolved items flagged since v4 — PhantomData cross-ref and impl Mul scaffold

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Const generics formally taught here but already used in lesson 74 — add 'you saw this before' note. Exercise 4 (matrix multiply with triple const generics) should be marked STRETCH
- **Changes made**: Changelog updated only

### v13-fix - Applied pending task file fixes (2026-03-04)
- Added backward reference to lesson 082 where const generics were first used
- Marked Exercise 4 (triple const generic matrix multiply) as [STRETCH]
- **Why**: Connects the dots between preview usage (074) and formal coverage (080); Exercise 4 is significantly harder than the rest
- **Resolves**: v13 recommendation

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-95min. **Pacing**: Heavy. **Issues**: None — all scaffolding and cross-references verified. **Changes**: Changelog only.
