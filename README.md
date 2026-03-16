# TeaP 2026: LLM Familiarity Estimates as Psycholinguistic Predictors

**Do large language model familiarity estimates predict human lexical processing? A cross-language, cross-model study in English and German.**

Job Schepens — Universität zu Köln

---

## Contents

- **[Slides](https://jobschepens.github.io/teap-present/)** — RevealJS presentation (TeaP 2026)
- [preregistration.md](preregistration.md) — OSF preregistration draft

## Abstract

Human familiarity ratings — the degree to which a word feels known — are among the strongest predictors of lexical processing speed. Recent work shows that large language models (LLMs) can generate familiarity-like estimates that correlate highly with human familiarity norms. This project investigates whether AI-derived familiarity estimates add predictive value *beyond* established corpus frequency measures, and whether different LLMs (instruction-tuned vs base; open vs proprietary) produce equally valid estimates.

analyses cover:

- **English**: ~5,000 words (Glasgow norms; English Crowdsourcing Project LDT)
- **German adults**: ~11,000 words (Conde et al., 2026 norms; DLEX / Günther et al.)
- **German children**: DeveL lexical decision data (Schroeder et al., 2015)

Models compared: `swiss-ai/Apertus-70B-Instruct-2509`, `GPT-4o-mini`, `allenai/OLMo-3-1025-7B`.

## Rendering locally

```bash
quarto render word_familiarity_project_draft_slides.qmd
# output: docs/index.html
```

Requires [Quarto](https://quarto.org/) and Python 3 with `pandas` and `numpy`.

## License

CC-By 4.0
