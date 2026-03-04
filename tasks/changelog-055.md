# Changelog - Lesson 055: Rc<T>, Arc<T> - reference counting, shared ownership

## Section 12: Smart Pointers & Interior Mutability

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Rc<T> shared ownership, Rc::clone vs deep clone, Arc<T> thread-safe variant, choosing Box vs Rc vs Arc, reference cycle pitfall, Java GC comparison
- **Exercises added**: DAG with shared Rc nodes and strong_count tracking, reference cycle memory leak demonstration, Rc clone semantics with ptr_eq and drop counting, Arc shared across 4 threads with Rc failure comparison

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 2 requires RefCell (lesson 056 -- forward reference) to create reference cycle
  - Exercise 4 requires spawning threads (lesson 058 -- forward reference)
- **Recommendations**:
  - Provide RefCell boilerplate code for Exercise 2 and label as preview
  - Exercise 4 thread usage is simple enough to be acceptable as Arc motivation

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Exercise 2 requires RefCell (not taught until lesson 56). Exercise 4 requires thread::spawn (not taught until lesson 58). Reference cycle demo is valuable despite forward reference.
- **Why**: Forward references to RefCell and threads.
- **v4 recommendations status**: Not yet applied -- v4 recommended providing RefCell boilerplate. Gradual progression: Heavy continuation.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise 2 (reference cycle) uses RefCell not taught until lesson 056
  - Exercise 4 uses thread::spawn not taught until lesson 058
- **Action taken**: No structural changes. Heavy but within 2hr threshold.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed under relaxed threshold
- RefCell forward reference still flagged.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy)
- **Needs split**: No
- **Progression**: Second of heavy cluster. Forward references to RefCell (056) and threads (058).
- **Issues**: Exercise 2 requires RefCell (lesson 056) -- provide boilerplate with "preview" note. Exercise 4 uses thread::spawn (lesson 058) -- add brief note. Both flagged since v4, unresolved.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: FORWARD REFERENCE — Exercise 2 (reference cycle) requires RefCell<T> not taught until lesson 56. Provide boilerplate with preview note, or reorder. FORWARD REFERENCE — Exercise 4 uses thread::spawn (lesson 58). Acceptable as Arc motivation with brief note. Flagged since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Second heavy lesson in cluster (054-055-056-057a/b)
- **Unresolved from prior reviews**: (1) Exercise 2 uses RefCell (lesson 056) -- add preview note with boilerplate, (2) Exercise 4 uses thread::spawn (lesson 058) -- add preview note. Both flagged since v4.
- **New findings**: None
- **Recommendation**: Add preview notes with boilerplate for forward references at lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-100min (Heavy)
- **Needs split**: No
- **Progression**: Forward refs to RefCell (056) and thread::spawn (058) have preview notes -- partially addressed
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 2 should include RefCell boilerplate code
- **Recommendation**: Add RefCell boilerplate code to Exercise 2 at lesson start

### v11-fix - Added RefCell boilerplate to Exercise 2 (2026-03-04)
- Added RefCell usage scaffold with preview note for Exercise 2 (reference cycle)
- **Why**: RefCell not taught until lesson 056; learner needs concrete pattern
- **Resolves**: Genuinely unresolved item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Forward refs to RefCell (056) and threads (058) — both have preview notes
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Heavy
- **Issues**: TWO PREREQUISITE VIOLATIONS: Exercise 2 uses Rc<RefCell<Node>> (RefCell not taught until 56); Exercise 4 uses threads (not taught until 58). Both have preview notes and code snippets. Consider moving exercise 2 to lesson 56 and exercise 4 to lesson 58 to remove forward references
- **Changes made**: Changelog updated only

### v13-fix - Applied pending task file fixes (2026-03-04)
- Strengthened preview disclaimers on Exercise 2 (RefCell, lesson 56) and Exercise 4 (threads, lesson 58)
- **Why**: Two exercises use concepts not yet taught — clearer disclaimers help learners focus on the Rc/Arc concepts rather than struggling with unfamiliar RefCell/thread syntax
- **Resolves**: v13 prerequisite finding

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-90min
- **Pacing**: Heavy
- **Issues**: Forward references managed with previews
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-90min. **Pacing**: Heavy. **Issues**: Forward references to RefCell (056) and threads (058) managed with preview notes. **Changes**: Changelog only.
