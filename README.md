# Comparison of Dependency Length in Human and Large Language Model Generated Sentences

## Overview

This project investigates whether **Large Language Models (LLMs)**, such as GPT-4o, exhibit the same linguistic tendency as humans to minimize the distance between syntactically related words—a phenomenon known as **Dependency Length Minimization (DLM)**.

Using dependency parsing and statistical analysis across **10 languages**, the study compares human-written sentences from the **Universal Dependencies (UD) Treebank** with GPT-4o-generated sentences to understand how closely AI-generated language resembles natural human syntax.

This work was completed as part of the **CGS410 Course Project** at the **Indian Institute of Technology Kanpur**.

---

## Motivation

Human languages naturally tend to place syntactically related words close together, reducing cognitive load during language processing. While modern LLMs generate fluent text, it remains unclear whether they replicate this linguistic principle.

This project aims to answer:

> **Do Large Language Models minimize dependency lengths in the same way as human writers across multiple languages?**

---

## Objectives

- Compare dependency lengths between human and AI-generated sentences.
- Analyze syntactic efficiency across ten languages.
- Investigate the effect of sentence length on dependency distance.
- Evaluate whether LLMs truly imitate human sentence structure.

---

## Dataset

### Human Corpus
- Universal Dependencies (UD) v2.13
- 2,000 sentences per language
- 10 languages
- Total: **20,000 human-written sentences**

### AI Corpus
- GPT-4o generated sentences
- Same prompts across all languages
- 2,000 sentences per language
- Total: **20,000 AI-generated sentences**

Languages included:

- English
- German
- Spanish
- French
- Chinese
- Arabic
- Hindi
- Japanese
- Russian
- Turkish

---

## Methodology

The analysis pipeline consists of:

1. Collect multilingual human and GPT-generated sentences.
2. Parse dependency trees using **Stanza**.
3. Compute dependency distance for every dependency relation.
4. Calculate:
   - Average Dependency Length (ADL)
   - Normalized ADL (nADL)
   - Sentence Length
   - Type-Token Ratio (TTR)
5. Compare human and AI distributions using:
   - Kolmogorov–Smirnov Test
6. Build regression models to study the impact of:
   - Sentence Length
   - Lexical Diversity
   - Parse Depth

---

## Technologies Used

- Python
- Stanza NLP
- Universal Dependencies
- NumPy
- Pandas
- SciPy
- Statsmodels
- Matplotlib

---

## Repository Structure

```
.
├── analyze.py                 # Dependency length analysis
├── regression.py              # Statistical modelling
├── report.pdf                 # Final project report
├── figures/                   # Visualizations
└── README.md
```

---

## Key Findings

- AI-generated sentences consistently exhibit **larger dependency lengths** than human-written sentences across all ten languages.
- The average dependency length difference ranges from **0.44–0.49 words**.
- Even after normalizing for sentence length, approximately **30% of the gap remains**, indicating structural differences beyond sentence length.
- Both humans and LLMs favor short dependency distances, but AI produces long-distance dependencies significantly more often.
- Sentence length has a stronger influence on dependency length in AI-generated text than in human writing.

---

## Results

### Average Dependency Length

| Metric | Observation |
|---------|-------------|
| Languages Evaluated | 10 |
| Human Sentences | 20,000 |
| AI Sentences | 20,000 |
| Average Difference | 0.44–0.49 words |
| Statistical Significance | p < 0.001 |

### Major Observations

- Human language follows Dependency Length Minimization more consistently.
- GPT-4o approximates this linguistic behavior but does not fully replicate it.
- The gap widens as sentence length increases.
- Structural differences persist even after normalization.

---

## Applications

- Computational Linguistics
- Natural Language Processing (NLP)
- Cognitive Science
- AI Evaluation
- Large Language Model Analysis
- Multilingual Language Processing
- Syntax and Dependency Parsing Research

---

## Future Work

- Extend evaluation to additional LLMs (Claude, Gemini, Llama, Mistral)
- Analyze dependency patterns in long-form documents
- Incorporate semantic dependency parsing
- Evaluate discourse-level dependency structures
- Explore cognitive complexity metrics beyond dependency length

---

## References

- Universal Dependencies v2.13
- Stanza NLP Toolkit
- Gibson (1998) – Dependency Locality Theory
- Hawkins (1994) – Performance Theory of Order and Constituency

---

## Author

**Siddharth Kumar**  
B.Tech, Materials Science and Engineering  
Indian Institute of Technology Kanpur

---

## Course Information

**Course:** CGS410  
**Project Title:** Comparison of Dependency Length in Human and Large Language Model Generated Sentences

---

## License

This project is intended for educational and research purposes.
