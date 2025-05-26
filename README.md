<div id="top"></div>

<p align="center">
  <img src="ChatGPT Image May 26, 2025, 02_49_32 PM.png" alt="EnDive Logo" width="22%" style="margin-left:3%;" />
</p>

<p align="center"><em>Evaluating AI fairness across dialects of English.</em></p>

<p align="center">
  <a href="https://huggingface.co/EnDivee">
    <img src="https://img.shields.io/badge/%F0%9F%91%80%20Dataset-HuggingFace-blue" />
  </a>
  <a href="https://arxiv.org/abs/2504.07100">
    <img src="https://img.shields.io/badge/%F0%9F%93%9C%20Paper-arXiv-red" />
  </a>
  <a href="https://github.com/endiveee/EnDive-Code">
    <img src="https://img.shields.io/badge/%F0%9F%A4%96%20Code-GitHub-grey" />
  </a>
  <a href="https://endiveee.github.io">
    <img src="https://img.shields.io/badge/%F0%9F%8C%90%20Website-EnDive-brightgreen" />
  </a>
</p>

---

## 📝 About

**EnDive** (**En**glish **Div**ersity Evaluation) is a large-scale benchmark designed to evaluate the fairness and performance of large language models across underrepresented English dialects. Spanning five diverse dialects—AAVE, Chicano English, Colloquial Singapore English, Indian English, and Jamaican English—EnDive features 60 dialect-specific datasets covering 12 NLP tasks.

The benchmark captures how LLMs perform when prompts are written in different dialects rather than Standard American English (SAE). By comparing these dialect translations against SAE counterparts, EnDive identifies disparities in model accuracy, fluency, and robustness—highlighting critical issues of bias and inclusivity in today's AI systems.

---

## 📊 Performance Snapshot

<p align="center">
  <img src="file-747EcCdSFXWkYQVBrbhEY1" alt="Bar Graph of LLM Performance" width="65%" />
</p>

This table shows how accurately different language models understand various English dialects. Each column represents a dialect, and the scores compare standard English (SAE) to dialect-specific prompts (CoT). If a model scores much lower on dialects like AAVE or JamE compared to SAE, it suggests the model is biased and less effective for those dialects. This highlights the importance of evaluating AI fairness across diverse language varieties.

| Model              | AAVE (Δ) | ChcE (Δ) | CollSgE (Δ) | IndE (Δ) | JamE (Δ) |
|--------------------|----------|----------|-------------|----------|----------|
| 🥇 o1              | 89.13 → 93.15 | 88.54 → 93.39 | 89.14 → 93.50 | 90.34 → 94.07 | 89.40 → 93.14 |
| 🥈 Gemini 2.5 Pro   | 88.89 → 92.06 | 88.70 → 92.31 | 89.94 → 92.14 | 89.72 → 90.69 | 89.42 → 92.44 |
| 🥉 GPT-4o          | 82.20 → 87.36 | 80.37 → 87.35 | 87.31 → 89.06 | 83.74 → 87.52 | 82.53 → 87.40 |
| DeepSeek-v3        | 82.06 → 87.36 | 81.55 → 87.27 | 81.65 → 87.37 | 89.02 → 87.44 | 81.40 → 87.38 |
| Claude 3.5 Sonnet  | 79.78 → 83.10 | 81.15 → 88.78 | 81.18 → 88.93 | 81.60 → 89.64 | 81.06 → 88.37 |
| LLaMa-3-8B Instruct| 82.69 → 87.49 | 78.08 → 82.94 | 78.41 → 83.00 | 81.52 → 86.26 | 79.14 → 83.20 |
| GPT-4o-mini        | 74.53 → 78.27 | 75.01 → 77.70 | 76.50 → 86.61 | 74.66 → 82.56 | 80.56 → 86.60 |
| **Average**        | **82.75 → 86.97** | **81.91 → 87.11** | **83.20 → 88.39** | **86.95 → 88.95** | **83.20 → 88.39** |

---

## 🧪 Tasks

EnDive spans **12 NLP tasks** covering reasoning, classification, generation, and math. A few examples:

- 🧠 Commonsense: COPA, PIQA, SIQA
- 📚 Reading & QA: SQuAD, DROP, NarrativeQA
- 🧮 Math & Logic: GSM8K, ProofWriter
- 📄 Summarization: XSum, CNN/DM
- ✍🏽 Language Generation: WritingPrompts, DART

---

## 🧠 Simplified Methodology

We prompt GPT-4o-mini to translate SAE prompts into dialectal variants using few-shot CoT prompting. We apply automatic BLEU filtering and manual inspection to ensure quality. LLMs are then evaluated on both SAE and dialect prompts across tasks using ROUGE, BARTScore, and MTurk ratings to compare fairness and performance.

---

## 🗂 Directory Structure

EnDive-Code/
├── BLEU Score Code/ # BLEU filtering thresholds
├── Eval Code Multi-AAVENUE/ # Evaluation code for different dialects
├── GPT 4o Translation Code/ # Few-shot translation prompts with GPT-4o
├── Multi-VALUE Translation code/ # Rule-based translation baseline
├── Translation Alignment Code/ # Alignment validation
├── ChatGPT Image May 26, 2025...png # EnDive logo
├── Fluency Calculations.ipynb # Fluency metric notebooks
├── Metrics (Rouge, BARTScore...).ipynb# Metric analysis
├── Preference Scores.ipynb # Human eval preference scores
└── README.md # ← you are here


---

## 📚 Citation

If you use EnDive in your research, please cite us:

```bibtex
@misc{gupta2025endivecrossdialectbenchmarkfairness,
  title={EnDive: A Cross-Dialect Benchmark for Fairness and Performance in Large Language Models}, 
  author={Abhay Gupta and Jacob Cheung and Philip Meng and Shayan Sayyed and Austen Liao and Kevin Zhu and Sean O'Brien},
  year={2025},
  eprint={2504.07100},
  archivePrefix={arXiv},
  primaryClass={cs.CL},
  url={https://arxiv.org/abs/2504.07100}, 
}
```

## 📬 Contact

For questions or collaborations, feel free to email us at **abhaygupta1266@gmail.com**.

<p align="center">
  <img src="ChatGPT Image May 26, 2025, 02_49_32 PM.png" alt="EnDive Logo" width="22%" style="margin-left:3%;" />
</p>

<p align="center"><em>Building inclusive AI, one dialect at a time.</em></p>

<p align="left">
  <a href="#top">🔝 Back to Top</a>
</p>
