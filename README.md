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
| [**PACS: A Dataset for Physical Audiovisual CommonSense Reasoning**](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136970286.pdf) | PACS | Yu, S.; Wu, P.; Liang, P. P.; Salakhutdinov, R.; Morency, L. P. | ECCV 2022 | Video + Audio | [Code](https://github.com/samuelyu2002/PACS) | [Data](https://drive.google.com/drive/folders/1TjOKBTU9dsytHJIb919V4wXFR1Zm5TsJ) |
| [**Learning To Answer Questions in Dynamic Audio-Visual Scenarios**](https://openaccess.thecvf.com/content/CVPR2022/papers/Li_Learning_To_Answer_Questions_in_Dynamic_Audio-Visual_Scenarios_CVPR_2022_paper.pdf) | MUSIC-AVQA |Li, G.; Wei, Y.; Tian, Y.; Xu, C.; Wen, J. R.; Hu, D. | CVPR 2022 | Video + Audio | [Code](https://github.com/GeWu-Lab/MUSIC-AVQA) | [Data](https://drive.google.com/drive/folders/1WAryZZE0srLIZG8VHl22uZ3tpbGHtsrQ) |
| [**AVQA: A Dataset for Audio-Visual Question Answering on Videos**](https://dl.acm.org/doi/10.1145/3503161.3548291) | AVQA | Yang, P.; Wang, X.; Duan, X.; Chen, H.; Hou, R.; Jin, C.; Zhu, W. | ACM MM 2022 | Video + Audio | [Code](https://github.com/GeWu-Lab/MUSIC-AVQA) | [Data](https://drive.google.com/drive/folders/1WAryZZE0srLIZG8VHl22uZ3tpbGHtsrQ) |

---

### MLLM-eval era (>= 2024)

> Benchmarks explicitly designed to evaluate modern multimodal LLMs (MLLMs) QA capability, often with broader task coverage and richer analysis.

<!-- Tags index (optional but recommended for clickable badges) -->
### Tags
- <a id="tag-hallucination"></a>**hallucination**
- <a id="tag-temporal-reasoning"></a>**temporal-reasoning**
- <a id="tag-speech"></a>**speech**
- <a id="tag-music"></a>**music**
- <a id="tag-general-sound"></a>**general-sound**

<!-- Badge helpers (use anywhere) -->
<!-- Example: [![hallucination](https://img.shields.io/badge/hallucination-red)](#tag-hallucination) -->

| Paper | Benchmark Name | Authors | Venue | Modalities | Code | Data | Tags |
|---|---|---|---|---|---|---|---|
| [**The Curse of Multi-Modalities: Evaluating Hallucinations of Large Multimodal Models across Language, Visual, and Audio**](https://arxiv.org/abs/2410.12787) | CMM | Leng, S.; Xing, Y.; Cheng, Z.; Zhou, Y.; Zhang, H.; Li, X.; Zhao, D.; Lu, S.; Miao, C.; Bing, L. | arXiv 2024 | Language + Visual + Audio | [Code](https://github.com/DAMO-NLP-SG/CMM) | [Data](https://huggingface.co/datasets/DAMO-NLP-SG/CMM) | `hallucination` `coarse perception` `general-sound` |
| [**AVHBench: A Cross-Modal Hallucination Benchmark for Audio-Visual Large Language Models**](https://arxiv.org/abs/2410.18325) | AVHBench | Kim, S.-B.; Oh, H.-B.; Lee, J.; Senocak, A.; Chung, J. S.; Oh, T.-H. | ICLR 2025 | Video + Audio | [Code](https://github.com/kaist-ami/AVHBench) | [Data](https://github.com/kaist-ami/AVHBench#download-the-avhbench-dataset) | `hallucination` `coarse perception` `general-sound` |
| [**VGGSounder: Audio-Visual Evaluations for Foundation Models**](https://arxiv.org/abs/2508.08237) | VGGSounder | Zverev, D.; Wiedemer, T.; Prabhu, A.; Bethge, M.; Brendel, W.; Koepke, A. S. | ICCV 2025 | Video + Audio | [Code](https://github.com/Bizilizi/VGGSounder) | [Data](https://github.com/Bizilizi/VGGSounder) | `coarse perception` `general-sound`  |
| [**AVTrustBench: Assessing and Enhancing Reliability and Robustness in Audio-Visual LLMs**](https://arxiv.org/abs/2501.02135) | AVTrustBench | Chowdhury, S.; Nag, S.; Dasgupta, S.; Wang, Y.; Elhoseiny, M.; Gao, R.; Manocha, D. | ICCV 2025 | Video + Audio | [Code](https://github.com/schowdhury671/avtrustbench-) | [Data](https://github.com/schowdhury671/avtrustbench-/blob/main/data.md) | `hallucination` `coarse perception` `finegrained perception` `general-sound` |
| [**OmniBench: Towards The Future of Universal Omni-Language Models**](https://arxiv.org/abs/2409.15272) | OmniBench | Li, Y., Ma, Y., Zhang, G., Yuan, R., Zhu, K., Guo, H., Liang, Y., Liu, J., Wang, Z., Yang, J. and Wu, S. | NeurIPS 2025 (Datasets & Benchmarks) | Image + Audio | [Code](https://github.com/multimodal-art-projection/OmniBench) | [Data](https://huggingface.co/datasets/m-a-p/OmniBench) | `coarse perception` `general-sound` |
| [**Audio-centric Video Understanding Benchmark without Text Shortcut**](https://aclanthology.org/2025.emnlp-main.333.pdf) | AVUT | Yang, Y., Zhuang, J., Sun, G., Tang, C., Li, Y., Li, P., Jiang, Y., Li, W., Ma, Z. and Zhang, C. | EMNLP 2025 | Video + Audio | [Code](https://github.com/lark-png/AVUT) | [Data](https://huggingface.co/datasets/tsinghua-ee/AVUTBenchmark) | `finegrained perception` `coarse perception` `general-sound` |
| [**WorldSense: Evaluating Real-world Omnimodal Understanding for Multimodal LLMs**](https://arxiv.org/abs/2502.04326) | WorldSense | Hong, J.; Yan, S.; Cai, J.; Jiang, X.; Hu, Y.; Xie, W. | ICLR 2026 | Video + Audio | [Code](https://github.com/JaaackHongggg/WorldSense) | [Data](https://huggingface.co/datasets/honglyhly/WorldSense) | `coarse perception` `general-sound` |
| [**Daily-Omni: Towards Audio-Visual Reasoning with Multimodal Language Models**](https://arxiv.org/abs/2505.17862) | Daily-Omni | Zhou, Z. et al. | arXiv 2025 | Video + Audio | [Code](https://github.com/lliar-liar/daily-omni) | [Data](https://huggingface.co/datasets/liarliar/Daily-Omni) | `finegrained perception` `coarse perception` `general-sound` |
| [**AV-Odyssey Bench: Can Your Multimodal LLMs Really Understand Audio-Visual Information?**](https://arxiv.org/abs/2412.02611) | AV-Odyssey | Gong, K., Feng, K., Li, B., Wang, Y., Cheng, M., Yang, S., Han, J., Wang, B., Bai, Y., Yang, Z. and Yue, X. | arXiv 2025 | Image + Video + Audio | [Code](https://github.com/AV-Odyssey/AV-Odyssey) | [Data](https://huggingface.co/datasets/AV-Odyssey/AV_Odyssey_Bench) | `coarse perception` `general-sound` |
| [**OmniVideoBench: Towards Audio-Visual Understanding Evaluation for Omni MLLMs**](https://arxiv.org/abs/2510.10689) | OmniVideoBench | Li, C., Chen, Y., Ji, Y., Xu, J., Cui, Z., Li, S., Zhang, Y., Tang, J., Song, Z., Zhang, D. and He, Y. | ICLR 2026 | Video + Audio | [Code](https://github.com/NJU-LINK/OmniVideoBench) | [Data](https://huggingface.co/datasets/NJU-LINK/OmniVideoBench) | `finegrained perception` `general-sound` |
| [**OmniEval: A Benchmark for Evaluating Omni-modal Models with Visual, Auditory and Textual Inputs**](https://arxiv.org/abs/2506.20960) | OmniEval | Zhang, Y., Luo, Z., Yan, Q., He, W., Jiang, B., Chen, X. and Han, K. | arXiv 2025 | Video + Audio | - | - | `finegrained perception` `general-sound` |
| [**XModBench: Benchmarking Cross-Modal Capabilities and Consistency in Omni-Language Models**](https://arxiv.org/abs/2510.15148) | XModBench | Wang, X.; Liu, J.; Huang, C.; Yu, X.; Wang, Z.; Sun, X.; Wu, J.; Yuille, A.; Barsoum, E.; Liu, Z. | ICLR 2026 | Image + Audio | [Code](https://github.com/XingruiWang/XModBench) | [Data](https://huggingface.co/datasets/RyanWW/XModBench) | `coarse perception` `general-sound` |
| [**See, Hear, and Understand: Benchmarking Audiovisual Human Speech Understanding in Multimodal Large Language Models**](https://arxiv.org/abs/2512.02231) | AV-SpeakerBench | Nguyen, L.T.P., Yu, Z., Hang, S.L.Y., An, S., Lee, J., Ban, Y., Chung, S., Nguyen, T.H., Maeng, J., Lee, S. and Lee, Y.J. | CVPR 2026 Findings | Video + Audio (Speech) | [Code](https://github.com/plnguyen2908/AV-SpeakerBench) | [Data](https://huggingface.co/datasets/plnguyen2908/AV-SpeakerBench) | `finegrained perception` `coarse perception` `speech` |
| [**FutureOmni: Evaluating Future Forecasting from Omni-Modal Context for Multimodal LLMs**](https://arxiv.org/abs/2601.13836) | FutureOmni | Chen, Q.; Fu, J.; Li, C.; Ng, S.-K.; Qiu, X. | arXiv 2026 | Video + Audio | [Code](https://github.com/OpenMOSS/FutureOmni) | [Data](https://huggingface.co/datasets/OpenMOSS-Team/FutureOmni) | `finegrained perception` `general-sound` |
| [**AVMeme Exam: A Multimodal Multilingual Multicultural Benchmark for LLMs' Contextual and Cultural Knowledge and Thinking**](https://arxiv.org/abs/2601.17645) | AVMeme Exam | Jiang, X. et al. | arXiv 2026 | Video + Audio | [Code](https://avmemeexam.github.io/public/) | [Data](https://huggingface.co/datasets/naplab/AVMeme-Exam) | `coarse perception` `general-sound` |
| [**A Comprehensive Benchmark for Evaluating Multi-Talker Audio-Visual Dialogue Generation**](https://arxiv.org/abs/2602.00607) | MTAVG-Bench | Zhou, Y.H., Li, H., Lin, R., Huang, H., Zhou, J., Yuan, C., Lan, T., Zhou, Z., Li, Y., Xu, J. and Liao, J. | arXiv 2026 | Video + Audio | - | - | `finegrained perception` `speech` |

## Foundational Models

> Focus on foundational models that support (or are designed for) **audio + visual + language** understanding / generation.

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

## Contributing

Contributions are welcome!

Please include:
- **Paper / benchmark / model name**
- **Authors**
- **Venue + year**
- **Official code link**
- **Official data / project page**
- A short note explaining why it is relevant to **audio-visual QA**

---

## License

- This list/repository content: **MIT** 
- Individual papers, datasets, and models remain under their own licenses.