# Reading and maintaining this draft

Entry point: `main.tex`. Compile it with pdfLaTeX and BibTeX, or run `latexmk -pdf main.tex`. In Overleaf, select `main.tex` as the main document if a legacy ACL example is still selected. The user confirmed that this GitHub repository is connected to Overleaf; the live editor and its current main-document setting have not been independently inspected.

The manuscript uses **CulMix-Video** throughout. Its working question is whether models can identify cultural cues, attribute their evidence, and assign the roles of culturally associated elements in mixed video contexts. It includes relocation and changes of carrier, as well as fusion. Cultural associations are not exclusive national origins.

## Suggested reading order

1. `DECISIONS_AND_OPEN_QUESTIONS.md`: user-confirmed scope, working proposals, conflicts, and five author decisions.
2. `PAPER_OUTLINE.md`: each section's central question.
3. Abstract, Introduction, Scope and Definitions, and Tasks in the manuscript.
4. The three `REFERENCE_AUDIT_*.md` notes: verified sources and the specific claims each supports.

## Status conventions

- All construction procedures and model selections are proposals unless explicitly described as a prior pilot observation.
- Red `\todo{...}` marks specific decisions in drafted sections.
- Dataset Statistics, Implementation Details, Results and Analysis, Conclusion, Ethical Considerations, Limitations, and Protocol and Release Audit contain only headings.
- Core task candidates: cultural cue recognition and cue-modality attribution.
- Exploratory task: relation frames and roles. The six-frame inventory, five-frame alternative, node types, and single-versus-multiple-relation output are unresolved.
- Optional grounding, multilingual consistency, context comparisons, and compositional splits are not additional confirmed deliverables.

## Reference provenance

`references.bib` contains entries staged after primary-source verification. The staging files retain provenance comments. A few records are conservative transcriptions of verified publisher metadata, explicitly identified as such, rather than official citation exports. `minerva_stale_author_export.bib` is an audit record marked **DO NOT IMPORT** and is not loaded by the manuscript.

MINERVA-Cultural is cited under its verified proceedings title, CURVE. The paper/repository count discrepancy is documented in the cultural reference audit. This draft avoids those disputed counts. No broad claim that prior work lacks culture mixing, video grounding, or aligned modality evaluation is made.

## Files and existing work

The draft uses `main.tex`, the section files in `sections/`, and `references.bib`. The files in `sections/` include both drafted content and headings for future sections.

The draft is intentionally longer than a final submission outline. Venue-specific length, track, and ACL 2027 formatting requirements remain to be checked when preparing the submission.
