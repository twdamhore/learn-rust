# Changelog - Lesson 038: HashMap, HashSet, BTreeMap, entry API

## Section 8: Collections & Iterators

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: HashMap CRUD operations, entry API patterns, Hash+Eq requirements, HashSet operations, BTreeMap for sorted maps
- **Exercises added**: word frequency counter, entry API mastery with grouping, simple cache implementation, set operations and sorted map output

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Three collection types plus the entry API is substantial
  - Exercise 3 (Cache<K,V>) uses generic type parameters before generics taught (lesson 041)
- **Recommendations**:
  - Simplify Exercise 3 to use concrete types (HashMap<String, String>) or note the generic preview

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Three collection types plus entry API is substantial. Exercise 3 (Cache<K,V>) uses generic type parameters before generics formally taught (lesson 39). Entry API (3 patterns) deserves focused attention.
- **Why**: Too many collection types; generic preview issue.
- **v4 recommendations status**: Not yet applied -- v4 recommended simplifying to concrete types.
- **Gradual progression**: Heavy spike; three collections is ambitious.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hr
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Three collection types plus entry API
  - Exercise 3 (Cache<K,V>) uses generic params before generics taught (lesson 39)
  - v4 recommendation to use concrete types not applied
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed
- No changes needed under relaxed threshold. Generic Cache<K,V> forward reference still flagged. Note: first of three heavy lessons in a row (036-037-038) — learner fatigue risk.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy)
- **Needs split**: No
- **Progression**: First of three consecutive heavy lessons (036-037-038). Warn learner to pace across sessions.
- **Issues**: Exercise 3 Cache<K,V> uses generic type parameters before lesson 041 -- should use concrete types like HashMap<String, String> (flagged since v4, unresolved). Entry API (3 distinct patterns) deserves focused attention.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Three collection types plus entry API is substantial. PREREQUISITE ISSUE — Exercise 3 defines Cache<K,V> using generics before generics taught in lesson 39. Should use concrete types. FATIGUE WARNING — first of three consecutive heavy lessons (036-037-038). Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Good match
- **Time estimate**: 90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: First of three consecutive heavy lessons (036-037-038). Learner fatigue risk.
- **Unresolved from prior reviews**: (1) Exercise 3 Cache<K,V> uses generics before lesson 041 -- replace with concrete types (e.g., HashMap<String, String>). (2) Three consecutive heavy lessons (036-037-038) flagged for fatigue. Both unresolved since v4.
- **New findings**: None
- **Recommendation**: Replace Cache<K,V> with concrete types. Add note advising learner to pace across sessions for the 036-038 cluster.

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-100min (Heavy)
- **Needs split**: No
- **Progression**: First of 3 consecutive heavy lessons (036-037-038) -- fatigue warning remains relevant
- **Changelog reconciliation**: "Exercise 3 uses generic Cache<K,V>" flagged since v4 as unresolved -- but task file already uses concrete `String` types with note about generics in lesson 041. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No further changes needed. Cache<K,V> issue is resolved in task file. Fatigue warning for 036-038 cluster stands.

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-100min
- **Pacing**: Heavy
- **Issues**: First of 3 consecutive heavy lessons (036-037-038); Ex 3 cache exercise uses closures.
- **Recommendations**: Add fatigue warning note for 036-038 cluster.
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-85min
- **Pacing**: Good-Heavy
- **Issues**: Exercise 3 uses impl FnOnce() -> String (closures lesson 51) — consider simplifying to take String value, or add note explaining the closure parameter. Add fatigue warning for 036-037-038 heavy cluster
- **Changes made**: Changelog updated only

### v13-fix - Applied pending task file fixes (2026-03-04)
- Added fatigue warning note for the 036-037-038 dense cluster
- **Why**: Three consecutive Good-Heavy lessons on related topics (collections + iterators) can cause burnout
- **Resolves**: v12 and v13 recommendation

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-90min
- **Pacing**: Heavy
- **Issues**: Exercise 3 used `impl FnOnce() -> String` closure parameter, which is a forward reference to closures (lesson 055)
- **Changes made**: Simplified Exercise 3 from `get_or_insert_with` with `impl FnOnce() -> String` to `get_or_insert` taking a `String` value directly. Added note that closure-based version is covered after lesson 055.

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-90min. **Pacing**: Heavy. **Issues**: None — v14 closure removal correct, fatigue warning in place. **Changes**: Changelog only.
