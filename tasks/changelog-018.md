# Changelog - Lesson 018: Strings in Rust for Java/Go devs - String, &str, when to use which

## Section 4: Strings & Slices

### v1 - Initial creation
- Lesson added to curriculum
- **NEW**: Bridging lesson added after gap analysis

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and bridging lesson tag all align with curriculum
- Correctly tagged as [NEW - bridging lesson] matching CLAUDE.md [NEW] designation
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: String vs &str deep understanding, function signature guidelines (when to use each), UTF-8 implications (len vs chars, no indexing), conversion methods between String and &str, essential string methods
- **Exercises added**: Function signature practice (4 functions with rationale), CSV string processing pipeline, UTF-8 exploration with multi-script strings (Java/Go comparison), word counter with ownership tradeoff (HashMap<&str> vs HashMap<String>)

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 2 uses structs (lesson 019), method chaining, and `Vec` (lesson 034)
  - Exercise 4 uses `HashMap` (lesson 036) and confronts ownership puzzle with `HashMap<&str, usize>` vs `HashMap<String, usize>`
  - Exercise 1 mentions 'store_name on a struct' requiring struct knowledge (lesson 019)
  - Deliberately placed early per CLAUDE.md as bridging lesson for 'biggest pain point from Java/Go'
- **Recommendations**:
  - Provide enough scaffolding code that learner can complete exercises without prior struct/HashMap knowledge
  - Explicitly note which concepts are being previewed
  - Or simplify exercises to use only concepts taught so far (variables, functions, slices)

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Deliberately placed early (biggest Java/Go pain point per CLAUDE.md). Exercise 1 references structs (lesson 19), Exercise 2 uses structs + Vec (lesson 34), Exercise 4 uses HashMap (lesson 36) -- major forward references.
- **Why**: Early placement is correct in principle but exercises outrun taught concepts.
- **v4 recommendations status**: Not yet applied -- v4 recommended scaffolding or simplifying to avoid HashMap/struct dependencies. Gradual progression: Heavy; exercises need rescoping.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hr
- **Pacing verdict**: Heavy borderline
- **Split needed**: No
- **Key issues**:
  - Exercise 1 references structs (lesson 19)
  - Exercise 2 uses structs + Vec (lesson 34)
  - Exercise 4 uses HashMap (lesson 36)
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- Forward references to structs/Vec/HashMap still flagged but within limit

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-120 min (Heavy borderline)
- **Needs split**: No
- **Progression**: Correctly placed as bridging lesson ("biggest pain point from Java/Go").
- **Issues**: Forward deps on structs (Ex 1.4), Vec/structs (Ex 2 CSV pipeline), HashMap (Ex 4) -- all flagged since v4, unresolved. Recommend simplifying exercises to avoid untaught dependencies.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-120 min
- **Pacing**: Heavy (borderline)
- **Needs split**: No
- **Issues**: Exercise 1 references structs (lesson 19), Exercise 2 uses structs+Vec, Exercise 4 uses HashMap (lesson 36). Multiple forward dependencies despite being a strings lesson. Should simplify exercises to avoid struct/HashMap dependencies. Unresolved since v4.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Aligned with CLAUDE.md Section 4 (Strings & Slices, bridging lesson)
- **Time estimate**: 90-120 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Correctly placed early as bridging lesson for Java/Go devs' biggest pain point. Heavy but within limits.
- **Unresolved from prior reviews**: Exercise 1 item 4 references structs (lesson 19), Exercise 2 uses structs+Vec, Exercise 4 uses HashMap (lesson 36). Forward deps need removal or scaffolding. Flagged since v4.
- **New findings**: None beyond prior reviews
- **Recommendation**: Before teaching, simplify exercises to remove struct/HashMap dependencies or provide full scaffolding code for untaught concepts

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 100-130min (Heavy-Borderline)
- **Needs split**: No (within 2hr limit)
- **Progression**: Bridging lesson correctly placed. Heavy but justified for biggest Java/Go pain point.
- **Changelog reconciliation**: All prior findings consistent — no stale flags
- **Genuinely unresolved**: Exercise 2 (CSV pipeline) is too complex for this stage — uses .parse(), closures, method chaining not yet taught. Should simplify. Exercise 4 (two word counter versions) could reduce to one.
- **Recommendation**: Simplify Exercise 2 to remove .parse()/closures/method-chaining dependencies. Consider reducing Exercise 4 from two versions to one.

### v11-fix - Simplified CSV pipeline exercise (2026-03-04)
- Reduced Exercise 2 from multi-step filter/parse pipeline to simple field extraction
- Removed .parse::<u32>(), closures, and filtering — not yet taught at this stage
- Exercise still demonstrates String vs &str ownership in text processing
- **Why**: Original exercise used 3+ untaught concepts
- **Resolves**: MODERATE priority item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 100-130min
- **Pacing**: Heavy (borderline OVERLOADED)
- **Issues**: HashMap forward ref (scaffolded); Ex 4 two-variant word counter is ambitious
- **Recommendations**: Reduce Ex 4 from two word counter versions to one; keep the other as stretch
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing review and split (2026-03-04)
- Reviewed all 100+ tasks for realistic human pacing (1-2hr OK, split if >2hr)
- **Estimated time**: ~2+ hours (borderline OVERLOADED)
- **Decision**: SPLIT into task-018a.md and task-018b.md
- **Rationale**: 5 objectives, 4 substantial exercises, HashMap forward reference (lesson 036), word counter requiring two implementations. Flagged as Heavy since v4 (12 reviews). v12 explicitly recommended reducing word counter from two versions to one.
- **018a covers**: String vs &str fundamentals, signatures, conversions (3 exercises)
- **018b covers**: UTF-8 implications, string methods, word counter [STRETCH] (3 exercises)
- **Key improvement**: Word counter reduced to single version marked [STRETCH], new conversion fluency exercise added, new string methods practice exercise added
- **Status**: SUPERSEDED -- see task-018a.md and task-018b.md

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 018a/018b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Status**: Correctly superseded by 018a/018b
- **Changes made**: Changelog updated only
