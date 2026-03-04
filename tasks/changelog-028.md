# Changelog - Lesson 028: Crates, packages, use, re-exports, prelude pattern

## Section 6: Project Organization

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Crate vs package vs module distinction, use declaration styles (single/nested/glob/alias), absolute vs relative paths, re-exports with pub use, prelude concept and std::prelude
- **Exercises added**: Practice all use statement styles in one program, re-exports for clean API with internal modules, external crates (rand/chrono) from crates.io, exploring std prelude items and creating custom prelude module

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - Exercise 3 requires internet access to download crates
- **Recommendations**: None - lesson builds naturally on lesson 027

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: Java/Go devs understand dependency management well. Exercise 3 requires internet access for crate downloads.
- **Why**: Familiar concepts with moderate overhead.
- **v4 recommendations status**: Not yet applied -- v4 recommended noting internet requirement. Gradual progression: Good breather after heavy lesson 25.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~50-60 min
- **Pacing verdict**: Moderate
- **Split needed**: No
- **Key issues**: None - requires internet for external crates; good breather after heavy lesson 027
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~50-60 min)
- **Status**: No changes needed

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~50-60 min (Moderate)
- **Needs split**: No
- **Progression**: Good breather after heavy lesson 027. Dependency concepts familiar from Java/Go.
- **Issues**: Exercise 3 requires internet access (minor logistics).
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~50-60 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: None
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 50-60 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Good breather after heavy lesson 027. Dependency management concepts familiar from Java/Go.
- **Unresolved from prior reviews**: None
- **New findings**: Exercise 3 needs internet access note (minor logistics, flagged in prior reviews but not as unresolved)
- **Recommendation**: Add internet access note to Exercise 3 when lesson begins

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 50-65min (Moderate)
- **Needs split**: No
- **Progression**: Good breather after heavy 025. Internet required for Exercise 3 (note in task).
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No changes needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 50-65min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-85min
- **Pacing**: Good
- **Issues**: Exercise 2 requires multi-crate setup (formally lesson 27); Exercise 3 could provide exact Cargo.toml dependency lines to avoid crates.io navigation time
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 65-85min
- **Pacing**: Medium-Heavy
- **Issues**: None (v13 concerns resolved)
- **Changes made**: Added path dependency syntax and lesson 029 cross-reference to Exercise 2; added exact Cargo.toml dependency lines (`rand = "0.8"`, `chrono = "0.4"`) to Exercise 3, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 65-85min. **Pacing**: Medium. **Issues**: None — v14 additions (dependency syntax, Cargo.toml lines) well-targeted. **Changes**: Changelog only.
