# Changelog - Lesson 017: Slices - string slices, array slices, &str vs String

## Section 4: Strings & Slices

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Slices as fat pointers, string slices (&str) with UTF-8 boundaries, array/Vec slices (&[T]), parallel relationships (String/&str, Vec/&[T]), idiomatic parameter types
- **Exercises added**: First word finder (first_word + nth_word), array slice operations (sum_slice + largest), UTF-8 boundary panic and safe slicing, slice vs owned domain extraction comparison with Java history

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate-to-Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 2 returns `Option<&i32>` but `Option` is not introduced until lesson 022
- **Recommendations**:
  - Either provide the `Option`/`Some`/`None` syntax explicitly inline
  - Or simplify return type to `i32` (panicking on empty input)

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate-to-Heavy (~1-1.25 hr) for 1-2 hour target
- **Changes noted**: Exercise 2 returns Option<&i32> but Option not introduced until lesson 22. Exercise 3 (UTF-8 boundary panic) uses char_indices requiring iterator knowledge.
- **Why**: Slice concepts are essential but some exercises use untaught types.
- **v4 recommendations status**: Not yet applied -- v4 recommended inlining Option or simplifying return type. Gradual progression: Slight upward push; manageable.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1-1.25 hr
- **Pacing verdict**: Moderate-Heavy
- **Split needed**: No
- **Key issues**:
  - Exercise 2 returns Option<&i32> but Option not taught until lesson 22
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate-Heavy (~1-1.25 hr)
- **Status**: No changes needed
- Option forward reference still flagged

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60-75 min (Moderate)
- **Needs split**: No
- **Progression**: Critical lesson. Content is appropriate.
- **Issues**: Exercise 1 (nth_word) and Exercise 2 (largest) return Option types but Option not taught until lesson 22. Should add inline explanation of Option/Some/None (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~60-75 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercises 1-2 return Option types but Option not introduced until lesson 22. Should inline-explain Option/Some/None or change return types. Unresolved since v4.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Aligned with CLAUDE.md Section 4 (Strings & Slices)
- **Time estimate**: 60-80 minutes (Moderate-Heavy)
- **Needs splitting**: No
- **Pacing context**: Critical slice concepts lesson. Content is appropriate for this stage.
- **Unresolved from prior reviews**: Exercises 1 and 2 return Option types but Option not introduced until lesson 22. Need inline explanation of Option/Some/None or simplified return types. Flagged since v4.
- **New findings**: None beyond prior reviews
- **Recommendation**: Before teaching, either add a brief inline Option/Some/None explainer or change return types to non-Option alternatives

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 70-90min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Exercise 3 uses `.char_indices()` which is minor stretch but acceptable.
- **Changelog reconciliation**: Option forward reference "needs preview note" flagged since v4 — task file already contains Preview note explaining Option<T>. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No action needed. Option preview note already present in task file.

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Heavy
- **Issues**: Minor — uses Option before lesson 022 but preview note is present
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: Option<&str> in Exercise 1 extension is a forward reference to lesson 22; Exercise 4 could be made optional/stretch to reduce load
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: nth_word extension in Exercise 1 uses Option (forward ref to lesson 22) and adds significant scope
- **Changes made**: nth_word marked STRETCH in Exercise 1, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Changes made**: Added .find('@') hint to Exercise 4 with Option preview reminder
- **Why**: Exercise implicitly requires .find() for email domain extraction, taught in 018b
