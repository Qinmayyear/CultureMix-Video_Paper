# CulMix-Video drafting decisions

Date: 9 November 2026. This is an author discussion record, not a completed experimental protocol.

## Confirmed by the user or visible in the project

- The target is ACL 2027. The submission track, final formatting rules, and deadline still need confirmation.
- The study concerns cultural mixing in video. Mixing includes coexistence, changes in performer or setting, and adaptation; technical fusion is not required.
- The full dataset should extend beyond performing arts. Performing arts and media adaptations were a search pilot.
- The user prefers a few meaningful tasks. Directed relation and role classification is an explicitly favored research direction, but its ontology has not been approved.
- Previous conversation reports 30 collected candidate links. Those are retrieval candidates, not a verified dataset size or completed annotation study.
- The user reported three potentially suitable examples among 30 manually inspected search results in an earlier search experiment. This is an informal observation, not a controlled comparison of search methods.
- The current paper is an ACL review-mode scaffold with section files and an empty bibliography. Existing unrelated Git deletions and untracked outputs belong to the user and must remain untouched.

## Working design inferred from the discussion

- Research question: Can multimodal models identify culturally associated elements, locate their supporting modalities, and distinguish their roles when several cultural contexts appear in the same video?
- Use specific cue instances and their participating entities or contexts as relation nodes. Cultural associations, component types, and evidence channels are separate attributes. Recognition currently proposes concept-level aggregation; relation prediction needs instance IDs, so these are distinct outputs.
- Cue recognition and modality attribution are the strongest candidates for the core tasks. These are proposals supported by discussion, not a finalized task list.
- Use culture association rather than requiring a unique historical origin. Countries, communities, languages, traditions, and religions are overlapping descriptors, not a mandatory geographical tree.
- Use relation-specific argument roles for asymmetric relations. Preserve symmetric coexistence and fusion. Direction describes organization within the observed sample, not historical influence.
- Keep video-internal evidence separate from uploader metadata. Linguistic labels describe evidence, not a person's nationality.
- Reuse the existing section files. Follow v-HUB's progression from scope to curation, annotations, derived tasks, modality settings, and diagnostics. Retain the current early Related Work section for easy review.

## Conflicts and provisional choices

| Issue | Conflicting proposals | Draft treatment |
|---|---|---|
| Number of frames | Five frames with carrier included in embedding versus six with separate realization | Present six as candidate labels; explicitly consider merging embedding and realization after annotation. |
| Culture labels | Earlier rigid region-country-community tree versus shared and transnational traditions | Use multiple supported associations and optional levels; do not force a tree. |
| Temporal scope | Source videos of 10 seconds to 30 minutes versus short benchmark clips | Treat source filtering and evaluation units separately; final clip policy remains open. |
| Input modalities | Earlier use of `video-only` sometimes included audio | Use V for silent frames, VA for frames plus native audio, and explicit T for supplied text; embedded visual text remains part of V. |
| Relation evidence | Names of cues may make roles obvious without watching | Add cue-text-only controls and matched alternatives; oracle cues are diagnostic, not proof of video understanding. |
| Relation nodes | Two cue instances versus a cue and a documented carrier/context | Permit participating entities and contexts as nodes; require separate evidence for their cultural associations. Synthesis result nodes remain open. |
| Co-presence | Independent symmetric relation versus a residual fallback | Draft treats it as independent and compatible with other frames; keep the fallback alternative explicit for the pilot. |
| Answerability | One gold label set versus different evidence available in V and VA | Propose condition-specific answerability masks; do not penalize silent-frame models for audio-only cues as ordinary recognition misses. |
| Context invariance | Natural videos with the same form versus strict counterfactual pairs | Call natural pairs matched comparisons; causal invariance requires an intervention that preserves the target. |
| Related work | Previous chat supplied specific publication and dataset claims | Recheck primary sources; retain only verified references. Unverified details stay out of the paper. |

## How the attachments inform this draft

The supplied v-HUB PDF separates collection/filtering, rich annotations, task construction, modality settings, and analysis. It labels whether a cue contributes to the target phenomenon, rather than merely whether the cue is present. We adopt that separation without copying its humor tasks, short-clip limits, annotator counts, or findings.

The supplied world-modelling guidelines emphasize observable actions, local practices, overlapping language/region labels, and separate scene descriptions from cultural notes. These inform our operational definition. Its 8–15 second clips, prefix/suffix prediction, single primary category, per-item quota, and staffing requirements are not decisions for CulMix-Video.

## Five decisions needed from the authors

1. What is the release scope: which cultural descriptors and non-performance domains, and what dataset target is realistic after audiovisual verification?
2. Which tasks are mandatory: cue recognition and modality attribution only, or also relation-frame and role classification after a pilot?
3. What is the evaluation unit and evidence policy: clips or full videos, native audio, supplied subtitles, and metadata-dependent cases?
4. What human annotation resources are available: relevant cultural expertise, annotator count per item, languages, compensation, adjudication, and rights review?
5. Which model families, exact checkpoints/API versions, input budgets, and train/dev/test or test-only setting are feasible?

## Source and completion status

The bibliography begins empty. Recommended additions are listed with verified identifiers in the reference audit notes before their official entries are imported. No experiments or annotation agreements have been measured for this draft. All unsettled manuscript details must retain visible `\todo{...}` markers.

The supplied directory is a local GitHub checkout. The user confirmed during drafting that this GitHub repository is connected to Overleaf and asked us to continue without waiting for replies. Use the existing repository as the delivery route. Do not claim that the live Overleaf UI was independently checked.
