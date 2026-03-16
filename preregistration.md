# OSF Preregistration: LLM Familiarity Estimates as Psycholinguistic Predictors — English and German

**Registration date:** March 2026 (to be submitted before data collection begins for Apertus and OLMo familiarity generation)
**Covers:** Phase B (English) and Phase C (German) of the TeaP 2026 research plan. Phase A (leakage audit) is exploratory and is not covered by this preregistration.

---

## Title

Do large language model familiarity estimates predict human lexical processing? A cross-language, cross-model study in English and German.

---

## Description

Human familiarity ratings — the degree to which a word feels known — are among the strongest predictors of lexical processing speed. Recent work shows that large language models (LLMs) can generate familiarity-like estimates that correlate highly with human familiarity norms (Brysbaert, Martínez, & Reviriego, 2024). Whether these AI estimates add predictive value *beyond* established corpus frequency measures, and whether different LLMs (instruction-tuned vs base; open vs proprietary) produce equally valid estimates, is an open question.

This preregistration covers two confirmatory analyses examining AI familiarity as a predictor of lexical decision times, with corpus frequency variables and word-level controls included as baselines:

- English: ~5,000 words from the Glasgow norms (Scott et al., 2019); lexical decision data from the English Crowdsourcing Project (Mandera et al., 2020).
- German: ~11,000 words from Conde et al. (2026) German familiarity norms; lexical decision data from Brysbaert et al. (2011) and studies in Günther et al. (2020).

Three LLMs are compared: `swiss-ai/Apertus-70B-Instruct-2509` (instruction-tuned; open; familiarity generated in this project), `GPT-4o-mini` (instruction-tuned; proprietary; familiarity taken from published AI norms), and `allenai/OLMo-3-1025-7B` (base, non-instruction-tuned; fully open weights and open training data Dolma 3; familiarity generated in this project). Additionally, we include LLM-text-based word frequency, which is word frequency tallied from LLM-generated running text following Schepens et al. (2025).

---

## License

CC-By 4.0

---

## Subjects

Psycholinguistics; Cognitive Science; Natural Language Processing; Language Comprehension; Word Recognition

---

## Research Questions and Hypotheses

**RQ1 (English):** Do AI familiarity estimates from Apertus, GPT-4o-mini, and OLMo-3-7B predict English lexical decision times beyond corpus frequency (SUBTLEX-US, Multilex) and word-level controls?

- **H1:** Each AI familiarity predictor (Apertus, GPT-4o-mini, OLMo-3-7B) will individually account for unique variance in English lexical decision times over and above corpus frequency and controls, as indicated by ΔAIC ≤ −2 (model vs M2 baseline).

**RQ2 (English):** Do AI familiarity estimates remain informative when surprisal and LLM-text-based word frequency are also included?

- **H2:** At least one AI familiarity predictor will retain a unique contribution (ΔAIC ≤ −2 relative to M7.full without AI familiarity terms) in the full model including all frequency measures and surprisal.

**RQ3 (German):** Do AI familiarity estimates from Apertus, GPT-4o-mini, and OLMo-3-7B predict German lexical decision times beyond corpus frequency (SUBTLEX-DE, childLex, Multilex) and word-level controls?

- **H3:** Mirrors H1 for German.

**RQ4 (German):** Do AI familiarity estimates remain informative in German when surprisal and LLM-text-based word frequency are also included?

- **H4:** Mirrors H2 for German.

**RQ5 (Cross-model):** How well does each AI familiarity estimate align with *human* familiarity ratings (Glasgow norms / Conde et al., 2026), and does alignment predict lexical decision validity?

- **H5:** Correlation between AI familiarity and human familiarity will be positive and substantial (r > .50) for all three LLMs, with instruction-tuned models (Apertus, GPT-4o-mini) showing higher alignment than the base model (OLMo-3-7B).

---

## Foreknowledge of Data or Evidence

**Selected option:** *Authors have observed the data, but have not performed the proposed analyses.*

**Explanation:** The human familiarity norm datasets (Glasgow norms; Conde et al., 2026) and corpus frequency resources (SUBTLEX-US, SUBTLEX-DE, childLex, Multilex) are published and have been examined by the authors for scope and variable definitions. The lexical decision datasets (English Crowdsourcing Project; DLEX; Günther et al. studies) are also published and partially known to the authors. However, none of the proposed nested regression analyses have been performed, and the AI familiarity data for Apertus and OLMo-3-7B do not yet exist (they will be generated after this plan is registered). GPT-4o-mini familiarity data comes from published norms (Brysbaert, Martínez, & Reviriego, 2024; Conde et al., 2026) and has been examined at the level of variable summaries but not in the context of the proposed models.

