# Cultural benchmark reference audit

Verified against primary sources on 2026-11-09. This is a list of recommended additions, not evidence that any CulMix-Video experiment or annotation has been completed. Publisher/author citation exports are archived separately in `verified_cultural_entries.bib`; no main bibliography is edited by this audit.

## Reliable framing

Existing work covers country-indexed cultural knowledge, multilingual visual/video QA, cultural evidence grounding, and controlled cultural mixing. The defensible distinction for CulMix-Video is its proposed combination of real videos, component-level cultural attribution, explicit evidence modalities, and candidate relation/role annotations. Do not claim that culture mixing or cultural video grounding has never been studied. A direction between annotated components is not evidence of historical cultural influence.

## Recommended sources and supported claims

### CultureMix / World in a Frame

- Eunsu Kim et al. **World in a Frame: Understanding Culture Mixing as a New Challenge for Vision-Language Models**. arXiv:2511.22787 (2025); CVPR 2026 paper also located.
- Primary: [arXiv](https://arxiv.org/abs/2511.22787), [CVPR paper](https://openaccess.thecvf.com/content/CVPR2026/papers/Kim_World_in_a_Frame_Understanding_Culture_Mixing_as_a_New_CVPR_2026_paper.pdf).
- CultureMix contains approximately 23k diffusion-generated, human-verified food images. Its four settings are food-only, food+food, food+background, and food+food+background. It tests whether food/country predictions remain consistent under mixed contexts. This directly motivates separating a target component from surrounding cultural context.
- Boundary: generated food images, not natural videos or a directed relation-labeling benchmark. Do not turn its reported background effects into our own findings. Use approximately 23k until exact split counts are reconciled with the selected paper version.
- Official CVPR citation export retrieved: key `Kim_2026_CVPR`, June 2026, pp. 2477–2489. The arXiv and proceedings year differ legitimately.

### ViMUL-Bench

- Bhuiyan Sanjid Shafique et al. **A Culturally-diverse Multilingual Multimodal Video Benchmark & Model**. EMNLP 2025, pp. 19998–20022. DOI: `10.18653/v1/2025.emnlp-main.1012`.
- Primary and official citation: [Anthology](https://aclanthology.org/2025.emnlp-main.1012/), [BibTeX](https://aclanthology.org/2025.emnlp-main.1012.bib). Key: `shafique-etal-2025-culturally`.
- Approximately 8k native-speaker-verified QA items across 14 languages and 15 categories, including eight cultural categories. Includes multiple-choice and short/long open-ended QA on videos of different lengths.
- Boundary: broad multilingual video understanding; does not establish the proposed per-component evidence-modality or culture-relation labels. Multilingual coverage alone is not a controlled same-item cross-language consistency test.

### MINERVA-Cultural / CURVE

- Darshan Singh et al. **MINERVA-Cultural: A Benchmark for Cultural and Multilingual Long Video Reasoning**. arXiv:2601.10649 (2026).
- Primary: [arXiv v2](https://arxiv.org/abs/2601.10649v2), [author repository](https://github.com/google-deepmind/neptune#minerva-cultural).
- [ArXiv v2 Section 3](https://arxiv.org/html/2601.10649v2) reports 2,400 human-authored QA pairs, 540 videos, 18 locales and six domains. Mean duration is 12.62 minutes; range: one minute to over one hour. Native-language answers and reasoning traces accompany open-ended questions; a three-level semantic judge scores answers. Say “18 locales,” since en-GB and en-IN both occur.
- Version conflict: the repository reports approximately 2,200 QA pairs and a different locale list. Its citation says CURVE/year 2025, although arXiv submission was January 2026. Use the paper's 2,400 count when citing it.
- Official CVPR export: **CURVE: A Benchmark for Cultural and Multilingual Long Video Reasoning**, key `Singh_2026_CVPR`, June 2026, pp. 32860–32871. This entry is included in `verified_cultural_entries.bib`. The stale `curve25` export is isolated in `minerva_stale_author_export.bib`; do not import it. Suggested prose: “MINERVA-Cultural (published as CURVE).”

### Cultural Moment Benchmark (CMB)

- Burak Satar et al. **Cultural Moment Benchmark: Evaluating Video Cultural Reasoning and Grounding in Southeast Asia**. EMNLP 2026, pp. 43574–43607. DOI printed by publisher: `10.18653/2026.emnlp-main.1913`.
- Primary: [Anthology and citation export](https://aclanthology.org/2026.emnlp-main.1913/), [dataset card](https://huggingface.co/datasets/Multimedia-SMU/culturalmoment-benchmark). Key: `satar-etal-2026-cultural`.
- Covers 306 concepts, seven Southeast Asian countries and five categories; the dataset card reports 624 source videos and 631 localization pairs. Three stages select a concept name from four options, select an unlabeled video moment from four options, and predict start/end times in a different example video. Reset/Carry/Feedback conditions distinguish isolated and chained reasoning.
- Boundary: its single sub-event localization output does not solve repeated, disjoint evidence intervals automatically. It studies modality ablations, which differ from requiring models to label each cue's evidence modality. The public dataset card describes staged release; do not imply every full video/annotation is openly downloadable.
- Metadata issue: Anthology exports author `Yu-Tong, Cheng`; author dataset material uses Yu-Tong Cheng. Preserve source export and check the PDF before final submission.

### CultureVidBench

- Xianjing Han et al. **CultureVidBench: Benchmarking Cultural Understanding in Text-to-Video Generation**. EMNLP 2026, pp. 49814–49832. DOI: `10.18653/2026.emnlp-main.2191`.
- Primary: [Anthology and citation export](https://aclanthology.org/2026.emnlp-main.2191/), [project](https://hanxjing.github.io/CultureVidBench/). Key: `han-etal-2026-culturevidbench`.
- 1,000 prompts span 12 countries, six continents, eight cultural regions and 14 aspects. These aspects fall under material culture, social practice/performance, and ritual/ceremony. Evaluation considers visual, visible-text, and audio cultural details in generated videos.
- Boundary: text-to-video generation evaluation, not comprehension of collected real videos. It supports multimodal cultural cue design, not a claim that our modality-attribution task already has an identical protocol.

### CulturalVQA

- Shravan Nayak et al. **Benchmarking Vision Language Models for Cultural Understanding**. EMNLP 2024, pp. 5769–5790. DOI: `10.18653/v1/2024.emnlp-main.329`.
- Primary: [Anthology](https://aclanthology.org/2024.emnlp-main.329/), [BibTeX](https://aclanthology.org/2024.emnlp-main.329.bib). Key: `nayak-etal-2024-benchmarking`.
- 2,378 image-question pairs from 11 countries on five continents, with one to five reference answers. Cultural topics include food, clothing, drinks, rituals and traditions.
- Useful for culturally grounded VQA and geographic coverage. Country labels are a dataset indexing scheme, not proof that cultures are homogeneous or mutually exclusive. This is not a culture-mix relation task.

### CVQA

- David Romero et al. **CVQA: Culturally-diverse Multilingual Visual Question Answering Benchmark**. NeurIPS 2024 Datasets and Benchmarks; arXiv:2406.05967.
- Primary: [author project and BibTeX](https://cvqa-benchmark.org/), [proceedings PDF](https://proceedings.neurips.cc/paper_files/paper/2024/file/1568882ba1a50316e87852542523739c-Paper-Datasets_and_Benchmarks_Track.pdf). Author-export key: `romero2024cvqa`.
- Approximately 10k questions across 30 countries, 31 languages and 39 country-language pairs. English/local-language versions support multilingual visual QA comparison.
- Boundary: cultural and linguistic coverage; no explicit directed cultural relations. Prefer the official proceedings citation if available; the project currently supplies an arXiv-style entry.

### GIMMICK

- Florian Schneider, Carolin Holtermann, Chris Biemann, and Anne Lauscher. **GIMMICK: Globally Inclusive Multimodal Multitask Cultural Knowledge Benchmarking**. Findings of ACL 2025, pp. 9605–9668. DOI: `10.18653/v1/2025.findings-acl.500`.
- Primary: [Anthology](https://aclanthology.org/2025.findings-acl.500/), [BibTeX](https://aclanthology.org/2025.findings-acl.500.bib). Key: `schneider-etal-2025-gimmick`.
- Six tasks across three datasets cover 728 cultural events/facets, 144 countries and six macroregions. Studies cultural knowledge through multiple modalities and geographic information.
- Useful precedent for multidimensional cultural evaluation and stratified reporting. It does not establish that nation, language and cultural affiliation are interchangeable labels.

### Seeing Culture

- Burak Satar et al. **Seeing Culture: A Benchmark for Visual Reasoning and Grounding**. EMNLP 2025, pp. 22227–22243. DOI: `10.18653/v1/2025.emnlp-main.1131`.
- Primary: [Anthology](https://aclanthology.org/2025.emnlp-main.1131/), [BibTeX](https://aclanthology.org/2025.emnlp-main.1131.bib). Key: `satar-etal-2025-seeing`.
- 1,065 images, 138 artifacts and 3,178 questions (1,093 unique), from seven Southeast Asian countries. A visual multiple-choice recognition stage precedes artifact segmentation; correct first-stage responses advance to grounding.
- Direct precedent for distinguishing recognition from evidence grounding. Its staged evaluation should not be described as our proposed multi-interval video evidence task.

### BLEnD-Vis

- Bryan Chen Zhengyu Tan et al. **BLEnD-Vis: Benchmarking Multimodal Cultural Understanding in Vision Language Models**. EACL 2026, pp. 4647–4669. DOI: `10.18653/v1/2026.eacl-long.215`.
- Primary: [Anthology](https://aclanthology.org/2026.eacl-long.215/), [BibTeX](https://aclanthology.org/2026.eacl-long.215.bib). Key: `tan-etal-2026-blend`.
- 313 templates, 16 regions, 4,916 generated/human-validated images and over 21k MCQs. Aligns Region-to-Entity text, Entity-to-Region text, and Entity-to-Region image question formats.
- Useful for consistency across question direction and modality. These question directions are not directed relations between cultural components. Do not confuse BLEnD-Vis with the earlier text-only BLEnD benchmark.

### BLEnD (text-only predecessor)

- Junho Myung et al. **BLEnD: A Benchmark for LLMs on Everyday Knowledge in Diverse Cultures and Languages**. NeurIPS 2024, volume 37, pp. 78104–78146. DOI: `10.52202/079017-2483`.
- Primary: [proceedings page](https://papers.nips.cc/paper_files/paper/2024/hash/8eb88844dafefa92a26aaec9f3acad93-Abstract-Datasets_and_Benchmarks_Track.html), [official BibTeX](https://papers.nips.cc/paper_files/paper/24495-/bibtex).
- 52.6k short-answer and multiple-choice QA pairs cover everyday cultural knowledge across 16 countries/regions and 13 languages. The countries/regions include subnational cultural contexts, illustrating why country alone is an incomplete cultural taxonomy.
- Boundary: text-only cultural knowledge, not visual/video evidence attribution or culture mixing. Include when explaining cultural granularity; BLEnD-Vis is the more direct multimodal task reference.

### MMAC

- Weihua Zheng et al. **MMAC: A Multilingual, Multimodal Alignment Framework for Cultural Grounding Evaluation**. ACL 2026, pp. 21667–21709. DOI: `10.18653/v1/2026.acl-long.989`.
- Primary: [Anthology and official export](https://aclanthology.org/2026.acl-long.989/). Key: `zheng-etal-2026-mmac`.
- 27,000 human-curated questions cover eight Asian countries and ten languages, with aligned text, image and speech inputs. The protocol includes cross-country differences, cross-language/modal consistency, generalization and grounding validity. Multiple-choice answers are accompanied by generated explanations.
- Highly relevant to modality controls. Do not claim that all prior cultural benchmarks lack aligned cross-modal testing; MMAC explicitly supplies it. Our distinction must concern component-specific attribution in natural video and relations, not multimodality alone.

### When Cultures Move

- Shuowei Li, Yuming Zhao, Parth Bhalerao, and Oana Ignat. **When Cultures Move: Measuring and Improving Multicultural Text-to-Video Generation**. NLP4PI 2026, pp. 575–591. DOI: `10.18653/2026.nlp4pi-1.42`.
- Primary: [Anthology and official export](https://aclanthology.org/2026.nlp4pi-1.42/). Key: `li-etal-2026-cultures`.
- 243 prompts and 972 generated videos cover Chinese, American and Romanian cultures, three action categories, and mono-/cross-cultural settings. Evaluation uses CLIP-based measures, VLM judging and video-quality measures. MAVEN refines person, action and location dimensions.
- Closely related to culturally different performers, actions and settings. Distinguish its controlled generated-video representation task from interpreting cultural relations in collected videos. Avoid claiming that multi-culture video scenarios have never been benchmarked.

## Drafting checks

- All exact dataset numbers above describe the cited works, not CulMix-Video.
- Prefer narrow contrast statements over “first,” “no prior benchmark,” or universal absence claims.
- The examples considered in chat have not been independently verified by this reference audit.
- The earlier user reference to “five types” does not itself establish a finalized taxonomy; locate the actual notes or leave a TODO.
- Candidate directed labels need a pilot agreement study. Recognition, evidence attribution, localization, and cultural interaction must remain distinct concepts.
