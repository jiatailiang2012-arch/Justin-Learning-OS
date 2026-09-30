# Justin Learning OS — Operating Specification

This is the authoritative operating specification for this school-learning vault. Apply it with the user's current instructions. README provides the entry point; templates implement these rules. The initial pilot is Biology Units 1–3. This is not a family knowledge base, medical reference, research notebook, or future research repository.

## Preserve and evolve

- Audit → preserve → modify → add. Inspect existing work first. Commit the existing state before substantial migration; never rebuild by deleting the vault.
- Preserve all original sources, evidence, student writing, source IDs, and history. Do not silently change provenance or rewrite student explanations.
- Preserve existing folder and template paths. Practice, Mistakes, and Output are dormant; no automation is implied.
- The original foundation was called Version 2. It is now treated as the existing V0.x foundation of the long-term pilot; retain its history rather than replacing it.

## Separate coverage from understanding

Source Registry answers whether every teacher-provided source has been fully processed. Source Digests preserve each source's contents and chunk evidence. The persistent Concept Wiki integrates knowledge across sources and units. Unit Maps are entry points, not owners of concepts.

Workflow: source intake → registration → complete chunk extraction → concept synthesis → student check/explanation → future retrieval practice and weakness detection → future study output. Source completeness and student understanding are separate checks.

## Files and raw evidence

- `00_Inbox/`: incoming originals, registered on receipt.
- `01_Sources/Biology/Raw/`: immutable preserved originals. Digests remain separate files in `01_Sources/Biology/` using `BIO-S001 - Short Title.md` names.
- `02_Knowledge/Biology/`: persistent `Concept Name.md` pages and `Unit 1 - Unit Map.md` style entry points. Do not invent unit topics before sources arrive.
- `03_Practice/Biology/`, `04_Mistakes/Biology/`, `05_Output/Biology/`: retain for later work referencing persistent Concepts and supporting evidence.
- `90_Templates/`: edit the existing templates rather than create competing versions.
- `99_System/`: Registry and dated migration reports.

Never overwrite raw PDFs, slides, handouts, worksheets, lab instructions, textbook excerpts, images, or downloaded materials. Copies must preserve the original contents. Revisions receive distinct filenames and a linked revision record; never overwrite the earlier original. Preserve dated snapshots of changing web material where possible. Record missing originals or unreadable portions as blocking coverage issues. Tools must write derived files outside Raw.

## Provenance and teacher coverage

Allowed `origin` values: `teacher`, `textbook`, `external`, `AI-added`. These are not interchangeable. Record original authorship/title even for teacher-distributed material.

`teacher_provided` independently records whether the teacher supplied or assigned the material. Registry: `yes`, `no`, `unknown`; Digest YAML: `true`, `false`, `null`. Count all yes/true sources for teacher coverage, including assigned textbooks and external articles. Unknown assignments remain a visible reconciliation issue; do not silently omit them or declare coverage complete.

For new sources: use `textbook` for textbooks; `teacher` for teacher-authored materials; `external` for independently authored non-textbook materials; `AI-added` for generated content. Record teacher assignment separately. Existing origin labels retain their original meaning and history: a legacy `teacher` source stays `teacher` and maps to teacher_provided=true. Do not automatically infer no/false from any other origin. If correction is necessary, document old value, new value, evidence, date, and reason in the Digest before updating Registry and Digest together. No source rows existed at this migration.

Teacher-provided never means teacher-emphasized. Assignment intent, test scope, and emphasis require explicit evidence; otherwise record `unknown`. Priority remains `teacher-stated`, `high`, or `normal`; it never reduces coverage requirements.

## Source lifecycle and chunk coverage

Preserve `inbox → registered → extracting → extracted → verified` and the detailed gates in `99_System/Source-Registry.md`.

- Register every teacher source on receipt, including apparently unimportant supplements. No source may be skipped on relevance or priority grounds.
- Plan the full assigned extent before extraction. Short sources need one chunk; long sources need multiple chunks. Cover the final page/slide/timestamp explicitly, plus captions, figures, tables, sidebars, questions, and appendices within scope.
- Chunk states are `pending`, `extracting`, `processed`; checked-against-original is separate. `extracted` requires every chunk processed, with no omitted/unreadable content.
- `verified` requires a named human reviewer/date, comparison to original evidence, complete chunk checks, and transfer accounting for retained knowledge points. AI can prepare checks but cannot self-certify human verification.
- Every retained point needs a Concept link and reciprocal evidence, or an explicit reason that no Concept is needed. A possible link is not completed transfer.
- Unresolved extraction/accuracy gaps block source verification. A faithfully captured disagreement between sources may remain open in the Wiki without blocking source completeness; never pretend it is resolved.
- New revisions or omissions reopen the affected source/chunks and affected Concept verification. Keep Registry and Digest synchronized.

