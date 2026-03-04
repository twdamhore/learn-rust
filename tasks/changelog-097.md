# Changelog - Lesson 097: Serde - Serialize/Deserialize, JSON, TOML, custom

## Section 19: Ecosystem & Tooling

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Derive Serialize/Deserialize, serde_json for JSON, toml crate for config, serde attributes customization, custom Deserialize implementation
- **Exercises added**: Generic ApiResponse JSON roundtrip, TOML config with nested sections and defaults, adjacently-tagged enum with rename_all, custom HexColor deserializer

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Covers derive basics, JSON, TOML, 6+ serde attributes, AND custom deserializer
  - Exercise 4 (custom Deserialize with Visitor) is one of serde's hardest topics -- could take 30+ minutes alone
- **Recommendations**:
  - Move custom deserializer to optional/stretch or provide heavy scaffolding

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: Exercise 4 (custom Deserialize with Visitor pattern) is one of serde's most complex topics, could take 30+ min alone. Six serde attributes + JSON + TOML + custom deserializer is too much.
- **Why**: Custom Deserialize extremely advanced for first serde lesson
- **v4 recommendations status**: Not yet applied -- v4 recommended moving custom deserializer to optional or providing heavy scaffolding. Gradual progression: Heavy; ambitious scope.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.75-2.5 hours
- **Pacing verdict**: Heavy - TRIM (not split)
- **Split needed**: No
- **Key issues**:
  - Exercise 4 (custom Deserialize with Visitor pattern) is one of serde's hardest topics; could take 30-45 min alone
  - Six serde attributes + JSON + TOML + custom deserializer is too much for one lesson
- **Action taken**: Exercise 4 (custom Deserialize with Visitor) should be marked as stretch/optional when task content is updated. No split needed -- trimming Exercise 4 to optional brings pacing within range.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- Within relaxed threshold. Custom Deserialize exercise (Ex4) should be marked stretch/optional.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-110 min (Heavy); ~70-80 min with Ex4 optional
- **Needs split**: No
- **Issues**: Exercise 4 (custom Deserialize with Visitor) MUST be marked [STRETCH/OPTIONAL] (flagged since v4 across 4 review rounds, STILL unresolved). This is the highest-impact unfixed issue in this lesson.
- **Changes made**: None (content fix deferred to lesson start -- HIGH PRIORITY)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-110 min (with Ex4)
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: HIGH PRIORITY: Exercise 4 (custom Deserialize with Visitor pattern) is one of serde's hardest topics, 30-45 min alone. MUST be marked [STRETCH/OPTIONAL]. Without this, lesson exceeds 2hrs. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90-110 minutes (Heavy)
- **Needs splitting**: No (if Exercise 4 marked optional)
- **Pacing context**: Section 19 opener. Heavy but manageable if trimmed.
- **Unresolved from prior reviews**: HIGH PRIORITY: Exercise 4 (custom Deserialize with Visitor pattern) MUST be [STRETCH/OPTIONAL]. Flagged 6 consecutive times since v4. Highest-impact unfixed issue in lessons 090-090. Without this fix, lesson exceeds 2 hours.
- **New findings**: None
- **Recommendation**: Mark Exercise 4 [STRETCH/OPTIONAL] BEFORE lesson start — this is the single most important content fix in this range

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy)
- **Needs split**: No
- **Progression**: Section 19 opener. Serde concepts translate well from Jackson/encoding/json.
- **Changelog reconciliation**: "Exercise 4 should be [STRETCH]" flagged v4-v10 as unresolved — task file already has [STRETCH] since v3. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No action needed — Exercise 4 [STRETCH] already present in task file

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy
- **Issues**: Ex 4 (custom Deserialize) correctly [STRETCH]
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy (Good without STRETCH)
- **Issues**: DeserializeOwned vs Deserialize<'de> distinction not explained — common confusion point. Exercise 4 (custom visitor/Deserialize) appropriately marked STRETCH
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: DeserializeOwned vs Deserialize<'de> distinction not explained — common confusion point
- **Changes made**: Added DeserializeOwned explanation before exercises, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-100min. **Pacing**: Heavy. **Issues**: None — STRETCH and DeserializeOwned note verified. **Changes**: Changelog only.
