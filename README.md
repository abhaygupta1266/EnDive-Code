<div id="top">

<p align="center">
  <img src="https://endiveee.github.io/assets/logo.png" alt="EnDive Logo" width="40%" />
</p>

<p align="center">
  <em>Evaluating AI fairness across dialects of English.</em>
</p>

<p align="center">
  <a href="https://huggingface.co/EnDivee">
    <img src="https://img.shields.io/badge/Dataset-HuggingFace-blue?logo=huggingface&logoColor=white" />
  </a>
  <a href="https://arxiv.org/abs/2504.07100">
    <img src="https://img.shields.io/badge/Paper-arXiv-b31b1b.svg?logo=arxiv&logoColor=white" />
  </a>
  <a href="https://github.com/endiveee/EnDive-Code">
    <img src="https://img.shields.io/badge/Code-GitHub-181717?logo=github&logoColor=white" />
  </a>
  <a href="https://endiveee.github.io">
    <img src="https://img.shields.io/badge/Website-Endive-darkgreen?logo=googlechrome&logoColor=white" />
  </a>
</p>

</div>

---

## 🌿 Introduction

**EnDive** (**En**<b>glish</b> **Div**<b>ersity</b>) is the first large-scale benchmark designed to evaluate large language model (LLM) performance across a broad spectrum of underrepresented English dialects. It contains over **40,000 examples** across **12 tasks**, spanning domains like language understanding, reasoning, and code generation.

While most AI systems are optimized for Standard American English (SAE), **EnDive reveals how these systems struggle on dialectal variations** like African American Vernacular English (AAVE), Jamaican English (JamE), and Indian English (IndE). 

By highlighting these disparities, EnDive aims to **promote fairness and inclusivity in AI development**.

---

## 📊 Benchmark Overview

| Task Type               | Tasks Included                             |
|-------------------------|---------------------------------------------|
| Language Understanding  | SST-2, COPA, RTE, BoolQ, ANLI               |
| Commonsense Reasoning   | PIQA, SocialIQa, OpenBookQA                |
| Multi-hop QA            | HotpotQA                                   |
| Translation             | XNLI, NLI-X                                |
| Code & Math             | GSM8K, MBPP                                |

- ✅ All examples are derived from high-quality existing datasets
- 🔁 Translations are generated via few-shot prompting and filtered by BLEU score thresholds
- 🌍 Five dialects supported: **AAVE**, **JamE**, **IndE**, **SingE**, and **NigE**

---

## 🚀 Try It Out

- 🔗 Dataset on HuggingFace: [https://huggingface.co/EnDivee](https://huggingface.co/EnDivee)
- 📄 Paper: [arXiv:2504.07100](https://arxiv.org/abs/2504.07100)
- 🧠 Code: [GitHub Repo](https://github.com/endiveee/EnDive-Code)
- 🌐 Website: [endiveee.github.io](https://endiveee.github.io)

---

## 📈 Performance Snapshot

![Bar Graph of LLM Performance](https://endiveee.github.io/assets/performance_chart.png)

> This table shows how accurately different language models understand various English dialects. Each column represents a dialect, and the scores compare standard English (SAE) to dialect-specific prompts (CoT). If a model scores much lower on dialects like AAVE or JamE compared to SAE, it suggests the model is biased and less effective for those dialects. This highlights the importance of evaluating AI fairness across diverse language varieties.

---

## 🧠 Simplified Methodology

<p align="center">
  <img src="https://endiveee.github.io/assets/simplified_approach.png" alt="Simplified EnDive Methodology" width="80%" />
</p>

1. **Select Task + SAE Prompt**  
2. **Generate Dialectal Version via Few-Shot Prompting**  
3. **Filter with BLEU Score + Annotator Review**  
4. **Evaluate Models across all dialects using the same metrics**  
5. **Compare SAE vs Dialect CoT performance deltas**

---

## 🧾 Citation

If you use EnDive in your work, please cite us:

```bibtex
@article{gupta2024endive,
  title={EnDive: A Benchmark for Evaluating Fairness in Language Models Across English Dialects},
  author={Gupta, Abhay and Others},
  journal={arXiv preprint arXiv:2504.07100},
  year={2024}
}
```

---

## 🧰 File Structure

```bash
EnDive-Code/
│
├── data/                  # Sample subsets & BLEU filtering thresholds
├── scripts/               # Translation, filtering, evaluation code
├── results/               # Model performance logs
├── assets/                # Visuals for paper/website
├── utils/                 # Helper functions & evaluation metrics
└── README.md              # This file!
```

---

## 🤝 Contributing

We welcome PRs, issues, and collaborators—especially those working on:
- Dialect translation improvements
- Error analysis
- Fairness evaluation techniques

Start by cloning this repo and exploring `scripts/`!

---

## 📬 Contact

For questions, collaborations, or dataset access:

- Lead Author: **Abhay Gupta**
- Email: **abhaygupta1266@gmail.com**
- Website: [https://endiveee.github.io](https://endiveee.github.io)

---

## 🧡 Acknowledgments

Thanks to our amazing annotators, dialect speakers, and researchers from the fairness and NLP communities who made this possible.

---

<p align="center">
  <img src="https://endiveee.github.io/assets/logo.png" alt="EnDive Logo" width="100px" />
</p>

<p align="center">
  <em>Building inclusive AI, one dialect at a time.</em>
</p>

---

[⬆ Back to Top](#top)
