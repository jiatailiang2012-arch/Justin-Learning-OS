# Justin Learning OS

Version 2: the Source and Concept foundation for high-school Honors Biology.

**Coverage is guaranteed at the Source layer. Understanding is built at the Concept layer.**

Open this existing project directory as an Obsidian vault. Its current folder name is `Justin-Bio-Learning-OS`; the intended future private GitHub repository name is `Justin-Learning-OS`. No nested vault is needed.

## Vault layout

- `00_Inbox/`: newly received originals awaiting filing; register them immediately.
- `01_Sources/Biology/`: preserved originals and one Source Digest per source.
- `02_Knowledge/Biology/`: Concept Notes and Unit Maps.
- `03_Practice/Biology/`, `04_Mistakes/Biology/`, `05_Output/Biology/`: reserved for later versions.
- `90_Templates/`: manual templates for Digests, Concepts, and Unit Maps.
- `99_System/`: [[99_System/Source-Registry|Source Registry]] and coverage rules.

## Manual workflow

1. Register every teacher-provided source on receipt, including apparently unimportant supplements. Preserve its original file or original URL; for changeable online material, retain a dated copy when possible and record any preservation gap.
2. Assign a stable unique ID such as `BIO-S001`. Copy [[90_Templates/Source-Digest|Source Digest]] to `01_Sources/Biology/BIO-S001 - Short Title.md`. Keep original filenames identifiable; a companion original can use `BIO-S001 - Original Title.pdf`.
3. Record the full source extent, plan chunks covering it without gaps, then extract every chunk. A short source still uses one chunk. Update the Digest and Registry together.
4. Compare extraction with the original. Account for each retained knowledge point in the Concept Transfer Check, linking to a Concept or explaining why none is needed.
5. Copy [[90_Templates/Biology-Concept|Biology Concept]] to `02_Knowledge/Biology/Concept Name.md` as needed. Several sources may support one Concept. Preserve claim-level provenance and locations.
6. Copy [[90_Templates/Unit-Map|Unit Map]] to `02_Knowledge/Biology/Unit Name - Unit Map.md`. List every teacher source, including incomplete ones. Reconcile coverage weekly and before tests.

## Conventions and human thinking

- Source origins are exactly `teacher`, `external`, or `AI-added`. Origin describes how material entered the course collection; a teacher-assigned outside article is `teacher`, with its author/URL retained. Independently added references are `external`; AI additions are `AI-added`.
- Teacher-provided does not mean teacher-emphasized. Record emphasis or assignment intent only with explicit evidence; otherwise use `unknown`.
- Use vault-relative wiki links without `.md`, for example `[[02_Knowledge/Biology/Concept Name|Concept Name]]`. Short `[[Concept Name]]` links are fine when names are unique. Cite Digest headings and original locations together.
- Use the same source ID, unit name, origin, and status in the Registry and Digest. Use ISO dates (`YYYY-MM-DD`); leave unknown template values empty. Use YAML booleans for `student_checked`; table flags use `yes`, `no`, or `unknown`.
- Use `unknown` for unknown scope/intent, `none` for confirmed absence, and `not applicable — reason` where a content category does not apply. Empty templates are not completed checks.
- AI extraction remains a draft until verified. Core Ideas should be student-written or student-confirmed. Student Explanation belongs to the student. Important diagrams should eventually be checked against originals by the student; record pending student checks honestly.
- All counts and checks are manual in Version 2. Templates describe required gates; they do not automatically enforce them. An empty Registry proves no coverage until reconciled with teacher distribution channels.

## Scope and Git

Supported future source types include textbook PDFs, scanned pages, teacher PDFs, slides, photographed handouts, worksheets, lab instructions, diagrams, images, webpages, online articles, videos, study guides, oral teacher notes, and other supplements. Use pages, slides, timestamps, headings, image regions, question numbers, or dated note sections as appropriate locations.

Version 2 does not ingest or process learning materials, install tools, create lab reports or essays, or implement quizzes, mistake automation, mastery scoring, Anki, Dataview, LaTeX, NotebookLM, transcription, OCR pipelines, APIs, or scheduled automation. External engines and repositories, including Skill-Anything, are not dependencies of this vault.

Git tracks Markdown, originals intentionally retained for versioning, and `.gitkeep` placeholders for empty folders. Keep passwords, API keys, secrets, caches, and temporary processing files out of Git. `.gitignore` is a safeguard, not a secret detector; inspect staged changes before any future commit or push. No GitHub connection or publication is part of this setup. Any future repository must be private and named `Justin-Learning-OS`.
