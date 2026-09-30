# Source Registry

**Have we processed EVERY teacher-provided source completely?**

Register every teacher-provided source when received. Never omit one because it appears unimportant. External and AI-added sources may also be registered; keep their origins distinct and exclude them from teacher-source totals.

| ID | File / URL | Type | Origin | Unit | Source Location | Size | Received | Method | Status | Chunks Total | Chunks Done | Digest Path | Student Checked | Unit Map Linked | Exam Scope | Priority | Issues |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Field Rules

- **ID:** stable unique identifier, e.g. `BIO-S001`. No sample sources are registered here.
- **File / URL:** link to preserved original or original URL. **Type:** medium, e.g. `teacher-pdf`, `slides`, `video`, `oral-teacher-notes`.
- **Origin:** only `teacher`, `external`, or `AI-added`. Teacher-assigned outside materials have origin `teacher`; preserve their original authorship too.
- **Unit:** consistent unit name; list all applicable units for shared sources, or `unknown` until assigned.
- **Source Location:** full assigned extent within the original, e.g. pages 1–18, slides 1–35, or timestamps 00:00–12:30. If unspecified, cover the entire supplied source.
- **Size:** total pages, slides, duration, images, or note sections; record `unknown` until established. **Received:** `YYYY-MM-DD`. **Method:** actual extraction method, or `not started`.
- **Chunks Total / Done:** planned chunks / chunks fully processed into the Digest. Use `unknown / 0` until planned. Every source needs at least one chunk; long sources need multiple chunks covering the full extent without gaps.
- **Digest Path:** vault-relative wiki link. **Student Checked:** `yes` only after the student checks the Digest against the original, including important diagrams; otherwise `no` or `unknown`. Log partial checks in the Digest.
- **Unit Map Linked:** `yes` only when the source is listed in every applicable Unit Map; otherwise `no` or `unknown`.
- **Exam Scope:** teacher's actual statement with a location/date, or `unknown`. Unknown scope never excludes a teacher source from coverage.
- **Priority:** only `teacher-stated`, `high`, or `normal`; default `normal`. `teacher-stated` requires evidence of explicit teacher emphasis. Priority NEVER changes coverage requirements.
- **Issues:** unresolved gaps, unreadable content, preservation gaps, or questions; `none` only after checking. Teacher-provided does NOT automatically mean teacher-emphasized.

## Status Gates

`inbox → registered → extracting → extracted → verified`

- **inbox:** received and entered here immediately; metadata/original filing still pending.
- **registered:** ID, origin, original reference, and known metadata recorded; unknowns explicit.
- **extracting:** Digest created and chunk coverage planned; extraction underway.
- **extracted:** every planned chunk fully processed into the Digest; Chunks Done equals Chunks Total. Unreadable or omitted content blocks this gate. AI extraction is still a draft.
- **verified:** Digest checked against the original, all coverage checks complete, and each retained knowledge point linked to a Concept or explicitly marked as not requiring one with a reason. Record reviewer and date. Unresolved content/accuracy gaps block verification; clearly recorded learning questions may remain.

Student Checked is separate from verification: a named non-student reviewer may verify coverage, but must not claim student checking or understanding. New source revisions or discovered omissions reopen the affected chunks and source status; update both records. Preserve the earlier original and identify the revision.

## Weekly Reconcile

- [ ] Compare actual teacher distribution channels (class portal, assignments, handouts, links, and oral notes) with this Registry; record the channels and date below.
- [ ] Register missing sources immediately, regardless of apparent importance, priority, or known exam scope.
- [ ] Confirm originals, full assigned extents, and complete chunk plans; inspect missing/unreadable portions and revisions.
- [ ] Reconcile chunk counts and statuses against Digests; do not advance incomplete sources.
- [ ] Check retained knowledge-point transfers and original-location evidence; separate teacher, external, and AI-added material.
- [ ] Reconcile all applicable Unit Maps, student-check flags, and unresolved issues.

Reconcile log: date / reviewer / channels checked / missing items or issues / next action. No reconcile has been performed yet.

## Pre-Test Coverage Check

- [ ] Repeat Weekly Reconcile against teacher distribution channels through the latest assignment date.
- [ ] Record the teacher's actual test scope and priorities; leave unknowns explicit. ANY teacher-provided supplemental material may be tested.
- [ ] Account for every teacher source for the unit, including supplements and shared-unit sources; investigate unassigned sources. Never exclude a source based on priority or guessed relevance.
- [ ] Confirm every source is verified, every chunk accounted for, and no coverage/accuracy gap remains; otherwise list the blockers explicitly.
- [ ] Confirm relevant knowledge transfers, source citations, figures, tables, diagrams, and teacher-specific details.
- [ ] Update Unit Map totals and unresolved issues; identify outstanding student checks, especially important diagrams.

Check log: date / reviewer / scope evidence / coverage blockers / pending student checks. No pre-test check has been performed yet.
