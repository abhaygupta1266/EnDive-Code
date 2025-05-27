<div id="top"></div>

<p align="center">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="May 26, 2025, 02_49_32 PM.png" alt="EnDive Logo" width="22%" />
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

**EnDive** (**En**glish **Div**ersity) is a large-scale benchmark designed to evaluate the fairness and performance of large language models (LLMs) across underrepresented English dialects. Spanning five diverse dialects—African American Vernacular English (AAVE), Chicano English (ChcE), Colloquial Singapore English (CollSgE), Indian English (IndE), and Jamaican English (JamE)—EnDive features 60 dialect-specific datasets covering 12 NLU tasks.

The benchmark captures how LLMs perform when prompts are written in different dialects rather than Standard American English (SAE). By comparing these dialect translations against SAE counterparts, EnDive identifies disparities in model accuracy, fluency, and robustness—highlighting critical issues of bias and inclusivity in today's AI systems.

---

## 📊 Performance Table

This table illustrates how well different language models understand and respond to English dialects by comparing their accuracy on SAE prompts versus dialect-specific prompts using Chain-of-Thought (CoT) reasoning. Each column represents a dialect—such as AAVE, JamE, or IndE—and each cell shows how a model’s performance changes when the same question is rephrased in that dialect. A significant drop in accuracy from SAE to CoT suggests the model struggles with that dialect, signaling potential bias and a lack of linguistic inclusivity. By highlighting these gaps, the table underscores the critical need to evaluate and improve AI fairness across diverse language varieties.

| Model              | AAVE (Δ) | ChcE (Δ) | CollSgE (Δ) | IndE (Δ) | JamE (Δ) |
|--------------------|----------|----------|-------------|----------|----------|
| 🥇 o1              | 89.13 → 93.15 | 88.54 → 93.39 | 89.14 → 93.50 | 90.34 → 94.07 | 89.40 → 93.14 |
| 🥈 Gemini 2.5 Pro   | 88.89 → 92.06 | 88.70 → 92.31 | 89.94 → 92.14 | 89.72 → 90.69 | 89.42 → 92.44 |
| 🥉 GPT-4o          | 82.20 → 87.36 | 80.37 → 87.35 | 87.31 → 89.06 | 83.74 → 87.52 | 82.53 → 87.40 |
| DeepSeek-v3        | 82.06 → 87.36 | 81.55 → 87.27 | 81.65 → 87.37 | 89.02 → 87.44 | 81.40 → 87.38 |
| Claude 3.5 Sonnet  | 79.78 → 83.10 | 81.15 → 88.78 | 81.18 → 88.93 | 81.60 → 89.64 | 81.06 → 88.37 |
| LLaMa-3-8B Instruct| 82.69 → 87.49 | 78.08 → 82.94 | 78.41 → 83.00 | 81.52 → 86.26 | 79.14 → 83.20 |
| GPT-4o-mini        | 74.53 → 78.27 | 75.01 → 77.70 | 76.50 → 86.61 | 74.66 → 82.56 | 80.56 → 86.60 |
| **Average**        | 82.75 → **86.97** | 81.91 → **87.11** | 83.20 → **88.39** | 86.95 → **88.95** | 83.20 → **88.39** |

---

## 🧪 Tasks

EnDive spans **12 NLP tasks** across four core reasoning categories:

- 🧠 Language Understanding: BoolQ, MultiRC, WSC, SST-2, COPA  
- 💻 Algorithmic Reasoning: HumanEval, MBPP  
- 🧮 Math: GSM8K, SVAMP  
- 🔎 Logic: LogicBench, FOLIO

---

## 🧠 Simplified Methodology

We generate dialectal translations of SAE prompts using few-shot prompting with GPT-4o. To ensure quality, we apply BLEU score filtering and exclude examples with significant similarity (translations that get >0.7 BLEU score). Translations are further validated by native speakers for fluency and authenticity. We then evaluate seven LLMs across 12 NLU tasks by comparing performance on SAE versus dialect variants.


---

## 📁 Directory Structure

```
EnDive-Code/
├── BLEU Score Code/                  # BLEU filtering thresholds
├── Eval Code Multi-AAVENUE/         # Evaluation code for different dialects
├── GPT 4o Translation Code/         # Few-shot translation prompts with GPT-4o
├── Multi-VALUE Translation code/    # Rule-based translation baseline
├── Translation Alignment Code/      # Alignment validation
├── ChatGPT Image May 26, 2025, 02_49_32 PM.png  # EnDive logo
├── Fluency Calculations.ipynb       # Fluency metric notebooks
├── Metrics (Rouge, BARTScore...).ipynb  # Metric analysis
├── Preference Scores.ipynb          # Human eval preference scores
└── README.md                        # ← you are here
```


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
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="May 26, 2025, 02_49_32 PM.png" alt="EnDive Logo" width="22%" />
</p>

<p align="center"><em>Pushing AI fairness forward, across diverse English dialects.</em></p>

<p align="left">
  <a href="#top">🔝 Back to Top</a>
</p>
