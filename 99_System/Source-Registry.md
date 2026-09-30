# Source Registry

**Have we processed EVERY teacher-provided source completely?**

Register every teacher-provided source when received. Never omit one because it appears unimportant. Coverage uses the Teacher Provided flag independently of origin: assigned textbooks and external articles count too. Other sources may also be registered. Unknown assignments remain visible reconciliation issues and block declaring teacher coverage complete.

| ID | File / URL | Type | Origin | Teacher Provided | Unit | Source Location | Size | Received | Method | Status | Chunks Total | Chunks Done | Digest Path | Student Checked | Unit Map Linked | Exam Scope | Priority | Issues |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Field Rules

- **ID:** stable unique identifier, e.g. `BIO-S001`. No sample sources are registered here.
- **File / URL:** link to preserved original or original URL. **Type:** medium, e.g. `teacher-pdf`, `slides`, `video`, `oral-teacher-notes`.
- **Origin:** `teacher`, `textbook`, `external`, or `AI-added`. New entries distinguish teacher-authored material, textbooks, independently authored outside material, and AI generation. Preserve source title and original authorship in the Digest.
- **Teacher Provided:** `yes`, `no`, or `unknown`; mirrors Digest `teacher_provided: true`, `false`, or `null`. Use `yes` for everything supplied or assigned by the teacher regardless of origin. Legacy `teacher` origins remain unchanged and map to `yes`; other origins do not imply `no`. See [[AGENTS#Provenance and teacher coverage|provenance rules]].
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
- **verified:** a named human reviewer checked the Digest against the original, completed every chunk's Checked field and all coverage checks, and confirmed each retained point links to an existing/new Concept or has an explicit no-Concept reason. Record reviewer/date. AI-only checking cannot establish this status. Unresolved extraction/content-accuracy gaps block verification; faithfully captured source disagreements may remain open in Concept Conflicts / Nuances.

Student Checked is separate from coverage verification: a named adult reviewer may verify coverage, but must not claim student checking or understanding. AI extraction remains student-unconfirmed until Justin's check. Concept synthesis separately stays draft until Justin checks its current content. New revisions or omissions reopen affected chunks/source status and affected Concept verification. Preserve the earlier original and identify the revision.

## Provenance and Revision History

This migration adds `textbook` and Teacher Provided without changing existing IDs or origin labels. The Registry had no source rows at migration. For later corrections, record the old/new values, date, evidence, and reason in the Digest Change History and update both records. Never silently relabel a source or overwrite raw material.

## Weekly Reconcile

- [ ] Compare actual teacher distribution channels (class portal, assignments, handouts, links, and oral notes) with this Registry; record the channels and date below.
- [ ] Register missing sources immediately, regardless of apparent importance, priority, or known exam scope.
- [ ] Confirm immutable originals, full assigned extents, and complete chunk plans, including the final page/slide/timestamp; inspect missing/unreadable portions and revisions.
- [ ] Reconcile chunk counts and statuses against Digests; do not advance incomplete sources.
- [ ] Reconcile Teacher Provided flags, including assigned textbooks and outside articles; resolve unknown assignments.
- [ ] Check retained knowledge-point transfers to persistent Concepts and original-location evidence; separate teacher, textbook, external, and AI-added material. Check cross-unit duplicates and preserve conflicts.
- [ ] Reconcile all applicable Unit Maps, student-check flags, and unresolved issues.

Reconcile log: date / reviewer / channels checked / missing items or issues / next action. No reconcile has been performed yet.

## Pre-Test Coverage Check

- [ ] Repeat Weekly Reconcile against teacher distribution channels through the latest assignment date.
- [ ] Record the teacher's actual test scope and priorities; leave unknowns explicit. ANY teacher-provided supplemental material may be tested.
- [ ] Account for every Teacher Provided `yes` source for the unit, including textbooks, outside articles, supplements, and shared-unit sources; investigate unknown assignments/units. Never exclude a source based on priority or guessed relevance.
- [ ] Confirm every source is verified, every chunk accounted for, and no coverage/accuracy gap remains; otherwise list the blockers explicitly.
- [ ] Confirm relevant knowledge transfers, source citations, figures, tables, diagrams, and teacher-specific details.
- [ ] Update Unit Map totals and unresolved issues; identify outstanding student checks, especially important diagrams.

Check log: date / reviewer / scope evidence / coverage blockers / pending student checks. No pre-test check has been performed yet.
