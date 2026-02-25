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

<!-- Big badge style: use `style=for-the-badge` -->
<!-- Tip: you can also add `&logo=...` to each badge if you want icons -->

<table style="width: 100%; table-layout: fixed;">
  <thead>
    <tr>
      <th style="width: 30%;">Paper</th>
      <th style="width: 10%;">Benchmark</th>
      <th style="width: 20%;">Authors</th>
      <th style="width: 10%;">Venue</th>
      <th style="width: 12%;">Modalities</th>
      <th style="width: 6%;">Code</th>
      <th style="width: 6%;">Data</th>
      <th style="width: 16%;">Tags</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="https://arxiv.org/abs/2410.12787"><b>The Curse of Multi-Modalities: Evaluating Hallucinations of Large Multimodal Models across Language, Visual, and Audio</b></a></td>
      <td>CMM</td>
      <td>Leng, S.; Xing, Y.; Cheng, Z.; Zhou, Y.; Zhang, H.; Li, X.; Zhao, D.; Lu, S.; Miao, C.; Bing, L.</td>
      <td>arXiv 2024</td>
      <td>Language + Visual + Audio</td>
      <td><a href="https://github.com/DAMO-NLP-SG/CMM">Code</a></td>
      <td><a href="https://huggingface.co/datasets/DAMO-NLP-SG/CMM">Data</a></td>
      <td>
        <a href="#tag-hallucination"><img alt="hallucination" src="https://img.shields.io/badge/hallucination-red?style=for-the-badge"></a>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2410.18325"><b>AVHBench: A Cross-Modal Hallucination Benchmark for Audio-Visual Large Language Models</b></a></td>
      <td>AVHBench</td>
      <td>Kim, S.-B.; Oh, H.-B.; Lee, J.; Senocak, A.; Chung, J. S.; Oh, T.-H.</td>
      <td>ICLR 2025</td>
      <td>Video + Audio</td>
      <td><a href="https://github.com/kaist-ami/AVHBench">Code</a></td>
      <td><a href="https://github.com/kaist-ami/AVHBench#download-the-avhbench-dataset">Data</a></td>
      <td>
        <a href="#tag-hallucination"><img alt="hallucination" src="https://img.shields.io/badge/hallucination-red?style=for-the-badge"></a>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2405.21075"><b>Video-MME: The First-Ever Comprehensive Evaluation Benchmark of Multi-Modal LLMs in Video Analysis</b></a></td>
      <td>Video-MME</td>
      <td>Fu, C.; Dai, Y.; Luo, Y.; Li, L.; Ren, S.; Zhang, R.; Wang, Z.; Zhou, C.; Shen, Y.; Zhang, M.; Chen, P.</td>
      <td>CVPR 2025</td>
      <td>Video + Audio/Subtitle</td>
      <td><a href="https://github.com/MME-Benchmarks/Video-MME">Code</a></td>
      <td><a href="https://huggingface.co/datasets/lmms-lab/Video-MME/tree/main">Data</a></td>
      <td>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2508.08237"><b>VGGSounder: Audio-Visual Evaluations for Foundation Models</b></a></td>
      <td>VGGSounder</td>
      <td>Zverev, D.; Wiedemer, T.; Prabhu, A.; Bethge, M.; Brendel, W.; Koepke, A. S.</td>
      <td>ICCV 2025</td>
      <td>Video + Audio</td>
      <td><a href="https://github.com/Bizilizi/VGGSounder">Code</a></td>
      <td><a href="https://github.com/Bizilizi/VGGSounder">Data</a></td>
      <td>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2501.02135"><b>AVTrustBench: Assessing and Enhancing Reliability and Robustness in Audio-Visual LLMs</b></a></td>
      <td>AVTrustBench</td>
      <td>Chowdhury, S.; Nag, S.; Dasgupta, S.; Wang, Y.; Elhoseiny, M.; Gao, R.; Manocha, D.</td>
      <td>ICCV 2025</td>
      <td>Video + Audio</td>
      <td><a href="https://github.com/schowdhury671/avtrustbench-">Code</a></td>
      <td><a href="https://github.com/schowdhury671/avtrustbench-/blob/main/data.md">Data</a></td>
      <td>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2409.15272"><b>OmniBench: Towards The Future of Universal Omni-Language Models</b></a></td>
      <td>OmniBench</td>
      <td>Li, Y.; Ma, Y.; Zhang, G.; Yuan, R.; Zhu, K.; Guo, H.; Liang, Y.; Liu, J.; Wang, Z.; Yang, J.; Wu, S.</td>
      <td>NeurIPS 2025 (D&amp;B)</td>
      <td>Image + Audio</td>
      <td><a href="https://github.com/multimodal-art-projection/OmniBench">Code</a></td>
      <td><a href="https://huggingface.co/datasets/m-a-p/OmniBench">Data</a></td>
      <td>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://aclanthology.org/volumes/2025.emnlp-main/"><b>Audio-centric Video Understanding Benchmark without Text Shortcut</b></a></td>
      <td>AVUT</td>
      <td>Yang, Y.; Zhuang, J.; Sun, G.; Tang, C.; Li, Y.; Li, P.; Jiang, Y.; Li, W.; Ma, Z.; Zhang, C.</td>
      <td>EMNLP 2025</td>
      <td>Video + Audio</td>
      <td><a href="https://github.com/lark-png/AVUT">Code</a></td>
      <td><a href="https://huggingface.co/datasets/tsinghua-ee/AVUTBenchmark">Data</a></td>
      <td>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2502.04326"><b>WorldSense: Evaluating Real-world Omnimodal Understanding for Multimodal LLMs</b></a></td>
      <td>WorldSense</td>
      <td>Hong, J.; Yan, S.; Cai, J.; Jiang, X.; Hu, Y.; Xie, W.</td>
      <td>ICLR 2026</td>
      <td>Video + Audio</td>
      <td><a href="https://github.com/JaaackHongggg/WorldSense">Code</a></td>
      <td><a href="https://huggingface.co/datasets/honglyhly/WorldSense">Data</a></td>
      <td>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2505.17862"><b>Daily-Omni: Towards Audio-Visual Reasoning with Multimodal Language Models</b></a></td>
      <td>Daily-Omni</td>
      <td>Zhou, Z. et al.</td>
      <td>arXiv 2025</td>
      <td>Video + Audio</td>
      <td><a href="https://github.com/lliar-liar/daily-omni">Code</a></td>
      <td><a href="https://huggingface.co/datasets/liarliar/Daily-Omni">Data</a></td>
      <td>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2412.02611"><b>AV-Odyssey Bench: Can Your Multimodal LLMs Really Understand Audio-Visual Information?</b></a></td>
      <td>AV-Odyssey</td>
      <td>Gong, K.; Feng, K.; Li, B.; Wang, Y.; Cheng, M.; Yang, S.; Han, J.; Wang, B.; Bai, Y.; Yang, Z.; Yue, X.</td>
      <td>arXiv 2025</td>
      <td>Video + Audio</td>
      <td><a href="https://github.com/AV-Odyssey/AV-Odyssey">Code</a></td>
      <td><a href="https://huggingface.co/datasets/AV-Odyssey/AV_Odyssey_Bench">Data</a></td>
      <td>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2510.10689"><b>OmniVideoBench: Towards Audio-Visual Understanding Evaluation for Omni MLLMs</b></a></td>
      <td>OmniVideoBench</td>
      <td>Li, C.; Chen, Y.; Ji, Y.; Xu, J.; Cui, Z.; Li, S.; Zhang, Y.; Tang, J.; Song, Z.; Zhang, D.; He, Y.</td>
      <td>ICLR 2026</td>
      <td>Video + Audio</td>
      <td><a href="https://github.com/NJU-LINK/OmniVideoBench">Code</a></td>
      <td><a href="https://huggingface.co/datasets/NJU-LINK/OmniVideoBench">Data</a></td>
      <td>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2506.20960"><b>OmniEval: A Benchmark for Evaluating Omni-modal Models with Visual, Auditory and Textual Inputs</b></a></td>
      <td>OmniEval</td>
      <td>Zhang, Y.; Luo, Z.; Yan, Q.; He, W.; Jiang, B.; Chen, X.; Han, K.</td>
      <td>arXiv 2025</td>
      <td>Vision + Audio</td>
      <td>-</td>
      <td>-</td>
      <td>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2510.15148"><b>XModBench: Benchmarking Cross-Modal Capabilities and Consistency in Omni-Language Models</b></a></td>
      <td>XModBench</td>
      <td>Wang, X.; Liu, J.; Huang, C.; Yu, X.; Wang, Z.; Sun, X.; Wu, J.; Yuille, A.; Barsoum, E.; Liu, Z.</td>
      <td>ICLR 2026</td>
      <td>Vision + Audio</td>
      <td><a href="https://github.com/XingruiWang/XModBench">Code</a></td>
      <td><a href="https://huggingface.co/datasets/RyanWW/XModBench">Data</a></td>
      <td>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2512.02231"><b>See, Hear, and Understand: Benchmarking Audiovisual Human Speech Understanding in Multimodal Large Language Models</b></a></td>
      <td>AV-SpeakerBench</td>
      <td>Nguyen, L.T.P.; Yu, Z.; Hang, S.L.Y.; An, S.; Lee, J.; Ban, Y.; Chung, S.; Nguyen, T.H.; Maeng, J.; Lee, S.; Lee, Y.J.</td>
      <td>CVPR 2026 Findings</td>
      <td>Video + Audio (Speech)</td>
      <td><a href="https://github.com/plnguyen2908/AV-SpeakerBench">Code</a></td>
      <td><a href="https://huggingface.co/datasets/plnguyen2908/AV-SpeakerBench">Data</a></td>
      <td>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-speech"><img alt="speech" src="https://img.shields.io/badge/speech-2a9d8f?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2601.13836"><b>FutureOmni: Evaluating Future Forecasting from Omni-Modal Context for Multimodal LLMs</b></a></td>
      <td>FutureOmni</td>
      <td>Chen, Q.; Fu, J.; Li, C.; Ng, S.-K.; Qiu, X.</td>
      <td>arXiv 2026</td>
      <td>Video + Audio</td>
      <td><a href="https://github.com/OpenMOSS/FutureOmni">Code</a></td>
      <td><a href="https://huggingface.co/datasets/OpenMOSS-Team/FutureOmni">Data</a></td>
      <td>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2601.17645"><b>AVMeme Exam: A Multimodal Multilingual Multicultural Benchmark for LLMs' Contextual and Cultural Knowledge and Thinking</b></a></td>
      <td>AVMeme Exam</td>
      <td>Jiang, X. et al.</td>
      <td>arXiv 2026</td>
      <td>Video + Audio</td>
      <td><a href="https://avmemeexam.github.io/public/">Code</a></td>
      <td><a href="https://huggingface.co/datasets/naplab/AVMeme-Exam">Data</a></td>
      <td>
        <a href="#tag-general-sound"><img alt="general-sound" src="https://img.shields.io/badge/general--sound-708090?style=for-the-badge"></a>
      </td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2602.00607"><b>A Comprehensive Benchmark for Evaluating Multi-Talker Audio-Visual Dialogue Generation</b></a></td>
      <td>MTAVG-Bench</td>
      <td>Zhou, Y.H.; Li, H.; Lin, R.; Huang, H.; Zhou, J.; Yuan, C.; Lan, T.; Zhou, Z.; Li, Y.; Xu, J.; Liao, J.</td>
      <td>arXiv 2026</td>
      <td>Video + Audio</td>
      <td>-</td>
      <td>-</td>
      <td>
        <a href="#tag-temporal-reasoning"><img alt="temporal-reasoning" src="https://img.shields.io/badge/temporal--reasoning-7b2cbf?style=for-the-badge"></a>
        <a href="#tag-speech"><img alt="speech" src="https://img.shields.io/badge/speech-2a9d8f?style=for-the-badge"></a>
      </td>
    </tr>
  </tbody>
</table>

<!-- Anchor targets for clickable badges -->
<a id="tag-hallucination"></a>
<a id="tag-temporal-reasoning"></a>
<a id="tag-speech"></a>
<a id="tag-music"></a>
<a id="tag-general-sound"></a>

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