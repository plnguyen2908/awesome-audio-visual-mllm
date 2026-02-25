# Awesome AudioVisual QA [![Awesome](https://awesome.re/badge.svg)](https://github.com/plnguyen2908/awesome-audio-visual-mllm)

A curated list of **audio-visual multimodal large language models (MLLMs)**, **benchmarks**, and **resources** for **video + audio + language** understanding and reasoning.

> Scope: This repository focuses on works involving **both audio and visual signals** (video/image), with language understanding/generation. 

> It also includes modern **MLLM evaluation benchmarks** for video analysis (especially those using audio): typically QA problems in audiovisual setting. Benchmarks that include subtitle without audio are excluded from the list. 

---

## Table of Contents

- [What is included](#what-is-included)
- [Benchmarks](#benchmarks)
  - [Pre-MLLM-eval era (< 2024)](#pre-mllm-eval-era--2024)
  - [MLLM-eval era (>= 2024)](#mllm-eval-era--2024)
- [Models](#models)
  - [Open-source](#open-source)
  - [Closed-source / API-based](#closed-source--api-based)
- [Datasets (optional split)](#datasets-optional-split)
- [Evaluation dimensions (suggested)](#evaluation-dimensions-suggested)
- [Contributing](#contributing)
- [License](#license)

---

## What is included

### ✅ Include
- **Audio-visual reasoning / QA datasets** (e.g., AVQA-style tasks)
- **Benchmarks for evaluating MLLMs on audiovisual inputs**
- **Models** that support **audio + visual + language** inputs/outputs

### ❌ Exclude (unless strongly relevant)
- Pure image-only benchmarks
- Pure ASR / speech-only benchmarks
- Pure video benchmarks with no meaningful audio relevance

---

## Benchmarks

### Pre-MLLM-eval era (< 2024)

> Foundational audio-visual QA/reasoning datasets and tasks.  
> These are highly relevant to AV perception/reasoning, but were **not primarily designed as comprehensive MLLM evaluation benchmarks**.

| Paper | Benchmark Name | Authors | Venue | Modalities | Code  | Data |
|---|---|---|---|---|---|---|
| [**PACS: A Dataset for Physical Audiovisual CommonSense Reasoning**](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136970286.pdf) | PACS | Yu, S.; Wu, P.; Liang, P. P.; Salakhutdinov, R.; Morency, L. P. | ECCV 2022 | Video + Audio | [Code](`https://github.com/samuelyu2002/PACS`) | [Data](`https://drive.google.com/drive/folders/1TjOKBTU9dsytHJIb919V4wXFR1Zm5TsJ`) |
| [**Learning To Answer Questions in Dynamic Audio-Visual Scenarios**](https://openaccess.thecvf.com/content/CVPR2022/papers/Li_Learning_To_Answer_Questions_in_Dynamic_Audio-Visual_Scenarios_CVPR_2022_paper.pdf) | MUSIC-AVQA |Li, G.; Wei, Y.; Tian, Y.; Xu, C.; Wen, J. R.; Hu, D. | CVPR 2022 | Video + Audio | [Code](https://github.com/GeWu-Lab/MUSIC-AVQA) | [Data](https://drive.google.com/drive/folders/1WAryZZE0srLIZG8VHl22uZ3tpbGHtsrQ) |
| [**AVQA: A Dataset for Audio-Visual Question Answering on Videos**](https://dl.acm.org/doi/10.1145/3503161.3548291) | AVQA | Yang, P.; Wang, X.; Duan, X.; Chen, H.; Hou, R.; Jin, C.; Zhu, W. | ACM MM 2022 | Video + Audio | [Code](https://github.com/GeWu-Lab/MUSIC-AVQA) | [Data](https://drive.google.com/drive/folders/1WAryZZE0srLIZG8VHl22uZ3tpbGHtsrQ) |

---

### MLLM-eval era (>= 2024)

> Benchmarks explicitly designed to evaluate modern multimodal LLMs (MLLMs), often with broader task coverage and richer analysis.

| Paper | Benchmark Name | Authors | Venue | Modalities | Code | Task | Data |
|---|---|---|---|---|---|---|---|
| [**WorldSense: Evaluating Real-world Omnimodal Understanding for Multimodal LLMs**](https://arxiv.org/abs/2502.04326) | WorldSense | Hong, J.; Yan, S.; Cai, J.; Jiang, X.; Hu, Y.; Xie, W. | ICLR 2026 | Video + Audio + Text | [Code](https://github.com/JaaackHongggg/WorldSense) | Omnimodal understanding & reasoning (MCQ QA) | - |
| [**Daily-Omni: Towards Audio-Visual Reasoning with Multimodal Language Models**](https://arxiv.org/abs/2505.17862) | Daily-Omni | Zhou, Z. et al. | arXiv | Video + Audio | [Code](https://github.com/lliar-liar/daily-omni) | Audio-visual reasoning (daily-life QA) | - |
| [**AVUT (Audio-centric Video Understanding Test)**](https://aclanthology.org/volumes/2025.emnlp-main/) | AVUT | TBD (EMNLP 2025 paper metadata) | EMNLP 2025 | Video + Audio | - | Audio-centric video understanding | - |
| [**AV-Odyssey**](https://arxiv.org/) | AV-Odyssey | TBD | arXiv | Video + Audio | - | Audio-visual perception & reasoning | - |
| [**OmniVideoBench: Towards Audio-Visual Understanding Evaluation for Omni MLLMs**](https://arxiv.org/abs/2510.10689) | OmniVideoBench | Li, C. et al. | ICLR 2026 | Video + Audio | - | Synergistic audio-visual understanding & reasoning | - |
| [**See, Hear, and Understand: Benchmarking Audiovisual Human Speech Understanding in Multimodal Large Language Models**](https://arxiv.org/abs/2512.02231) | AV-SpeakerBench | Nguyen, L. T. P. et al. | CVPR 2026 Findings | Video + Audio (Speech) | [Code](https://github.com/plnguyen2908/AV-SpeakerBench) | Audiovisual human speech understanding | [Data](https://huggingface.co/datasets/plnguyen2908/AV-SpeakerBench) |
| [**OmniEval: A Benchmark for Evaluating Omni-modal Models with Visual, Auditory and Textual Inputs**](https://arxiv.org/abs/2506.20960) | OmniEval | Zhang, Y. et al. | arXiv | Vision + Audio + Text | - | Omni-modal evaluation (tri-modal understanding) | - |
| [**XModBench: Benchmarking Cross-Modal Capabilities and Consistency in Omni-Language Models**](https://arxiv.org/abs/2510.15148) | XModBench | Wang, X.; Liu, J.; Huang, C.; Yu, X.; Wang, Z.; Sun, X.; Wu, J.; Yuille, A.; Barsoum, E.; Liu, Z. | ICLR 2026 | Text + Vision + Audio | [Code](https://github.com/XingruiWang/XModBench) | Cross-modal capability & consistency | [Data](https://huggingface.co/datasets/RyanWW/XModBench) |
| [**FutureOmni: Evaluating Future Forecasting from Omni-Modal Context for Multimodal LLMs**](https://arxiv.org/abs/2601.13836) | FutureOmni | Chen, Q.; Fu, J.; Li, C.; Ng, S.-K.; Qiu, X. | arXiv | Video + Audio | [Code](https://github.com/OpenMOSS/FutureOmni) | Omni-modal future forecasting | [Data](https://huggingface.co/datasets/OpenMOSS-Team/FutureOmni) |
| [**AVMeme Exam: A Multimodal Multilingual Multicultural Benchmark for LLMs' Contextual and Cultural Knowledge and Thinking**](https://arxiv.org/abs/2601.17645) | AVMeme Exam | Jiang, X. et al. | arXiv | Video + Audio | - | Cultural/contextual reasoning on audio-visual memes | [Data](https://huggingface.co/datasets/naplab/AVMeme-Exam) |
| [**A Comprehensive Benchmark for Evaluating Multi-Talker Audio-Visual Dialogue Generation**](https://arxiv.org/abs/2602.00607) | MTAVG-Bench | Zhou, Y. H. et al. | arXiv | Video + Audio | - | Multi-talker audio-visual dialogue generation evaluation | - |
| [**Towards The Future of Universal Omni-Language Models**](https://arxiv.org/abs/2409.15272) | OmniBench | Lin, J. et al. | NeurIPS 2025 (Datasets & Benchmarks) | Image + Audio + Text | [Code](https://github.com/multimodal-art-projection/OmniBench) | Tri-modal reasoning benchmark | - |
---

## Models

> Focus on models that support (or are designed for) **audio + visual + language** understanding / generation.

### Open-source

| Model | Org / Team | Year | Audio In | Video/Image In | Text Out | Speech Out | Code | Model | Notes |
|---|---|---:|:---:|:---:|:---:|:---:|---|---|---|
| Video-LLaMA | DAMO / contributors | 2023 | ✅ | ✅ | ✅ | ⚠️ | `TBD` | `TBD` | Early AV instruction-following video LLM |
| VideoLLaMA 2 | DAMO / contributors | 2024 | ✅ | ✅ | ✅ | ❌ | `TBD` | `TBD` | Stronger video/audio understanding |
| Qwen2.5-Omni | Qwen | 2025 | ✅ | ✅ | ✅ | ✅ | `TBD` | `TBD` | Omni multimodal model |
| MiniCPM-o | OpenBMB | 2025 | ✅ | ✅ | ✅ | ✅ | `TBD` | `TBD` | Real-time / on-device oriented omni interaction |
| VITA / VITA-1.5 | VITA team | 2024–2025 | ✅ | ✅ | ✅ | ✅ | `TBD` | `TBD` | Real-time vision-speech interaction |

> **Legend:** ✅ supported · ❌ not supported · ⚠️ partial / version-dependent

---

### Closed-source / API-based

| Model | Provider | Audio In | Video/Image In | Text Out | Speech Out | API / Docs | Notes |
|---|---|:---:|:---:|:---:|:---:|---|---|
| `TBD` | `TBD` |  |  |  |  | `TBD` | Add official documentation links only |

---

## Datasets (optional split)

If this repo grows, you can split datasets into a separate section/file with tags:

- **AVQA / reasoning**
- **Audio grounding**
- **Long-video understanding**
- **Instruction tuning**
- **Real-time multimodal interaction**
- **Multilingual AV evaluation**

Starter entries:
- PACS
- MUSIC-AVQA
- AVQA
- Video-MME (benchmark/eval set)

---

## Evaluation dimensions (suggested)

To make this repo more useful, consider tagging each benchmark/model by evaluation dimensions:

- **Audio grounding** (sound-source localization/reasoning)
- **Cross-modal consistency** (audio ↔ video alignment)
- **Temporal reasoning** (event order, duration, causality)
- **Long-context video understanding**
- **Speech content understanding** (ASR robustness, overlap, noise)
- **Multilingual AV understanding**
- **Real-time interaction latency**
- **Robustness** (noise, compression, missing modality, subtitle mismatch)

---

## Contributing

Contributions are welcome!

Please include:
- **Paper / benchmark / model name**
- **Authors**
- **Venue + year**
- **Official code link**
- **Official data / project page**
- A short note explaining why it is relevant to **audio-visual MLLM**

### Benchmark entry checklist
- [ ] Involves **audio + visual reasoning** OR evaluates **MLLMs on video** with audio/subtitles
- [ ] Added to the correct era (`<2024` vs `>=2024`)
- [ ] Includes **Code** and **Data** links
- [ ] Uses official sources (repo/project page) whenever possible

---

## License

- This list/repository content: **MIT** (recommended)
- Individual papers, datasets, and models remain under their own licenses.

---

## TODO (recommended next steps)

- [ ] Add official **code/data links** for the current benchmark entries
- [ ] Expand **post-2024 MLLM benchmarks**
- [ ] Add **taxonomy tags** (e.g., `#avqa`, `#long-video`, `#audio-grounding`)
- [ ] Add **model comparison schema** (streaming, latency, open weights, license)
- [ ] Add **awesome-list quality checks** (link checker, PR template)
