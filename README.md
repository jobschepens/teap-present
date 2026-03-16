# TeaP 2026: LLM Familiarity Estimates as Psycholinguistic Predictors

**Do large language model familiarity estimates predict human lexical processing? A cross-language, cross-model study in English and German.**

Job Schepens — Universität zu Köln

---

## Contents

- **[Slides](https://jobschepens.github.io/teap-present/)** — RevealJS presentation (TeaP 2026)
- **[PDF](https://jobschepens.github.io/teap-present/slides.pdf)** — PDF version of the slides
- [preregistration.md](preregistration.md) — OSF preregistration

## Abstract

Recent research suggests that LLM-generated word familiarity ratings outperform traditional frequency measures in predicting adult lexical decision times (Brysbaert et al., 2024)

Here, we report a validaition study that assesses whether these ratings indeed reflect lexical knowledge learned by the model, or if they partially result from memorization of existing human rating datasets present in the LLM's training data. This distinction has important implications for the validity of LLM-derived psycholinguistic measures. We address this training-data leakage concern by using open-source language models with publicly documented training data.

In a first step, we determine whether apertus' training data excludes existing word familiarity ratings. Second, we derive familiarity estimates for the ~1000 DeveL words using appropriate prompting.

This study provides an empirical validation of LLM-derived lexical measures while addressing concerns about training-data contamination. Our findings inform best practices for using language models as tools in psycholinguistic research and clarify the conditions under which LLM-generated measures can be used for obtaining lexical variables.

analyses cover:

- **English**: ~5,000 words (Glasgow norms; English Crowdsourcing Project LDT)
- **German adults**: ~2,000 words (Conde et al., 2026 norms)
- **German children**: ~1,000 words (Schroeder et al., 2015)

Models compared: `swiss-ai/Apertus-70B-Instruct-2509`, `GPT-4o-mini`, `allenai/OLMo-3-1025-7B`, `GPTOSS-120B`

## Rendering locally

```bash
quarto render word_familiarity_project_draft_slides.qmd
# output: docs/index.html
```

Requires [Quarto](https://quarto.org/) and Python 3 with `pandas` and `numpy`.

## License

CC-By 4.0