---

## Study Type

**Adjustment or control-based design.** The association between AI familiarity (or LLM-text-based frequency) and lexical decision times is estimated while controlling for corpus frequency measures and word-level controls, in order to isolate the unique predictive contribution of each AI predictor.

---

## Intention for Causal Interpretation

**Indirect inference on causal relationship(s).** The study is intended to examine whether the familiarity dimension captured by LLMs reflects cognitively relevant lexical knowledge, but regression on observational data cannot isolate a causal effect. Results inform the construct validity of AI familiarity as a psycholinguistic variable.

---

## Blinding

No blinding is involved. The study does not involve human subjects in data collection; all data are either existing published datasets or LLM outputs.

---

## Study Design

Two parallel within-language observational analyses (English, German) using multiple linear regression (OLS) on word-level aggregate lexical decision RTs. The design is cross-sectional at the word level; word is the sole unit of analysis. There are no random effects: participant and item variation is eliminated by aggregating RTs to word means before analysis. No between-subject or within-subject manipulation is involved.

---

## Data Collection Procedures

**Existing data**

| Dataset | Language | Source | N words (approx.) | Status |
|---|---|---|---|---|
| Glasgow Norms (human familiarity) | English | Scott et al. (2019) | 5,500
| GPT-4o-mini familiarity | English | Brysbaert, Martínez, & Reviriego (2024) | ~5,000
| English Crowdsourcing Project (LDT) | English | Mandera et al. (2020) | ~62,000
| SUBTLEX-US | English | Brysbaert & New (2009) | —

| Conde et al. (2026) human + GPT-4o-mini familiarity | German | Conde et al. (2026) | ~11,000
| Word frequency and lexical decision times | German | Brysbaert et al. (2011) | ~3000, ~370,000
| LDT | German | Günther et al. (2020) | ~5000
| childLex (LDT) | German | Schroeder et al. (2015) | ~1000

**Data generated**

1. **Apertus familiarity (English and German):** `swiss-ai/Apertus-70B-Instruct-2509` queried for the ~5,000 Glasgow words and ~11,000 German words using a prompt protocol similar to Brysbaert, Martínez, & Reviriego (2024). Prompting repeated ≥3 times per word for stability assessment. Model version and decoding settings (temperature, sampling) logged.

2. **OLMo-3-7B familiarity (English and German):** `allenai/OLMo-3-1025-7B` (base, non-instruction-tuned; trained on publicly auditable Dolma 3 corpus) queried using the same prompt protocol. Because OLMo-3-7B is a base model, familiarity is extracted via log-probability scoring of rating-scale continuations rather than instruction-style prompting; the exact extraction protocol will be appended before generation begins.

3. **LLM-text-based word frequency (English and German):** Following Schepens et al. (2025, *Open Mind*). Corpus size and generation settings will be appended before execution.

**Sampling frame:** The analysis sample is defined by the intersection of (a) words with human familiarity ratings (Glasgow / Conde et al.) and (b) words present in the lexical decision dataset. No additional sampling is performed.

---

## Sample Size

- **English:** ~5,000 words (determined by Glasgow norm coverage intersected with English Crowdsourcing Project coverage).
- **German:** ~11,000 words (determined by Conde et al. (2026) coverage intersected with DLEX / Günther et al. coverage).

Sample sizes are fixed by the intersection of existing datasets and are not determined by a power analysis. Given typical effect sizes in lexical decision modeling (AIC improvements of 10–100+ for familiarity predictors at these N), sample sizes of 5,000 and 11,000 words provide high statistical power to detect improvements exceeding the ΔAIC ≤ −2 threshold.

---

## Sample Size Rationale

Sample sizes are constrained by data availability, not by power. At N = 5,000 or 11,000 words, the ΔAIC ≤ −2 threshold is very easily exceeded for any predictor with a non-trivial effect, making the criterion practical rather than conservative.

---

## Starting and Stopping Rules

Data collection (Apertus and OLMo-3-7B familiarity generation; LLM-text corpus generation) begins after this registration is submitted. Generation stops when all target words have received at least the minimum number of repeated prompts (≥3 per word). No sequential stopping rules apply; the full word list is processed in a single pre-specified batch per model.

