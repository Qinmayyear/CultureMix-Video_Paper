# Model and evaluation-reference audit

Checked on 2026-11-09. This note lists proposed additions before their staging in `verified_model_entries.bib`. No model has been evaluated for CulMix-Video. The shortlist is a reproducible starting point, not a claim that these are the newest or strongest models.

| Proposed citation key | Verified reference | Primary source and identifier | Supported use in this draft |
| --- | --- | --- | --- |
| `bai2025qwen25vl` | Shuai Bai et al. (2025), *Qwen2.5-VL Technical Report* | [arXiv:2502.13923](https://arxiv.org/abs/2502.13923), DOI `10.48550/arXiv.2502.13923`; [official citation block](https://github.com/QwenLM/Qwen3-VL#citation) | Candidate open visual model with video input. The Qwen2.5-VL repository now redirects to Qwen3-VL, but retains the Qwen2.5-VL citation block. |
| `xu2025qwen25omni` | Jin Xu et al. (2025), *Qwen2.5-Omni Technical Report* | [arXiv:2503.20215](https://arxiv.org/abs/2503.20215), DOI `10.48550/arXiv.2503.20215`; [official citation block](https://github.com/QwenLM/Qwen2.5-Omni#citation) | Candidate native audiovisual model. The report and repository explicitly support text, images, audio, and video. |
| `wang2025internvl35` | Weiyun Wang et al. (2025), *InternVL3.5: Advancing Open-Source Multimodal Models in Versatility, Reasoning, and Efficiency* | [arXiv:2508.18265](https://arxiv.org/abs/2508.18265), DOI `10.48550/arXiv.2508.18265`; [official citation block](https://github.com/OpenGVLab/InternVL#citation) | A second candidate open visual model. The official repository includes video inference examples. No native-audio support is assumed. |
| `shi2025vhub` | Zhengpeng Shi, Yanpeng Zhao, Jianqun Zhou, Yuxuan Wang, Qinrong Cui, Wei Bi, Songchun Zhu, Bo Zhao, and Zilong Zheng (2025), *v-HUB: A Benchmark for Video Humor Understanding from Vision and Sound* | [arXiv:2509.25773](https://arxiv.org/abs/2509.25773), DOI `10.48550/arXiv.2509.25773`; supplied `Notes/v-Hub.pdf` and [v3 HTML](https://arxiv.org/html/2509.25773v3) | Precedent for separately evaluating text descriptions, silent video frames, and video plus audio. This does not establish the effectiveness of the same design for culture mixing. |

## Checkpoint candidates

- [Qwen/Qwen2.5-VL-7B-Instruct](https://huggingface.co/Qwen/Qwen2.5-VL-7B-Instruct): official model card checked. Candidate for the visual condition; checkpoint revision remains to be frozen.
- [OpenGVLab/InternVL3_5-8B](https://huggingface.co/OpenGVLab/InternVL3_5-8B): official model card checked. Candidate for the visual condition; checkpoint revision remains to be frozen.
- `Qwen/Qwen2.5-Omni-7B`: official repository documents this checkpoint and inference using video with audio. Candidate for native audiovisual input; checkpoint revision remains to be frozen.
- Proprietary APIs: leave as placeholders until available endpoints, modality support, cost, and stable version identifiers are checked at experimental freeze. Do not inherit API identifiers from v-HUB without rechecking them.

## Bibliographic handling

- The staged Qwen2.5-VL entry reproduces the official citation metadata, with a project-local citation key and braces protecting the model name.
- The staged Qwen2.5-Omni entry reproduces the official title, authors, year, and arXiv identifier. Its official citation block separates authors with commas; the staged entry changes those separators to BibTeX `and` so authors render correctly. This is a syntax correction, not a change to authorship.
- The staged InternVL3.5 entry reproduces the official citation block, including its abbreviated author list ending in `and others`; only the key and title capitalization protection differ.
- The v-HUB arXiv BibTeX endpoint could not be retrieved. Its staged entry is a minimal record transcribed from the supplied paper and verified arXiv metadata, not an official export. The paper was first submitted in 2025; the inspected version is v3, revised 2026-06-01. This explains the 2025 reference year. No publication venue is asserted.
- The draft uses only the model families' input capabilities and v-HUB's modality-separated evaluation design. It does not transfer reported scores, model rankings, or experimental settings to CulMix-Video.

## Decisions still pending

Final model list; checkpoint revisions and API snapshots; supported input combinations; frame, audio, and generation budgets; hardware and total cost; prompts; any ASR/OCR systems; and whether to include a supplied-text diagnostic. All remain proposed and are marked in the manuscript.
