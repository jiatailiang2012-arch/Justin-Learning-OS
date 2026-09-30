# Persistent Concept Wiki Migration — 2026-09-30

## Audit of the Existing Vault

Inspected every existing vault file before proposing changes. The baseline contains 12 files: README, .gitignore, Source Registry, three templates, and six .gitkeep placeholders. There are no learning materials, source rows, actual Concept Notes, Unit Maps, or student explanations. No AGENTS.md exists in the vault or inspected ancestor directories. No Obsidian configuration is present in this vault.

The existing design already separates source coverage from concept understanding, tracks chunks, requires original-location evidence, and reserves student explanation space. Its original label is Version 2; preserve that historical label in Git. The new brief treats this existing foundation as V0.x in a longer production progression; this is a terminology change, not a rebuild.

At audit time Git existed on branch `master`, with no commits or remote; all 12 baseline files were untracked and no author identity was configured. The user subsequently supplied their GitHub account. Its public API returned login `jiatailiang2012-arch`, ID `289009586`, and a 2026 creation date. Using GitHub's documented ID-based noreply format, configured only this repository with name `jiatailiang2012-arch` and email `289009586+jiatailiang2012-arch@users.noreply.github.com`. No real email, credentials, global identity settings, remote, or publication were needed.

References: [public account](https://github.com/jiatailiang2012-arch), [GitHub noreply format](https://docs.github.com/en/account-and-profile/reference/email-addresses-reference). Original foundation preserved before modification in commit `a4aa018` (12 original files). The audit report is included with the migration, not in that baseline.

## KEEP

- All existing top-level folders and Biology subfolders; no cosmetic renaming.
- Source Registry as the authoritative coverage record, including its five lifecycle states.
- Source Digest as evidence of each source's complete contents, including chunk gates and retained teacher details.
- Existing templates and useful sections; modify them in place.
- Stable source IDs, source-to-concept transfer accounting, original locations, and provenance history.
- Student-authored explanation space and the distinction between teacher provision and teacher emphasis.
- Practice, Mistakes, and Output folders as dormant future capacity.
- .gitignore and all .gitkeep files.

## MODIFY

- README: describe Biology Units 1–3 as the pilot and persistent concepts as the knowledge architecture.
- Source Registry: extend provenance to include `textbook`; add an independent Teacher Provided flag so assigned textbooks remain in coverage totals. Preserve old origin values rather than silently relabeling them.
- Source Digest: mirror the provenance/coverage distinction, preserve immutable originals, and require transfer to an existing concept where appropriate.
- Biology Concept template: add aliases, cross-unit update rules, claim-level evidence with source titles, student verification, separate AI feedback, explicit teacher/textbook conflicts, and a small change history. Retain useful Biology sections.
- Unit Map template: reference persistent concepts across units, count teacher-provided materials independently of origin, and expose pending student verification.

## MOVE

None proposed. There is no content requiring relocation.

## DELETE

None proposed. No deletion is necessary.

## ADD

- AGENTS.md as the authoritative operating specification for this school-learning vault.
- This dated audit/migration report.
- A Raw subfolder under 01_Sources/Biology for future immutable originals; existing Source Digest locations remain stable.

## Decisions Implemented

1. **Provenance and course coverage are separate facts.** Allowed origins become `teacher`, `textbook`, `external`, and `AI-added`. Teacher Provided uses yes/no/unknown in the Registry and true/false/null in Digest frontmatter. Legacy teacher rows map to yes without changing their origin. Unknown assignments require reconciliation and cannot silently disappear from coverage. Actual source authorship and claim-level attribution must remain visible.
2. **One persistent page per distinct concept.** Search names, aliases, and existing content before creating a page. Add evidence and unit references to the existing page. Do not create a new page just because a later unit revisits the topic. Potential duplicate pages require a deliberate merge preserving student text, evidence, and links.
3. **Coverage verification is not student verification.** Registry `verified` means a named human has checked coverage and transfer against the original. AI-only checks cannot self-certify that gate. Concept synthesis remains draft until Justin checks it; AI feedback on his explanation is a separate assessment, not permission to rewrite it.
4. **Preserve conflicts.** Record both claims, their sources and locations, classroom implications, and unresolved questions. Teacher framing helps anticipate school expectations; it does not erase textbook or scientific nuance or establish scientific truth by itself.
5. **Keep the workflow manual.** Practice, Mistakes, and Output may later cite persistent Concepts and their evidence. No automation, fabricated learning records, or mastery scoring is needed now.
6. **Defer extraction-engine experiments.** The brief's Skill-Anything experiment is a future separate pilot using the original SYuan03/Skill-Anything repository, outside this vault, in a virtual environment, with only required PDF/video capabilities. Record coverage, chunk/tail handling, citations, figures, and reliability separately. This migration does not install or test it.

## Validation Results

- PASS: all 12 baseline files still exist; no deletion or relocation. .gitignore and all six original placeholders remain unchanged.
- PASS: Registry has its original 18 columns plus Teacher Provided (19 total). Markdown table widths align across documents.
- PASS: all three template frontmatter key sets match the intended schema, without duplicate keys. The added fields use plain YAML strings, lists, and null; no plugins are needed.
- PASS: all 10 actual wiki links resolve, including heading targets. Code-formatted example links remain explicit placeholders, not fabricated content.
- PASS: Git whitespace checks; no learning materials or generated Biology content exist in Inbox, Sources, Knowledge, Practice, Mistakes, or Output.
- PASS: manual rule review separates source coverage, student source checking, Concept verification, AI assessment, and review status. Every important substantive claim has a defined evidence chain containing ID, title, provenance, Digest point, and original location.

### Scenario Walkthrough (Rules Only)

| Scenario | Expected Path in Updated Rules | Result |
| --- | --- | --- |
| Teacher assigns a textbook | origin=textbook, Teacher Provided=yes; counted in unit source coverage | Supported |
| Teacher assignment is unknown | Keep it visible as a reconciliation issue; do not declare complete coverage | Supported |
| Final page/slide chunk is missing | Chunks Done stays below total; extracted and verified gates fail | Supported |
| Unit 3 extends a Unit 1 concept | Search names/aliases/content; update the same page, unit list, and evidence; both maps link there | Supported |
| Teacher and textbook disagree | Preserve both evidence-backed claims and record classroom framing separately from scientific nuance | Supported |
| AI synthesizes from verified sources | Concept stays draft until Justin checks it; source status alone cannot confirm understanding | Supported |
| Justin supplies an explanation | Preserve his exact words; assess separately in AI Check with reasons/evidence | Supported |
| A checked Concept receives new claims | Preserve earlier confirmation/student words; reopen draft verification and log pending additions | Supported |
| Future practice exposes a weakness | Link observed response and evidence to the same persistent Concept; do not invent scores | Supported as a manual future workflow |

These are architecture/consistency checks, not real extraction or learning trials. No Biology materials were processed, no duplicates were actually merged, and no student explanation was assessed.

## Execution Status

Audit, preservation, migration, and structural validation are complete. Updated the five existing documentation/template files in place. Added AGENTS.md, this report, and one Raw folder placeholder. Preserved all other files and folders. The migration is saved as a separate local Git commit after the baseline; no remote is configured.

## Deliberately Deferred

No Biology ingestion/extraction, actual Concept or Unit Map population, student assessment, quiz/mistake automation, mastery scoring, plugins, Dataview, flashcards, LaTeX, OCR/video pipelines, APIs, watchers, agents, or scheduled work. No Skill-Anything clone, installation, dependency, or pilot execution. No GitHub repository creation or push. Practice/Mistakes/Output remain dormant.

## Current Folder Tree

```text
Justin-Bio-Learning-OS/
├── .git/                         (local history; generated internals omitted)
├── .gitignore
├── AGENTS.md
├── README.md
├── 00_Inbox/
│   └── .gitkeep
├── 01_Sources/
│   └── Biology/
│       ├── .gitkeep
│       └── Raw/
│           └── .gitkeep
├── 02_Knowledge/
│   └── Biology/
│       └── .gitkeep
├── 03_Practice/
│   └── Biology/
│       └── .gitkeep
├── 04_Mistakes/
│   └── Biology/
│       └── .gitkeep
├── 05_Output/
│   └── Biology/
│       └── .gitkeep
├── 90_Templates/
│   ├── Biology-Concept.md
│   ├── Source-Digest.md
│   └── Unit-Map.md
└── 99_System/
    ├── Migration-Audit-2026-09-30.md
    └── Source-Registry.md
```

## Readiness and Open Questions

Ready at the architecture/template level for a separately authorized Biology Units 1–3 intake. Completeness, extraction quality, study usefulness, and Justin's understanding cannot be claimed until real sources and student activity have been checked.

No unresolved structural blocker remains. Exact unit titles, full teacher-distribution channels, source inventory, scope statements, and the person performing human coverage review remain intake details to establish later. The two design ambiguities (authorship versus teacher assignment, and source verification versus student verification) are resolved explicitly in AGENTS.md and the templates. Stop here; do not ingest materials as part of this migration.
