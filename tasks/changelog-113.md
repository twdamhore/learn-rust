# Changelog - Lesson 113: Database and Authentication
## Section 21: Capstone Projects

### v1 - Created from split (2026-03-03)
- Split from original lesson 112 which was rated OVERLOADED (~3-4 hrs)
- **Reason for split**: Original combined axum learning, full CRUD, SQLite persistence, and JWT authentication in one lesson; axum had no prior introduction in the curriculum
- **Scope**: Replace in-memory storage with SQLite via sqlx, add JWT authentication with jsonwebtoken crate, add auth middleware with custom extractor. Builds on the working axum API from 112.
- **Estimated time**: ~1.5-2 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~95-120 min (Heavy, upper end of target)
- **Needs split**: No
- **Issues**: jsonwebtoken crate is entirely new -- add JWT background note and Go middleware comparison.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~95-120 min
- **Pacing**: Heavy (upper boundary)
- **Needs split**: No
- **Issues**: Introduces TWO new crates (jsonwebtoken, sqlx integration). Should add JWT background note. Tightest "no split needed" in capstone section — learner who struggles with JWT could push past 2hrs.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match (split sub-part)
- **Time estimate**: 95-120 minutes (Very Heavy)
- **Needs splitting**: No, but monitor during execution
- **Pacing context**: Heaviest sub-part in capstone section. Introduces jsonwebtoken + sqlx integration simultaneously. Tightest margin for staying under 2hrs.
- **Unresolved from prior reviews**: None
- **New findings**: Should add JWT background note explaining token structure and why it suits stateless APIs. Learner who struggles with JWT concepts could push past 2hrs.
- **Recommendation**: Add JWT background note. Monitor during execution -- if learner hits 90min before Exercise 3, defer Exercise 3 to stretch goal.

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 100-130min (Very Heavy, tightest margin)
- **Needs split**: No but borderline
- **Progression**: Heaviest sub-part in capstone section. Introduces jsonwebtoken + sqlx integration simultaneously.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: (1) Add JWT background note explaining token structure and why it suits stateless APIs. (2) Add monitoring guidance ("if 90min before Ex 3, defer it"). (3) Exercise 3 (auth middleware) could be [STRETCH].
- **Recommendation**: Add JWT background note, add time monitoring guidance, consider marking Exercise 3 [STRETCH]

### v11-fix - Added JWT primer, monitoring guidance, and [STRETCH] on Exercise 3 (2026-03-04)
- Added JWT background note for learners unfamiliar with token-based auth
- Added time monitoring guidance (defer Ex 3 if past 90 min)
- Marked Exercise 3 as [STRETCH]
- **Why**: Tightest margin lesson (100-130min); JWT concepts need context
- **Resolves**: Genuinely unresolved items from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 100-130min
- **Pacing**: Heavy (borderline OVERLOADED)
- **Issues**: Heaviest capstone lesson — introduces sqlx+axum integration AND JWT simultaneously. Even without [STRETCH] Ex 3, Exs 1-2 could take 90-120min.
- **Recommendations**: Warn learner this is heaviest capstone; don't feel bad deferring Ex 3
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-110min
- **Pacing**: Heavy
- **Issues**: JWT (jsonwebtoken crate) entirely new and not introduced elsewhere. Time check note at 90min is excellent practical guidance. Exercise 3 (auth middleware) appropriately marked STRETCH
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 90-110min
- **Pacing**: Heavy borderline
- **Issues**: None (STRETCH and time check manage scope)
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 90-110min. **Pacing**: Heavy borderline. **Changes**: Added Cargo.toml snippet for sqlx/jsonwebtoken dependencies and time management note (defer Ex 2 if Ex 1 exceeds 60min). **Why**: Tightest-margin lesson in capstone section needs explicit dependency guidance and fallback pacing option.
