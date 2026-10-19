---
language:
  - en
  - pl
license: cc-by-4.0
pretty_name: "Psychology Games — Bilingual (EN/PL) Taxonomy v5 of Psychological Experiments, Games, and Phenomena with Evidence-Graded Claims"
description: "Bilingual (English and Polish) open dataset of 28 canonical psychological experiments, cognitive tasks, decision games, interpersonal manipulation patterns, and clinical/historical artifacts from https://psychology.games, featuring formal Taxonomy v5 placement rules, safety & awareness-asymmetry metadata, 190+ atomic empirical claims with evidence grades, and 215+ audited bibliographic sources with DOIs."
size_categories:
  - n<1K
task_categories:
  - text-classification
  - question-answering
  - text-retrieval
tags:
  - psychology
  - cognitive-science
  - behavioral-economics
  - game-theory
  - taxonomy
  - fact-checking
  - bilingual
  - polish
---

# Psychology Games — Bilingual (EN/PL) Taxonomy v5 & Evidence-Graded Claims Dataset

An open research and educational dataset from **[Psychology Games (psychology.games)](https://psychology.games/)** (Polish edition: **[psychology.games/pl](https://psychology.games/pl/)**), providing a formal, rule-governed **Taxonomy v5** of psychological experiments, decision-theoretic games, perceptual illusions, persuasion tactics, and interpersonal phenomena, paired with **atomic, evidence-graded empirical claims** and **audited primary-source bibliography**.

- **Live Reference & Interactive Demonstrations (EN):** [https://psychology.games/](https://psychology.games/)
- **Polska edycja serwisu (PL):** [https://psychology.games/pl/](https://psychology.games/pl/)
- **All Entries Index:** [https://psychology.games/entries](https://psychology.games/entries) · [https://psychology.games/pl/entries](https://psychology.games/pl/entries)
- **Taxonomy Categories:** [https://psychology.games/categories](https://psychology.games/categories) · [https://psychology.games/pl/categories](https://psychology.games/pl/categories)
- **Psychological Mechanisms:** [https://psychology.games/mechanisms](https://psychology.games/mechanisms) · [https://psychology.games/pl/mechanisms](https://psychology.games/pl/mechanisms)
- **Bibliography & Primary Sources:** [https://psychology.games/sources](https://psychology.games/sources) · [https://psychology.games/pl/sources](https://psychology.games/pl/sources)

> [!IMPORTANT]
> **Educational & Non-Clinical Disclaimer:** This dataset and the [psychology.games](https://psychology.games/) reference site are strictly educational, historical, and methodological resources. They are **not** clinical, diagnostic, or therapeutic instruments.

---

## Package Contents (`open-data/`)

| File | Records | Description |
| --- | ---: | --- |
| `psychology-games-entries-taxonomy.json` / `.csv` | **28 entries** (EN + PL) | Bilingual entry records covering canonical experiments (*Asch conformity*, *Milgram obedience*, *Stanford prison*), cognitive tasks (*Stroop task*, *Wason selection task*, *DRM false memory*, *Linda problem*, *Monty Hall*, *Müller-Lyer*), strategic games (*Prisoner's Dilemma*, *Ultimatum Game*, *Keynesian beauty contest*), interpersonal patterns (*gaslighting*, *love bombing*, *stonewalling*, *foot-in-the-door*, *good cop/bad cop*, *cold reading*, *dark patterns*, *phishing*, *Ponzi scheme*), and cultural/clinical artifacts (*Rorschach inkblot test*, *Heinz dilemma*, *Trolley problem*, *Chinese room*, *Progressive muscle relaxation*, *Papers, Please*, *Silent Hill 2*). Includes formal Taxonomy v5 placement rules, rejected near-misses, mechanisms, safety flags, awareness asymmetry, and structured synthesis sections (`what_is_happening`, `what_this_shows`, `what_this_does_not_show`, `research_and_limitations`). |
| `psychology-games-empirical-claims.json` / `.csv` | **190+ claims** (EN + PL) | Atomic factual, empirical, and historical claims extracted from every entry (`[[c:claim-id]]`), annotated with `evidence_grade` (`replicated_finding`, `supported_with_limits`, `historical_or_descriptive`, `contested_or_mixed`, `conceptual_or_normative`), `is_central_claim`, bilingual claim text, and verbatim `support_notes_en` linking to exact pages/tables in primary sources. |
| `psychology-games-bibliography-sources.json` / `.csv` | **215+ sources** | Audited bibliography of primary papers, meta-analyses, monographs, and official records with DOIs/URLs, `source_type`, `opened_by_model` provenance flag, and methodological verification notes. |

---

## Taxonomy v5 Architecture

Every entry in [psychology.games](https://psychology.games/) is classified along two orthogonal axes plus an explicit safety & asymmetry profile:

1. **Primary Category (`primary_category`):**
   - `knowledge.studies` — Bounded historical research programs (*Asch*, *Milgram*, *Stanford prison*)
   - `instruments.tasks_and_paradigms` / `instruments.tests` / `instruments.dilemmas_and_thought_experiments` / `instruments.exercises` — Structured procedures, tasks, and thought experiments (*Stroop*, *Wason*, *DRM*, *Trolley*, *Heinz*, *Chinese room*, *Rorschach*, *PMR*)
   - `games.formal_and_strategic` / `games.video_and_tabletop` — Strategic decision games and playable media (*Prisoner's Dilemma*, *Ultimatum Game*, *Keynesian beauty contest*, *Papers, Please*, *Silent Hill 2*)
   - `interpersonal.persuasion_and_compliance` / `interpersonal.deception_and_exploitation` / `interpersonal.coercive_and_abusive_patterns` — Asymmetric influence, manipulation, and coercive relational patterns (*foot-in-the-door*, *cold reading*, *dark patterns*, *phishing*, *Ponzi scheme*, *gaslighting*, *love bombing*, *stonewalling*, *good cop/bad cop*)
   - `phenomena.illusions_and_biases` — Perceptual and judgmental phenomena (*Müller-Lyer illusion*, *Linda problem*, *Monty Hall problem*)
2. **Primary & Secondary Psychological Mechanisms (`primary_mechanism`):** `social_influence_conformity`, `authority_obedience`, `strategic_interdependence`, `heuristics_framing_judgment`, `memory_reconstruction`, `perception_awareness`, `attention_automaticity_conflict`, `moral_reasoning_norms`, `coercive_control_erosion`, `deception_trust_exploitation`, `emotion_arousal_regulation`.
3. **Explicit Placement Audit (`placement`):** Each entry records its constituting source, normalization rule, and why competing near-miss categories were rejected.

---

## License & Citation (CC BY 4.0)

This dataset is licensed under **[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)**.

When using this dataset in NLP/LLM fact-checking benchmarks, psychology education, or taxonomy research, please attribute:

> **Source:** *Psychology Games — Interactive Reference & Taxonomy v5 of Psychological Experiments, Games, and Phenomena* ([https://psychology.games](https://psychology.games) / [https://psychology.games/pl](https://psychology.games/pl)), licensed under CC BY 4.0.

```bibtex
@dataset{psychology_games_taxonomy_2026,
  title        = {Psychology Games: Bilingual (EN/PL) Taxonomy v5 of Psychological Experiments, Games, and Phenomena with Evidence-Graded Claims},
  author       = {Pytlarz, Piotr},
  year         = {2026},
  version      = {1.0.0},
  publisher    = {psychology.games},
  url          = {https://psychology.games/},
  license      = {CC-BY-4.0}
}
```
