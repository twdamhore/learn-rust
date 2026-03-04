# Changelog - Lesson 022: Methods and associated functions (impl blocks)

## Section 5: Structuring Data

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Write impl blocks with &self/&mut self/self, define associated functions and constructors, auto-referencing, multiple impl blocks, comparison with Java/Go methods
- **Exercises added**: Rectangle methods (area/perimeter/can_hold), constructor pattern with ::new and ::square, builder-style Config with method chaining, mutable Counter methods demonstrating &self vs &mut self

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate-to-Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 3 introduces builder pattern (formally taught in lesson 088)
  - Exercise 3 uses `.into()` for string conversion which requires the `Into` trait (lesson 046)
- **Recommendations**:
  - Replace `.into()` with `String::from()` to avoid forward reference to Into trait

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate-to-Heavy (~1-1.25 hr) for 1-2 hour target
- **Changes noted**: Exercise 3 introduces builder pattern (lesson 79 topic). Exercise 3 uses .into() requiring Into trait (lesson 44). Good lesson 19 continuity.
- **Why**: Builder pattern is a big forward reference; .into() can be replaced with String::from().
- **v4 recommendations status**: Not yet applied -- v4 recommended replacing .into() with String::from(). Gradual progression: Slight upward push; manageable with .into() fix.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1-1.25 hr
- **Pacing verdict**: Moderate-Heavy
- **Split needed**: No
- **Key issues**:
  - Exercise 3 introduces builder pattern (lesson 79) and uses .into() (lesson 44)
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate-Heavy (~1-1.25 hr)
- **Status**: No changes needed
- Builder pattern preview and .into() issue still flagged

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60-75 min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Good continuity with lesson 19 (Rectangle carries forward).
- **Issues**: Exercise 3 uses .into() (Into trait not taught until lesson 44) -- should use String::from() instead (flagged since v4, unresolved). Builder pattern should note it's a preview of lesson 79.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~60-75 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercise 3 uses .into() (Into trait, lesson 44). Should use String::from() instead. Exercise 3 also previews builder pattern (lesson 79). Unresolved since v4.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Aligned with CLAUDE.md Section 5 (Structuring Data)
- **Time estimate**: 60-80 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Good continuity with lesson 19 (Rectangle carries forward). Manageable with minor fixes.
- **Unresolved from prior reviews**: (1) Replace `.into()` with `String::from()` in Exercise 3 (`.into()` requires Into trait, lesson 44). (2) Note builder pattern in Exercise 3 as preview of lesson 79. Flagged since v4.
- **New findings**: None beyond prior reviews
- **Recommendation**: Before teaching, replace `.into()` with `String::from()` and add a note that builder pattern is a preview of lesson 79

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 60-80min (Moderate)
- **Needs split**: No
- **Progression**: Builder pattern preview is fine as "methods that take self and return Self."
- **Changelog reconciliation**: ".into() forward reference" flagged since v4 — but the task file uses `String::from()`, not `.into()`. The concern is a phantom issue. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No action needed. The `.into()` issue does not exist in the task file.

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-80min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: Exercise 3 builder pattern is formally lesson 79 content — consider simplifying to just 'method taking self by value' without full builder chaining
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 65-85min
- **Pacing**: Medium-Heavy
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 65-85min
- **Pacing**: Medium-Heavy
- **Changes made**: Replaced `Config::default()` with `Config::new()` in Exercise 3 and added note that Default trait is in lesson 046
- **Why**: Config::default() requires Default trait (lesson 046) and trait impl syntax (lesson 042), both not yet taught
