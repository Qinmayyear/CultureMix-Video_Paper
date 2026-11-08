# Paper outline and central questions

Working title: **CulMix-Video: Evaluating Cultural Cues and Their Relations in Video**.

Working research question: **Can multimodal models recognize cultural cues and their supporting modalities, and understand how those cues are organized when cultural contexts mix in video?**

This outline follows the supplied v-HUB paper's separation of data curation, annotation, task construction, modality settings, and diagnostics. Existing section files are retained; scope and construction remain together in Section 3. The only ordering change moves the existing conclusion before the unnumbered ethics and limitations sections. No section files are renamed or removed.

| Existing file | Section and core question |
|---|---|
| `sections/00_abstract.tex` | Why cultural mixing matters; what is being designed; what the tasks diagnose; what has not yet been evaluated. |
| `sections/01_introduction.tex` | Why recognition in an isolated cultural setting does not establish understanding of mixed contexts; why video and audio matter; what this draft contributes. |
| `sections/02_related_work.tex` | Four themes: cultural recognition; cultural video/generation and evidence; mixed contexts/composition; visual relations and semantic roles. What does each cover and what remains different here? |
| `sections/03_benchmark.tex` | What culture and cultural understanding mean operationally; what qualifies as mixing; how sources, screening, cue annotation, rights review, and quality control would work. |
| `sections/04_tasks.tex` | For each core or candidate task: exact input, output, ability, metric, ambiguity handling, and dependency on annotation. |
| `sections/05_experiments.tex` | Which model families and controls should be evaluated, and under which modality conditions? No performance numbers. |
| `sections/06_analysis.tex` | Which hypotheses and failure types should future results test? Preserve result placeholders. |
| `sections/07_ethics.tex` | How should cultural association, identity, sourcing, and annotator expertise be handled? Which decisions remain pending? |
| `sections/08_limitations.tex` | What cannot be concluded from this operational definition or the current pilot? |
| `sections/09_conclusion.tex` | What does the design enable, without asserting unmeasured effectiveness? |
| `sections/10_appendix.tex` | Draft annotation fields, relation boundary cases, protocol records, and audit checklist for coauthors. |

## Conservative contribution statements

1. An operational definition of cultural mixing that includes coexistence, recontextualization, and adaptation in video.
2. A data representation connecting cultural cue instances to component types, cultural associations, and observable evidence.
3. A compact task design for recognition and modality attribution, with a candidate relation-frame and role task.
4. A planned evaluation separating recognition, evidence use, role assignment, and dependence on contextual or textual cues.

These are design contributions at this stage. Claims about dataset scale, coverage, annotation reliability, release, or model limitations require completed work and must remain TODOs.
