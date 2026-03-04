# Changelog - Lesson 043: Trait objects - dyn Trait, vtables, object safety

## Section 9: Generics & Traits

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Dynamic dispatch and vtables, creating trait objects (Box/&/Arc), object safety rules, static vs dynamic dispatch trade-offs, heterogeneous collections and plugin architectures
- **Exercises added**: Vec<Box<dyn Shape>> heterogeneous collection, object safety violation and fix, plugin system with 3 plugins, static vs dynamic dispatch comparison with assembly/binary inspection

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate-to-Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 4 (comparing generated assembly) could be time-consuming for a beginner
  - Vec<Box<dyn Shape>> pattern overlaps with task 054 exercise 4
- **Recommendations**:
  - Consider making Exercise 4 (assembly comparison) optional
  - Differentiate the Shape exercises between tasks 043 and 054

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate-to-Heavy (~1-1.25 hr) for 1-2 hour target
- **Changes noted**: Exercise 4 (assembly/binary comparison) is unrealistic for this stage. Vec<Box<dyn Shape>> pattern duplicated in task 054 Exercise 4. Plugin system (Exercise 3) is the most valuable exercise.
- **Why**: Assembly comparison too advanced; exercise duplication.
- **v4 recommendations status**: Not yet applied -- v4 recommended making Exercise 4 optional. Gradual progression: Slight upward push.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.25 hours
- **Pacing verdict**: Moderate-Heavy - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise 4 (assembly/binary comparison) unrealistic at this stage
  - Vec<Box<dyn Shape>> duplicated with task 054
- **Action taken**: No structural changes. Issues flagged for future content revision.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate-Heavy (~1.25 hr)
- **Status**: No changes needed
- Assembly comparison exercise still flagged as unrealistic.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~75 min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Plugin system exercise is the highlight. Good step up from 042.
- **Issues**: Exercise 4 (assembly comparison) is unrealistic -- replace with simpler static vs dynamic dispatch comparison (flagged since v4, unresolved). Vec<Box<dyn Shape>> exercise overlaps with task 054.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~75 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 4 (assembly/binary comparison) unrealistic — learner shouldn't inspect assembly at this stage. Replace with simpler dispatch comparison. DUPLICATE EXERCISE — Vec<Box<dyn Shape>> repeats in task 054 Exercise 4. Flagged since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 75-90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Plugin system exercise is the highlight; step up from 042
- **Unresolved from prior reviews**: (1) Exercise 4 (assembly comparison) unrealistic -- replace with simpler dispatch comparison (flagged since v4). (2) Vec<Box<dyn Shape>> duplicated in task 054 Exercise 4 (flagged since v4).
- **New findings**: None
- **Recommendation**: Replace Exercise 4 with simpler static-vs-dynamic dispatch comparison; differentiate Shape exercise from task 054

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-100min (Heavy)
- **Needs split**: No
- **Progression**: Plugin system exercise remains the highlight. Good step up from 042.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 4 (assembly comparison) is unrealistic at this stage -- should be simplified to static-vs-dynamic dispatch comparison without assembly, or marked [STRETCH]
- **Recommendation**: Replace Exercise 4 with conceptual static-vs-dynamic dispatch comparison (no assembly) or mark [STRETCH]

### v11-fix - Simplified Exercise 4 from assembly to binary size comparison (2026-03-04)
- Replaced assembly inspection with binary size comparison (more accessible)
- Marked as [STRETCH]
- **Why**: Assembly inspection unrealistic for Rust beginners at this stage
- **Resolves**: Minor item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Vec<Box<dyn Shape>> pattern in Ex 1 duplicates task 054 Ex 4 — should differentiate domains. UNRESOLVED from v4.
- **Recommendations**: Task 054 should use different trait/type set
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Changed Exercise 1 domain from `Shape` (area/name with Circle/Rectangle/Triangle) to `Widget` (render/name with Button/TextBox/Checkbox) to differentiate from task 054
- Updated Exercises 2 and 4 to reference `Widget` instead of `Shape` for consistency
- **Why**: Vec<Box<dyn Shape>> pattern was duplicated between task 043 and task 054 (flagged since v4). Task 043 now uses a Widget UI system while task 054 uses a Logger system.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-85min
- **Pacing**: Good-Heavy
- **Issues**: Box<dyn Trait> is an unavoidable forward reference (Box lesson 54). Box has been previewed in lessons 24 and 42. Consider adding brief Box primer at lesson top and dropping Arc<dyn Trait> from objectives until lesson 55
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-90min
- **Pacing**: Heavy
- **Issues**: Box<dyn Trait> is a forward reference (Box lesson 054); Arc<dyn Trait> is a forward reference (Arc lesson 055)
- **Changes made**: Added Box<T> primer note before exercises section. Removed Arc<dyn Trait> from Objective 2, keeping only Box<dyn Trait> and &dyn Trait, with note that Arc<dyn Trait> is covered in lesson 055.

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-90min. **Pacing**: Heavy. **Issues**: Suggest adding forward pointer to lesson 054 in Box primer. **Changes**: Changelog only.
