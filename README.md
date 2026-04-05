# 🔍 Systematic Literature Review: AI Agents for Software Documentation

[![Protocol Status](https://img.shields.io/badge/Protocol-Frozen%20v1.0-blue)](./PROTOCOL.md)
[![Screening Status](https://img.shields.io/badge/Screening-In%20Progress-yellow)](./screening/)
[![Papers Included](https://img.shields.io/badge/Papers%20Included-TBD-lightgrey)](./screening/SLR_DataExtraction.xlsx)
[![Methodology](https://img.shields.io/badge/Methodology-Kitchenham%20%26%20Charters-green)](./protocol/review_protocol_v1.0.md)
[![License](https://img.shields.io/badge/License-CC%20BY%204.0-orange)](./LICENSE)

> A Kitchenham & Charters compliant Systematic Literature Review investigating how artificial intelligence agents are used to generate, maintain, and evaluate software documentation.

---

## 📋 Research Questions

| ID | Research Question |
|----|-------------------|
| **RQ1** | What AI agent architectures and approaches are used for software documentation tasks? |
| **RQ2** | What types of documentation can AI agents generate (API docs, tutorials, in-code comments, architecture diagrams)? |
| **RQ3** | What evaluation metrics and benchmarks are used to assess documentation quality? |
| **RQ4** | What are the reported benefits and limitations compared to human-written documentation? |
| **RQ5** | How do AI agents address documentation debt and maintenance challenges? |

---

## 🗂️ Repository Structure

```
slr-ai-agents-software-documentation/
│
├── README.md                          # This file
├── PROTOCOL.PDF                        # Full review protocol (frozen)
├── CHANGELOG.md                       # Decision and version history
│
├── protocol/
│   ├── review_protocol_v1.0.md        # Frozen protocol (do not overwrite)
│   ├── inclusion_exclusion_criteria.md
│   └── search_strings.md
│
├── search/
│   ├── search_log.md                  # Date, database, query, result count
│   └── deduplication_log.md
│
├── screening/
│   ├── SLR_Screening_Log.xlsx        # Screening log
│   ├── title_abstract_screening.md
│   └── fulltext_screening.md
│
├── papers/
│   ├── included/                      # Included PDFs
│   └── excluded/                      # Excluded PDFs
│
├── writing/
│   ├── drafts/                        # Versioned drafts (never delete old versions)
│   ├── sections/                      # Active section files
│   └── figures/                       # PRISMA diagram
│
├── references/
│   ├── library.bib                    # Master BibTeX
│   └── citation_notes.md
│
└── .github/
    └── ISSUE_TEMPLATE/
        └── decision_needed.md
```

---

## 🔬 Methodology

This review follows the **Kitchenham & Charters (2007)** guidelines for conducting systematic literature reviews in software engineering.

### Search Databases

| Database | Status | Records |
|----------|--------|---------|
| IEEE Xplore | ✅ Completed | 269 |
| ACL Anthology | ✅ Completed | 56 |
| Scopus | ✅ Completed | 396 |
| Google Scholar | ✅ Completed | 61 |
| **Total** | | **n = 782** |
| Total (after deduplication) | - 178 excluded | 604 |
| Pre-Screening (keyword excluded) | - 412 excluded | 192 |
| Title Abstract (T/A) Screening | - 131 excluded | 61 |
| Full-text Screening | - 40 excluded | 21 |
| **Final Studies included in SLR** |  | **n = 21** |

### Search String

```
("AI agent" OR "autonomous agent" OR "LLM agent" OR "language agent"
 OR "large language model" OR "LLM" OR "neural" OR "deep learning")
AND
("software documentation" OR "code documentation" OR "API documentation"
 OR "code comment*" OR "code summarization" OR "program comprehension"
 OR "docstring generation" OR "README generation")
AND
("generation" OR "synthesis" OR "automatic" OR "automated")
```

### Inclusion Criteria

- **Databases:** IEEE Xplore, ACL Anthology, Scopus, Google Scholar
- **SE Venues:** ICSE, FSE, ASE, ICSME, MSR, ICPC
- **AI/ML Venues:** ACL, EMNLP, NeurIPS, ICML (with code focus)
- **Journals:** TSE, TOSEM, EMSE, JSS
- **Publication years:** 2021–2026
- Studies with empirical evaluation or implementation
- English language, full-text accessible

### Exclusion Criteria

- Technical reports, white papers, position papers without evaluation
- Studies without implementation details
- Non-AI documentation tools (static analysis only, template-based)
- Duplicate publications (keep most complete version)

---

## 📊 Current Progress

### PRISMA Flow (Live)

```
Identification:   782 records
After dedup:      604
Pre-Screening:    192 pass / 412 excluded
T/A Screening:    61 pass / 131 excluded
Full-text:        21 assessed / 40 excluded
INCLUDED:         21
```
---

## 🤖 AI-Assisted Workflow & Academic Integrity

This review uses AI tools (Claude) in a **strictly assistive role**, following the declared process in [`protocol/review_protocol_v1.0.md`](./protocol/review_protocol_v1.0.md).

| ✅ AI IS used for | ❌ AI is NOT used for |
|-------------------|-----------------------|
| Editing and improving drafted text | Writing sections from scratch |
| Suggesting structure and flow | Generating paper summaries to replace reading |
| Checking logical gaps in arguments | Making inclusion/exclusion decisions |
| Formatting citations and references | Interpreting findings |
| Suggesting additional search terms | Any text copied without substantial revision |

All screening decisions, data extraction, analysis, and writing are performed by the human author(s). AI assistance is limited to productivity and quality improvement on already-drafted content.

---

## 🏷️ Version Tags

| Tag | Description |
|-----|-------------|
| `protocol-v1.0` | Protocol frozen before search began |
| `search-complete` | All databases searched |
| `screening-complete` | PRISMA screening finalized |
| `extraction-complete` | All data extraction verified |
| `submission-v1` | First arXiv submission |

---

## 👤 Authors

**Nida BAŞER**
| [Institution](ogu.edu.tr)
| [Email](501720241001@ogrenci.ogu.edu.tr)
| [Personal email](nida.bsr@gmail.com)
| [ORCID](https://orcid.org/0000-0001-5016-7456)

**Dr. Damla SİVRİOĞLU ASLAN**
| [Institution](company)
| [Email](your@email.com)
| [Personal email](your@email.com)
| [ORCID](https://orcid.org/0000-xxxx-xxxx-xxxx)

**Dr. Berna ATAK BÜLBÜL**
| [Institution](company)
| [Email](your@email.com)
| [Personal email](your@email.com)
| [ORCID](https://orcid.org/0000-xxxx-xxxx-xxxx)

---

## 📄 License

This repository's content (protocol, extraction forms, notes) is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
Included paper PDFs are subject to their respective publisher licenses.

---

## 📚 Citation

Once published, cite this review as:

```bibtex
@article{slr2026,
  title   = {A Systematic Literature Review of AI Agents for Software Documentation},
  author  = {Your Name},
  journal = {arXiv preprint},
  year    = {2025},
  url     = {https://arxiv.org/abs/XXXX.XXXXX}
}
```

---
*Protocol registered / timestamped via Git tag `protocol-v1.0` on [02.04.2026]. Search conducted after protocol was frozen.*
