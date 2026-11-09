# Draft validation report

Date: 2026-11-09. This report concerns the manuscript and its references, not validation of the proposed benchmark.

## Build and source checks

- `main.tex` compiles with pdfLaTeX, BibTeX, and `latexmk` using the existing ACL style.
- A separate clean build using only the manuscript sources, bibliography, and ACL style files also succeeded. No pre-existing auxiliary files are required.
- The revised PDF contains 9 pages, including references and the appendix.
- All 25 cited keys resolve to bibliography entries. No duplicate keys or undefined citations remain.
- The final log reports some underfull spacing and zero overfull boxes.
- The manuscript contains 27 active `\todo{...}` markers, indexed in `TODO_INDEX.md`.
- Dataset Statistics, Implementation Details, Results and Analysis, Conclusion, Ethical Considerations, Limitations, and Protocol and Release Audit contain only headings.

## Evidence and terminology checks

- The three reference audit notes record primary sources, supported claims, publication identifiers, and version conflicts. Imported entries are official citation exports or explicitly identified transcriptions of verified metadata.
- MINERVA-Cultural/CURVE naming and count differences are documented. The stale author export is not imported.
- No CulMix-Video dataset size, annotation agreement, model result, or empirical conclusion is invented. Candidate protocols and models are explicitly identified as proposals.
- “CulMix-Video” is the manuscript name. CultureMix refers to the cited image benchmark.
- Cultural association, component type, evidence channel, cue instance, concept-level recognition, and relation node have distinct meanings.
- V means silent frames; VA means frames plus native audio; supplied text, ASR/OCR, and metadata-assisted conditions are explicit.
- Mixing includes a cultural cue with a documented carrier or receiving context. It is not restricted to fusion or to performing arts.
- Relation direction denotes role assignment rather than historical influence. Shared labels, symmetric relations, unresolved cases, and multiple possible relations remain visible design concerns.
- No cultural affiliation is inferred from a person's appearance.

## Issues retained for author decisions

The task set, culture descriptors, coverage and size target, evaluation-unit duration, annotation staffing, rights process, relation inventory, matching rules, model snapshots, and input budgets remain unresolved. The most important five decisions are collected in `DECISIONS_AND_OPEN_QUESTIONS.md`.

The user confirmed that GitHub connects this repository to Overleaf. Repository delivery does not independently verify the live Overleaf editor state. If Overleaf retains a legacy ACL template as its main document, select `main.tex`.
