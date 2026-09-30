# Justin Learning OS

Persistent concept-based learning wiki for high-school Honors Biology. Biology Units 1–3 are the first pilot; concepts should continue accumulating across later units. The earlier Version 2 foundation is preserved in Git as the existing V0.x starting point, not discarded.

**Coverage is guaranteed at the Source layer. Understanding is built at the Concept layer.**

Open this existing project directory as an Obsidian vault. Its current folder name is `Justin-Bio-Learning-OS`; the intended future private GitHub repository name is `Justin-Learning-OS`. No nested vault is needed.

[[AGENTS|Operating specification]] is the authoritative project guide. See [[99_System/Migration-Audit-2026-09-30|Migration audit and validation]] for changes and boundaries. This vault is Justin's school-learning system, not a family, medical, or research knowledge base.

## Vault layout

- `00_Inbox/`: newly received originals awaiting filing; register them immediately.
- `01_Sources/Biology/`: one Source Digest per source; immutable originals live separately in `Raw/`.
- `02_Knowledge/Biology/`: persistent Concept pages shared across units, plus Unit Maps as entry points.
- `03_Practice/Biology/`, `04_Mistakes/Biology/`, `05_Output/Biology/`: dormant; future items link to persistent Concepts and their evidence.
- `90_Templates/`: manual templates for Digests, Concepts, and Unit Maps.
- `99_System/`: [[99_System/Source-Registry|Source Registry]] and coverage rules.

## Manual workflow

1. Register every teacher-provided source on receipt, including apparently unimportant supplements. Preserve its original file or original URL; for changeable online material, retain a dated copy when possible and record any preservation gap.
2. Assign a stable unique ID such as `BIO-S001`. Copy [[90_Templates/Source-Digest|Source Digest]] to `01_Sources/Biology/BIO-S001 - Short Title.md`. Preserve the original contents in `01_Sources/Biology/Raw/`, with an identifiable filename such as `BIO-S001 - Original Title.pdf`. Never overwrite originals; keep revisions separately.
3. Record the full source extent, plan chunks covering it without gaps, then extract every chunk. A short source still uses one chunk. Update the Digest and Registry together.
4. Compare extraction with the original. Account for each retained knowledge point in the Concept Transfer Check, linking to a Concept or explaining why none is needed.
5. Search existing Concept names, aliases, and content first. Update the existing page when a later source/unit adds information. Use [[90_Templates/Biology-Concept|Biology Concept]] to create `02_Knowledge/Biology/Concept Name.md` only for a distinct concept. Add units to its list instead of creating unit-specific duplicates. Attach evidence IDs to claims and preserve conflicting source statements.
6. Copy [[90_Templates/Unit-Map|Unit Map]] to `02_Knowledge/Biology/Unit Name - Unit Map.md`. List every teacher source, including incomplete ones. Reconcile coverage weekly and before tests.
7. Justin checks the concept against evidence and writes his own explanation. AI gives feedback separately. Keep AI synthesis marked draft until Justin confirms it; new substantive information reopens this check. Later practice can identify weak concepts and feed back into the same pages.

## Conventions and human thinking

- Source origins are `teacher`, `textbook`, `external`, or `AI-added`. For new entries, distinguish authorship/material origin from the separate Teacher Provided flag. An assigned textbook is `textbook` with Teacher Provided `yes`; an assigned outside article is `external` with `yes`. Legacy `teacher` entries keep their origin and map to `yes`. Never silently relabel provenance; preserve original authorship and change history.
- Teacher-provided does not mean teacher-emphasized. Record emphasis or assignment intent only with explicit evidence; otherwise use `unknown`.
- Use vault-relative wiki links without `.md`, for example `[[02_Knowledge/Biology/Concept Name|Concept Name]]`. Short `[[Concept Name]]` links are fine when names are unique. Cite Digest headings and original locations together.
- Use the same source ID, unit name, origin, teacher-provided flag, and status in the Registry and Digest. Use ISO dates (`YYYY-MM-DD`). `student_checked` is a YAML boolean; `teacher_provided` uses `true`, `false`, or `null` (unknown). Corresponding table flags use `yes`, `no`, or `unknown`.
- Use `unknown` for unknown scope/intent, `none` for confirmed absence, and `not applicable — reason` where a content category does not apply. Empty templates are not completed checks.
- Source `verified` means a named human checked coverage and transfer; it does not certify Justin's understanding. AI extraction remains student-unconfirmed until his source check. Concept AI synthesis has its own `verification_status: draft` until Justin checks it. Preserve Student Explanation and student-written Core Ideas; put AI feedback in AI Check. Check important diagrams against originals.
- Claims cite evidence IDs mapped to source IDs, titles, provenance, Digest points, and original locations. Teacher/textbook/external disagreements remain visible; teacher framing predicts classroom expectations but does not override scientific nuance.
- All counts and checks are manual in this pilot. Templates describe required gates; they do not automatically enforce them. An empty Registry proves no coverage until reconciled with teacher distribution channels. Unknown teacher assignments remain visible blockers to declaring coverage complete.

## Scope and Git

Supported future source types include textbook PDFs, scanned pages, teacher PDFs, slides, photographed handouts, worksheets, lab instructions, diagrams, images, webpages, online articles, videos, study guides, oral teacher notes, and other supplements. Use pages, slides, timestamps, headings, image regions, question numbers, or dated note sections as appropriate locations.

This migration does not ingest or process learning materials, install tools, create lab reports or essays, or implement quizzes, mistake automation, mastery scoring, Anki, Dataview, LaTeX, NotebookLM, transcription, OCR pipelines, APIs, or scheduled automation. The architecture is ready for a separately authorized Units 1–3 intake; its real learning usefulness remains to be tested with those materials and Justin.

Skill-Anything remains a future optional experiment using the original SYuan03 repository, outside this vault in a separate pilot and Python virtual environment. Start with only needed PDF/video capabilities, then assess coverage, chunk/end handling, citations, figures, and reliability. No installation or evaluation is part of this migration; the wiki remains independent of any extraction engine.

Git tracks Markdown, originals intentionally retained for versioning, and `.gitkeep` placeholders for empty folders. Keep passwords, API keys, secrets, caches, and temporary processing files out of Git. `.gitignore` is a safeguard, not a secret detector; inspect staged changes before any future commit or push. No GitHub connection or publication is part of this setup. Any future repository must be private and named `Justin-Learning-OS`.