---

## Manipulated Variables

None. This is a non-randomized observational study.

---

## Measured Variables

**Outcome variable (both languages):**
- Mean lexical decision reaction time (RT, log-transformed) per word, from the respective lexical decision dataset.

**Primary predictors:**
- Human familiarity rating (Glasgow norms / Conde et al., 2026); mean rating per word.
- AI familiarity (Apertus): mean rating across ≥3 repeated prompts per word.
- AI familiarity (GPT-4o-mini): value from published norms.
- AI familiarity (OLMo-3-7B): log-probability score of rating-scale continuations, mean across ≥3 prompt variants per word.
- Surprisal (Apertus, GPT-4o-mini, OLMo-3-7B): log-probability of each word as an isolated out-of-context token under each model.
- LLM-text-based word frequency (Apertus, OLMo-3-7B; GPT-4o-mini where feasible): log-frequency tally from LLM-generated running text (Schepens et al., 2025).

**Corpus frequency baselines:**
- English: log SUBTLEX-US frequency (Zipf scale); log Multilex frequency.
- German: log SUBTLEX-DE frequency (Zipf scale); log childLex frequency; log Multilex frequency.

**Controls:**
- Word length in letters (confirmed covariate).
- Orthographic neighborhood size (Coltheart's N or similar).

---

## Indices

-   **AI familiarity (Apertus):** Numeric rating extracted from each LLM response per word; mean across ≥3 prompts.
-   **AI familiarity (OLMo-3-7B):** Log-probability score of rating-scale token continuations; mean across ≥3 prompt variants per word. Same SD-flagging rule applied (SD > 1.5 flagged). If the model returns a value outside a defined valid range (e.g. 1–7 or 1–10 depending on prompt format), the response is coded as missing and excluded from the mean. Inter-prompt SD will be computed and reported; words with SD > 1.5 scale units will be flagged but not automatically excluded.
-   **LLM-text-based word frequency:** raw count of the target word form in the LLM-generated corpus, divided by total corpus length, log-transformed (log10; if count = 0, assigned log10(0.5/N) with N = corpus size).
-   **Log RT:** natural log of mean reaction time in ms per word. Extreme outlier words (|z| > 3 on log RT across the dataset) will be excluded prior to analysis.

---

## Statistical Models

See Study Design for the OLS vs LME decision rule. The model set below is applied identically in English (Phase B) and German (Phase C). M0–M2 form a true nested baseline sequence. M3.*–M6.* are **parallel comparisons against M2** (each ΔAIC is computed vs M2, not vs the prior row). M7.full is the combined full model.

| Model | Predictors |
|-------|-----------|
| M0 | Intercept only |
| M1 | Controls (word length [+ orthographic neighborhood if retained]) |
| M2 | M1 + corpus frequency baselines |
| M3.apertus | M2 + surprisal (Apertus) |
| M3.gpt | M2 + surprisal (GPT-4o-mini) |
| M3.olmo | M2 + surprisal (OLMo-3-7B) |
| M4.apertus | M2 + AI familiarity (Apertus) |
| M4.gpt | M2 + AI familiarity (GPT-4o-mini) |
| M4.olmo | M2 + AI familiarity (OLMo-3-7B) |
| M5.all-fam | M2 + AI familiarity (Apertus + GPT-4o-mini + OLMo-3-7B) |
| M6.llmfreq | M2 + LLM-text-based word frequency |
| M7.full | M2 + AI familiarity (Apertus + GPT-4o-mini + OLMo-3-7B) + surprisal (Apertus + GPT-4o-mini + OLMo-3-7B) + LLM-text-based word frequency |

All continuous predictors are z-standardized before entry.

All models are fit on the same word sample (listwise deletion on the full predictor matrix ensures identical N across model comparisons).

**Confirmatory secondary analyses — AI vs. human familiarity comparison:**
-   **Convergent validity (tests H5):** Pearson correlation between each AI familiarity measure and human familiarity (Glasgow / Conde et al.) per word, reported with 95% CI and scatterplots (OLS + confidence bands) for each LLM × language combination. Confirmatory criterion: r > .50 (see H5 and Inference Criteria).
-   **Parallel predictive validity:** AIC of the AI-familiarity-only model (M2 + one AI predictor) vs. the human-familiarity-only model (M2 + human familiarity) compared directly. Confirmatory interpretation: |ΔAIC| < 2 = equivalent predictive validity; ΔAIC ≤ −2 favouring AI = AI superior; ΔAIC ≥ 2 favouring human = human superior.

**Exploratory secondary analysis:**
- **Divergence analysis:** Words where AI and human familiarity disagree most (residuals from regression of AI on human ratings per LLM) examined as an additional predictor of log RT, to test whether AI–human disagreement carries independent psycholinguistic information. No confirmatory threshold; reported as hypothesis-generating.

---

## Transformations

- **RT:** natural log transformation of mean RT in ms.
- **Frequency predictors (SUBTLEX-US, SUBTLEX-DE, childLex, Multilex, LLM-text-based):** log10 or Zipf scale as delivered by the source; z-standardized before entry.
- **Familiarity predictors (human and AI):** z-standardized before entry.
- **Surprisal:** already on a log scale; z-standardized before entry.
- **Word length:** z-standardized before entry.
- **Orthographic neighborhood size:** z-standardized before entry if retained.
- **No transformations to the outcome beyond log RT.**

Categorical variables: none planned; all predictors are continuous.

---

## Inference Criteria

**Primary confirmatory criterion (per RQ1/RQ3):** A model with an individual AI familiarity predictor (M4.apertus, M4.gpt, or M4.olmo vs M2) confirms the hypothesis if:

- ΔAIC ≤ −2 (information-criterion improvement over M2).

**Confirmatory secondary criterion — convergent validity (H5):** Pearson r between AI familiarity and human familiarity is confirmed as substantial if r > .50, with the lower bound of the 95% CI exceeding .30, for each LLM × language combination.

**Confirmatory secondary criterion — parallel predictive validity:** Comparing AIC of the AI-only model vs. human-only model (both vs. M2 baseline): |ΔAIC| < 2 is interpreted as equivalent predictive validity; ΔAIC ≤ −2 favouring AI as AI superior; ΔAIC ≥ 2 favouring human as human superior. This criterion is applied per LLM × language combination.

**Multiple comparisons:** The same model set is applied in English and German independently. No correction is applied across languages; both are confirmatory and reported jointly. Within each language, the parallel comparisons (M3.*–M6.*) are each pre-specified and do not require correction relative to each other, as they test distinct predictors.

**Equivalence:** If ΔAIC > −2 (no improvement over M2), the null result is interpreted as evidence of negligible incremental validity for that predictor.

---

## Data Inclusion and Exclusion

**Word inclusion:**
- Must have a valid human familiarity rating in the norm dataset.
- Must appear in the lexical decision dataset with a mean RT based on ≥ 10 observations.
- Must receive a valid AI familiarity response from all three LLMs (listwise deletion across models to ensure identical samples across model steps).
- Must have a valid frequency value in all corpus frequency sources used for that language.

**Word exclusion:**
- Words with mean log RT that are extreme outliers (|z| > 3 on log RT across the full analysis set) are excluded before any model fitting.
- Words for which any AI model returns only invalid or out-of-range responses after ≥3 prompt attempts are excluded.

**No participant-level exclusion** (aggregate RT data are used directly from published datasets, which have already applied their own participant-level QC).

---

## Missing Data

Listwise deletion on all analysis variables. The analysis sample is defined as the complete-case intersection of all predictors and the outcome. No imputation is performed. The final N will be reported alongside the counts of words excluded at each step.

---

## Other Planned Analysis

1. **Cross-language comparison:** Effect sizes (ΔR², standardized β) for corresponding model steps will be compared across English and German to examine replicability. This is exploratory; no confirmatory threshold applies.

2. **Reliability of Apertus and OLMo-3-7B familiarity:** Intraclass correlation coefficient (ICC) or inter-prompt SD across ≥3 repeated prompts/variants per word will be reported as a data-quality indicator.

3. **Divergence analysis (exploratory):** Residuals from regressing each AI familiarity measure on human familiarity entered as a predictor of log RT. Reported per LLM × language. No confirmatory threshold; hypothesis-generating only.

4. **Cross-language model consistency:** Standardized β values for corresponding models (e.g., M4.apertus in English vs German) will be compared narratively to assess replicability across languages. Exploratory.

5. **LLM-text-based frequency vs corpus frequency correlation:** Pearson r between LLM-text-based frequency and each corpus frequency measure reported for each LLM and language. Exploratory.

---

## Context and Additional Information

This preregistration covers only Phases B and C of a broader research plan. Phase A (leakage audit: examination of whether training data for Apertus contains the norm datasets used here) is a separate exploratory investigation with no preregistration; its results will be reported as contextual, non-confirmatory evidence.

The OLMo-3-7B model (`allenai/OLMo-3-1025-7B`) is the preregistered base model; its exact HuggingFace revision hash will be appended as a locked addendum before generation begins. The prompt protocol and decoding settings for Apertus and OLMo-3-7B will be appended. OLMo-3-7B is preferred because its training corpus (Dolma 3; 5.9T tokens, ODC-BY license) is fully open and independently auditable, and because Ai2's OlmoTrace tool allows direct tracing of model outputs back to specific training documents — directly strengthening the Phase A leakage audit. GPT-4o-mini familiarity data come from published norms and are not generated by this project.

**Decision to be locked before analysis:** Whether orthographic neighborhood size is retained as a covariate will be decided based on pre-analysis inspection of the variance inflation factor (VIF) for word length and neighborhood size; if VIF > 5 for either predictor, neighborhood size will be dropped. This decision will be recorded in a pre-analysis memo timestamped before any model fitting.

**References:**

- Brysbaert, M., Martinez, G., & Reviriego, P. (2024). Moving beyond word frequency based on tally counting: AI-generated familiarity estimates of words and phrases are an interesting additional index of language knowledge. *Behavior Research Methods*, *56*, 3180–3199. https://doi.org/10.3758/s13428-024-02561-7
- Brysbaert, M., Mandera, P., McCormick, S. F., & Keuleers, E. (2019). Word prevalence norms for 62,000 English lemmas. *Behavior Research Methods*, *51*, 467–479. https://doi.org/10.3758/s13428-018-1077-9
- Brysbaert, M., & New, B. (2009). Moving beyond Kučera and Francis: A critical evaluation of current word frequency norms and the introduction of a new and improved word frequency measure for American English. *Behavior Research Methods*, *41*(4), 977–990. https://doi.org/10.3758/BRM.41.4.977
- Brysbaert, M., Buchmeier, M., Conrad, M., Jacobs, A. M., Bölte, J., & Böhl, A. (2011). The word frequency effect: A review of recent developments and implications for the choice of frequency estimates in German. *Experimental Psychology*, *58*(5), 412–424. https://doi.org/10.1027/1618-3169/a000123
- Conde, J., Martinez, G., Grandury, M., Arriaga, C., Haro, J., Schroeder, S., Hintz, F., Reviriego, P., & Brysbaert, M. (2026). Updating the German Psycholinguistic Word Toolbox with AI-generated estimates of concreteness, valence, arousal, age of acquisition, and familiarity. *Journal of Cognition*, *9*(1), 9. https://doi.org/10.5334/joc.482
- Guenther, F., Marelli, M., & Boelte, J. (2020). Semantic transparency effects in German compounds: A large dataset and multiple-task investigation. *Behavior Research Methods*, *52*(3), 1208–1224. https://doi.org/10.3758/s13428-019-01311-4
- Mandera, P., Keuleers, E., & Brysbaert, M. (2020). Recognition times for 62 thousand English words: Data from the English Crowdsourcing Project. *Behavior Research Methods*, *52*(2), 741–760. https://doi.org/10.3758/s13428-019-01272-8
- Schepens, J., Woloszyn, H., et al. (2025). Can large language models generate useful linguistic corpora? *Open Mind*, *9*. https://doi.org/10.1162/OPMI.a.30
- Schroeder, S., Wuerzner, K. M., Heister, J., Geyken, A., & Kliegl, R. (2015). childLex: A lexical database of German read by children. *Behavior Research Methods*, *47*(4), 1085–1094. https://doi.org/10.3758/s13428-014-0528-1
- Scott, G. G., Keitel, A., Becirspahic, M., Yao, B., & Sereno, S. C. (2019). The Glasgow Norms: Ratings of 5,500 words on nine scales. *Behavior Research Methods*, *51*, 1258–1270. https://doi.org/10.3758/s13428-018-1099-3
- Team OLMo, Ettinger, A., et al. (2025). *OLMo 3* [Preprint]. arXiv. https://arxiv.org/abs/2512.13961
    