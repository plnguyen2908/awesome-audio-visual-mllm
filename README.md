# Awesome AudioVisual MLLM [![Awesome](https://awesome.re/badge.svg)](https://github.com/plnguyen2908/awesome-audio-visual-mllm)

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
| [**Audio Visual Scene-Aware Dialog (AVSD)**](https://arxiv.org/abs/1806.00525) | AVSD | Alamri, Huda, Vincent Cartillier, Abhishek Das, Jue Wang, Anoop Cherian, Irfan Essa, Dhruv Batra et al. | CVPR 2019 | Video + Audio | - | [Data](https://drive.google.com/drive/folders/1SlZTySJAk_2tiMG5F8ivxCfOl_OWwd_Q) |
| [**Vggsound: A Large-Scale Audio-Visual Dataset**](https://ieeexplore.ieee.org/abstract/document/9053174?casa_token=LBHDwOeaVnsAAAAA:ADjjzZPgIWZvZcwRe6N3vhvB7OAi3BTfzIZMR1wLpRoYtKAD940_78HIRF4MTdV5-xHJC90ZRA) | Vggsound | Chen, Honglie, Weidi Xie, Andrea Vedaldi, and Andrew Zisserman. | ICASSP 2020 | Video + Audio | - | [Data](http://www.robots.ox.ac.uk/~vgg/data/vggsound/) |

---

### MLLM-eval era (>= 2024)

> Benchmarks explicitly designed to evaluate modern multimodal LLMs (MLLMs) QA capability, often with broader task coverage and richer analysis.

<!-- Tags index (optional but recommended for clickable badges) -->
### Tags
- <a id="tag-hallucination"></a>**hallucination:** Contain questions that test the hallucination of the MLLMs.
- <a id="tag-coarse-perception"></a>**coarse perception:** Contain questions that can be answered by the global cross-modality information between audio and visual.
- <a id="tag-finegrained-perception"></a>**finegrained perception:** Contain questions that can be answered by grounding a specific temporal segment before reasoning over that segment.
- <a id="tag-speech"></a>**speech:** Contain questions asking about human speech or dialouge.
- <a id="tag-music"></a>**music:** Contain questions asking about music.
- <a id="tag-general-sound"></a>**general-sound:** Contain questions asking about any type of sound.

<!-- Badge helpers (use anywhere) -->
<!-- Example: [![hallucination](https://img.shields.io/badge/hallucination-red)](#tag-hallucination) -->

| Paper | Benchmark Name | Authors | Venue | Modalities | Code | Data | Tags |
|---|---|---|---|---|---|---|---|
| [**The Curse of Multi-Modalities: Evaluating Hallucinations of Large Multimodal Models across Language, Visual, and Audio**](https://arxiv.org/abs/2410.12787) | CMM | Leng, S.; Xing, Y.; Cheng, Z.; Zhou, Y.; Zhang, H.; Li, X.; Zhao, D.; Lu, S.; Miao, C.; Bing, L. | arXiv 2024 | Language + Visual + Audio | [Code](https://github.com/DAMO-NLP-SG/CMM) | [Data](https://huggingface.co/datasets/DAMO-NLP-SG/CMM) | `hallucination` <br> `coarse perception` <br> `general-sound` |
| [**AVHBench: A Cross-Modal Hallucination Benchmark for Audio-Visual Large Language Models**](https://arxiv.org/abs/2410.18325) | AVHBench | Kim, S.-B.; Oh, H.-B.; Lee, J.; Senocak, A.; Chung, J. S.; Oh, T.-H. | ICLR 2025 | Video + Audio | [Code](https://github.com/kaist-ami/AVHBench) | [Data](https://github.com/kaist-ami/AVHBench#download-the-avhbench-dataset) | `hallucination` `coarse perception` `general-sound` |
| [**Video-MME: The First-Ever Comprehensive Evaluation Benchmark of Multi-Modal LLMs in Video Analysis**](https://arxiv.org/pdf/2405.21075) | Video-MME | Fu, C.; Dai, Y.; Luo, Y.; Li, L.; Ren, S.; Zhang, R.; Wang, Z.; Zhou, C.; Shen, Y.; Zhang, M.; Chen, P. | CVPR 2025 | Video + Audio/Subtitle | [Code](https://github.com/MME-Benchmarks/Video-MME) | [Data](https://huggingface.co/datasets/lmms-lab/Video-MME/tree/main) | `finegrained perception` `general-sound` |
| [**VGGSounder: Audio-Visual Evaluations for Foundation Models**](https://arxiv.org/abs/2508.08237) | VGGSounder | Zverev, D.; Wiedemer, T.; Prabhu, A.; Bethge, M.; Brendel, W.; Koepke, A. S. | ICCV 2025 | Video + Audio | [Code](https://github.com/Bizilizi/VGGSounder) | [Data](https://github.com/Bizilizi/VGGSounder) | `coarse perception` `general-sound`  |
| [**AVTrustBench: Assessing and Enhancing Reliability and Robustness in Audio-Visual LLMs**](https://arxiv.org/abs/2501.02135) | AVTrustBench | Chowdhury, S.; Nag, S.; Dasgupta, S.; Wang, Y.; Elhoseiny, M.; Gao, R.; Manocha, D. | ICCV 2025 | Video + Audio | [Code](https://github.com/schowdhury671/avtrustbench-) | [Data](https://github.com/schowdhury671/avtrustbench-/blob/main/data.md) | `hallucination` `coarse perception` `finegrained perception` `general-sound` |
| [**OmniBench: Towards The Future of Universal Omni-Language Models**](https://arxiv.org/abs/2409.15272) | OmniBench | Li, Y., Ma, Y., Zhang, G., Yuan, R., Zhu, K., Guo, H., Liang, Y., Liu, J., Wang, Z., Yang, J. and Wu, S. | NeurIPS 2025 (Datasets & Benchmarks) | Image + Audio | [Code](https://github.com/multimodal-art-projection/OmniBench) | [Data](https://huggingface.co/datasets/m-a-p/OmniBench) | `coarse perception` `general-sound` |
| [**Audio-centric Video Understanding Benchmark without Text Shortcut**](https://aclanthology.org/2025.emnlp-main.333.pdf) | AVUT | Yang, Y., Zhuang, J., Sun, G., Tang, C., Li, Y., Li, P., Jiang, Y., Li, W., Ma, Z. and Zhang, C. | EMNLP 2025 | Video + Audio | [Code](https://github.com/lark-png/AVUT) | [Data](https://huggingface.co/datasets/tsinghua-ee/AVUTBenchmark) | `finegrained perception` `coarse perception` `general-sound` |
| [**WorldSense: Evaluating Real-world Omnimodal Understanding for Multimodal LLMs**](https://arxiv.org/abs/2502.04326) | WorldSense | Hong, J.; Yan, S.; Cai, J.; Jiang, X.; Hu, Y.; Xie, W. | ICLR 2026 | Video + Audio | [Code](https://github.com/JaaackHongggg/WorldSense) | [Data](https://huggingface.co/datasets/honglyhly/WorldSense) | `coarse perception` `general-sound` |
| [**Daily-Omni: Towards Audio-Visual Reasoning with Multimodal Language Models**](https://arxiv.org/abs/2505.17862) | Daily-Omni | Zhou, Z., Wang, R. and Wu, Z. | arXiv 2025 | Video + Audio | [Code](https://github.com/lliar-liar/daily-omni) | [Data](https://huggingface.co/datasets/liarliar/Daily-Omni) | `finegrained perception` `coarse perception` `general-sound` |
| [**AV-Odyssey Bench: Can Your Multimodal LLMs Really Understand Audio-Visual Information?**](https://arxiv.org/abs/2412.02611) | AV-Odyssey | Gong, K., Feng, K., Li, B., Wang, Y., Cheng, M., Yang, S., Han, J., Wang, B., Bai, Y., Yang, Z. and Yue, X. | arXiv 2025 | Image + Video + Audio | [Code](https://github.com/AV-Odyssey/AV-Odyssey) | [Data](https://huggingface.co/datasets/AV-Odyssey/AV_Odyssey_Bench) | `coarse perception` `general-sound` |
| [**OmniVideoBench: Towards Audio-Visual Understanding Evaluation for Omni MLLMs**](https://arxiv.org/abs/2510.10689) | OmniVideoBench | Li, C., Chen, Y., Ji, Y., Xu, J., Cui, Z., Li, S., Zhang, Y., Tang, J., Song, Z., Zhang, D. and He, Y. | ICLR 2026 | Video + Audio | [Code](https://github.com/NJU-LINK/OmniVideoBench) | [Data](https://huggingface.co/datasets/NJU-LINK/OmniVideoBench) | `finegrained perception` `general-sound` |
| [**OmniEval: A Benchmark for Evaluating Omni-modal Models with Visual, Auditory and Textual Inputs**](https://arxiv.org/abs/2506.20960) | OmniEval | Zhang, Y., Luo, Z., Yan, Q., He, W., Jiang, B., Chen, X. and Han, K. | arXiv 2025 | Video + Audio | - | - | `finegrained perception` `general-sound` |
| [**XModBench: Benchmarking Cross-Modal Capabilities and Consistency in Omni-Language Models**](https://arxiv.org/abs/2510.15148) | XModBench | Wang, X.; Liu, J.; Huang, C.; Yu, X.; Wang, Z.; Sun, X.; Wu, J.; Yuille, A.; Barsoum, E.; Liu, Z. | ICLR 2026 | Image + Audio | [Code](https://github.com/XingruiWang/XModBench) | [Data](https://huggingface.co/datasets/RyanWW/XModBench) | `coarse perception` `general-sound` |
| [**See, Hear, and Understand: Benchmarking Audiovisual Human Speech Understanding in Multimodal Large Language Models**](https://arxiv.org/abs/2512.02231) | AV-SpeakerBench | Nguyen, L.T.P., Yu, Z., Hang, S.L.Y., An, S., Lee, J., Ban, Y., Chung, S., Nguyen, T.H., Maeng, J., Lee, S. and Lee, Y.J. | CVPR 2026 Findings | Video + Audio (Speech) | [Code](https://github.com/plnguyen2908/AV-SpeakerBench) | [Data](https://huggingface.co/datasets/plnguyen2908/AV-SpeakerBench) | `finegrained perception` `coarse perception` `speech` |
| [**FutureOmni: Evaluating Future Forecasting from Omni-Modal Context for Multimodal LLMs**](https://arxiv.org/abs/2601.13836) | FutureOmni | Chen, Q.; Fu, J.; Li, C.; Ng, S.-K.; Qiu, X. | arXiv 2026 | Video + Audio | [Code](https://github.com/OpenMOSS/FutureOmni) | [Data](https://huggingface.co/datasets/OpenMOSS-Team/FutureOmni) | `finegrained perception` `general-sound` |
| [**AVMeme Exam: A Multimodal Multilingual Multicultural Benchmark for LLMs' Contextual and Cultural Knowledge and Thinking**](https://arxiv.org/abs/2601.17645) | AVMeme Exam | Jiang, X., Wang, Q., Wu, J., He, X., Xu, Z., Ma, Y., Piao, M., Yang, K., Zheng, X., Shimizu, R. and Chen, Y., | arXiv 2026 | Video + Audio | [Code](https://avmemeexam.github.io/public/) | [Data](https://huggingface.co/datasets/naplab/AVMeme-Exam) | `coarse perception` `general-sound` |
| [**A Comprehensive Benchmark for Evaluating Multi-Talker Audio-Visual Dialogue Generation**](https://arxiv.org/abs/2602.00607) | MTAVG-Bench | Zhou, Y.H., Li, H., Lin, R., Huang, H., Zhou, J., Yuan, C., Lan, T., Zhou, Z., Li, Y., Xu, J. and Liao, J. | arXiv 2026 | Video + Audio | - | - | `finegrained perception` `speech` |

## Foundational Models

> Focus on foundational models that support (or are designed for) **audio + visual + language** understanding / generation.

### Open-source

| Model | Org / Team | Year | Audio In | Video/Image In | Text Out | Speech Out | Code | Model | Evaluated on (AVQA benchmarks) |
|---|---|---:|:---:|:---:|:---:|:---:|---|---|---|
| PandaGPT | PandaGPT authors (ImageBind + Vicuna) | 2023 | ✅ | ✅ (Image+Video) | ✅ | ❌ | https://panda-gpt.github.io/  | *(project page / paper)*  | AVSD, AVSSD, MUSIC-AVQA |
| VideoLLaMA2 | DAMO-NLP-SG (Alibaba) | 2024 | ✅ | ✅ (Video) | ✅ | ❌ | https://github.com/DAMO-NLP-SG/VideoLLaMA2  | https://huggingface.co/papers/2406.07476 | AVQA, AVSD, VGGSound, Music-AVQA  |
| VITA | VITA-MLLM | 2024 | ✅ | ✅ (Image+Video) | ✅ | ✅ | https://github.com/VITA-MLLM/VITA | https://huggingface.co/VITA-MLLM  | Video-MME |
| Unified-IO 2 (UIO2) | Allen Institute for AI (AI2) | 2024 | ✅ | ✅ (Image+Video) | ✅ | ✅ | https://unified-io-2.allenai.org/  | *(model releases vary; use project page above)*  | Vggsound  |
| OneLLM | Shanghai AI Lab / collaborators | 2024 | ✅ | ✅ (Video) | ✅ | ❌ | https://github.com/csuhan/OneLLM | *(see repo / paper)*  | MUSIC-AVQA, AVSD |
| video-SALMONN | Tsinghua + ByteDance | 2024 | ✅ | ✅ (Video) | ✅ | ❌ | https://github.com/bytedance/SALMONN/ | https://arxiv.org/abs/2406.15704 | AVQA, MUSIC-AVQA, AVSD |
| AnyGPT | OpenMOSS / AnyGPT authors | 2024 | ✅ *(speech/music)* | ✅ (Images) | ✅ | ✅ *(any-to-any, incl. speech)* | https://github.com/OpenMOSS/AnyGPT  | https://huggingface.co/papers/2402.12226  | N/A |
| VITA-1.5 | VITA-MLLM | 2025 | ✅ | ✅ (Image+Video) | ✅ | ✅ | https://github.com/VITA-MLLM/VITA | https://huggingface.co/VITA-MLLM/VITA-1.5  | Video-MME |
| Phi-4 Multimodal Instruct | Microsoft | 2025 | ✅ | ✅ (Image + Video) | ✅ | ❌ | https://huggingface.co/microsoft/Phi-4-multimodal-instruct | https://huggingface.co/microsoft/Phi-4-multimodal-instruct  | Video-MME |
|OmniVinci|NVIDIA| 2025|✅ | ✅ (Image+Video) | ✅ | ✅|https://github.com/NVlabs/OmniVinci|https://huggingface.co/nvidia/omnivinci| DailyOmni, Worldsense, Video-MME|
| video-SALMONN 2 | Tsinghua + ByteDance | 2025 | ✅ | ✅ (Video) | ✅ | ❌ | https://github.com/bytedance/video-SALMONN-2 | https://huggingface.co/tsinghua-ee/video-SALMONN-2 | Video-MME, AVUT, Worldsense, DailyOmni |
| Qwen2.5-Omni | Qwen (Alibaba Cloud) | 2025 | ✅ | ✅ (Image+Video) | ✅ | ✅ | https://github.com/QwenLM/Qwen2.5-Omni  | https://huggingface.co/Qwen/Qwen2.5-Omni-7B  | OmniBench, Video-MME|
| Qwen3-Omni | Qwen (Alibaba Cloud) | 2025 | ✅ | ✅ (Image+Video) | ✅ | ✅ | https://github.com/QwenLM/Qwen3-Omni | https://huggingface.co/Qwen/Qwen3-Omni-30B-A3B-Thinking  | Worldsense, Daily-Omni, Video-MME |
| D-ORCA | Tsinghua + Tencent | 2026 | ✅ | ✅ (Video) | ✅ | ❌ | https://github.com/WeChatCV/D-ORCA/ | https://huggingface.co/tsinghua-ee/D-ORCA-8B-0210 | Video-MME, Worldsense, AVUT, DailyOmni, AV-SpeakerBench |


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