## Persistent concepts and traceability

Before creating a page, search existing names, aliases, and content for the concept. Update an existing concept when a new unit/source adds evidence. Do not create source summaries or unit-prefixed duplicates as Concept pages. Add unit names to the existing `unit` list and link the same page from all applicable Unit Maps.

Create a new page only for a genuinely distinct concept. Potential duplicates require a deliberate merge preserving evidence, student text, aliases, incoming links, and history; no automatic deletion. Synonyms become aliases when they truly refer to the same concept. Connect pages only for real conceptual relationships.

Use wiki links without `.md`. Short `[[Concept Name]]` links require unique names; otherwise use vault-relative paths. Keep existing headings stable where possible.

Each important substantive claim carries a local evidence ID such as `E01`. In Source Evidence record source ID, source title, provenance, teacher-provided flag, Digest/knowledge-point link, and original page/slide/section/timestamp. The chain is claim → evidence row → Digest point → original location. External claims need equally clear citations. AI inference is explicitly `AI-added`; source-grounded AI paraphrases keep their cited evidence origin but remain drafts until checked. An evidence citation is not proof of student understanding.

## Conflicts and classroom expectations

Never silently harmonize differences. Preserve both claims with their evidence, describe whether the difference is terminology, scope, simplification, or contradiction, and record resolution status. Teacher framing takes priority for predicting classroom expectations, not for declaring scientific truth. Preserve textbook/external nuance. Guessed exam relevance is AI inference, not teacher emphasis.

## Student authorship and verification

- Student Explanation is Justin's text. Leave it empty until supplied; do not generate or silently rewrite it. Student-authored Core Ideas should likewise be preserved. Offer suggestions separately.
- Concept `verification_status` is `draft` or `student-checked`. AI synthesis stays draft until Justin checks the current content against evidence and records date/scope. Never infer his confirmation from silence, an AI score, a source's verified status, or a review session.
- Substantive new claims, conflicts, or source revisions reset the Concept to draft. Preserve prior confirmations and unchanged student text in Update History; identify the additions requiring a check.
- AI Check refers only to the supplied student explanation: `Unchecked`, `Accurate`, `Partially Accurate`, or `Needs Revision`. Feedback must cite evidence, explain problems, and suggest what Justin should revisit. It does not replace his words or change student verification automatically.
- Source `student_checked` separately means Justin checked that Digest against its original, including important diagrams. A named adult may verify source coverage while this remains false. AI extraction is still student-unconfirmed until this check occurs.
- Keep `review_status` and `last_reviewed` for actual review, without mastery scoring. Record weak points and last tested only from real student activity. AI-suggested misconceptions are possibilities, not diagnosed student errors.

## Scope, tools, and Git

This migration authorizes architecture changes only. Do not ingest or process Biology material until separately requested. Do not create factual sample Concept pages, actual Unit Maps with invented scope, practice results, essays, or lab reports.

Do not install plugins, Dataview, graph automation, flashcard pipelines, CourseMaster, quiz automation, LaTeX, heavy OCR, ingestion watchers, external APIs, scheduled automation, or specialized agent systems in this step.

Skill-Anything is an optional replaceable extraction engine, never a core dependency. A future explicitly requested experiment must use the original `github.com/SYuan03/Skill-Anything` repository, not a fork, outside this production vault in a separate pilot and Python virtual environment. Initially test only necessary PDF/video capabilities. Evaluate coverage, chunk completeness, final-page/tail handling, citations, figures/images, and reliability; record results separately. No clone/install/test is part of this migration.

Keep secrets and temporary processing outputs out of Git. Preserve local history; no destructive reset or history erasure. Future GitHub synchronization must target a PRIVATE `Justin-Learning-OS` repository; this migration does not authorize creating a remote or publishing. Never guess credentials.
