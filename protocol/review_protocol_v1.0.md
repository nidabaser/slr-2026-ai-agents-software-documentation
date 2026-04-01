# Review Protocol v1.0
## Systematic Literature Review: AI Agents for Software Documentation

> **Status:** FROZEN  
> **Version:** 1.0  
> **Date Frozen:** 2026-04-02  
> **Git Tag:** `protocol-v1.0`  
> **Methodology:** Kitchenham & Charters (2007) — *Guidelines for Performing Systematic Literature Reviews in Software Engineering*

---

## ⚠️ Protocol Integrity Notice

This document was finalized and committed **before** any database searches were executed. It must not be modified retroactively. If amendments are required after search commencement, create a new versioned file (`review_protocol_v1.1.md`) and document the reason for change in `CHANGELOG.md`. The original v1.0 must remain unaltered.

---

## 2. Research Questions

The following research questions were defined prior to search and guide all phases of this review.

| ID | Research Question |
|----|-------------------|
| **RQ1** | What AI agent architectures and approaches are used for software documentation tasks? |
| **RQ2** | What types of documentation can AI agents generate (API docs, tutorials, in-code comments, architecture diagrams)? |
| **RQ3** | What evaluation metrics and benchmarks are used to assess documentation quality? |
| **RQ4** | What are the reported benefits and limitations compared to human-written documentation? |
| **RQ5** | How do AI agents address documentation debt and maintenance challenges? |

---

## 3. Search Strategy

### 3.1 Search Databases

Searches will be conducted independently on each of the following databases:

| Database | URL |
|----------|-----|
| IEEE Xplore | https://ieeexplore.ieee.org |
| ACM Digital Library | https://dl.acm.org |
| Scopus | https://www.scopus.com |
| arXiv (via Semantic Scholar or direct) | https://arxiv.org |
| Google Scholar (supplementary) | https://scholar.google.com |

### 3.2 Final Search String

The following search string will be applied to title, abstract, and keywords fields in all databases. Minor syntax adaptations (Boolean operators, wildcard notation) will be applied per database as required and documented in `search/search_log.md`.

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

### 3.3 Search Log Requirements

For every database search, the following must be recorded in `search/search_log.md`:

- Database name
- Exact date of search
- Exact query string used (including any database-specific syntax)
- Filters applied (date range, language, document type)
- Total number of results returned

### 3.4 Supplementary Search

To reduce the risk of missing relevant work:

- **Forward citation search** on five anchor papers (DocAgent, RepoAgent, Hydra-Reviewer, RepoAgent, Who Writes the Docs) using Google Scholar "Cited by."
- **Backward reference search** (reference list scanning) of all included primary studies.
- Supplementary results will be documented separately in `search/search_log.md` and subjected to the same inclusion/exclusion criteria.

---

## 4. Inclusion and Exclusion Criteria

Criteria are applied in two sequential stages: (1) title and abstract screening, and (2) full-text assessment. Criteria are listed in priority order — any single exclusion criterion is sufficient for exclusion.

### 4.1 Inclusion Criteria

A study must satisfy **all** of the following:

| # | Criterion |
|---|-----------|
| IC1 | Published between **2021 and 2025** (inclusive). *Rationale: capture the LLM era of documentation agents; pre-2021 work predates widespread LLM adoption.* |
| IC2 | Written in **English**. |
| IC3 | **Full-text accessible** via institutional or open access. |
| IC4 | Presents an **AI-based system, tool, or agent** that generates, evaluates, or maintains software documentation. |
| IC5 | Includes **empirical evaluation** of the proposed approach (quantitative or qualitative) OR sufficient implementation detail to assess technical contribution. |
| IC6 | Published in a **peer-reviewed venue** (see venue lists below) OR as an arXiv preprint with a documented conference/journal submission or ≥10 citations. |

**Target venues — Software Engineering:**
ICSE, FSE/ESEC, ASE, ICSME, MSR, ICPC, SANER, EASE

**Target venues — AI/NLP:**
ACL, EMNLP, NAACL, NeurIPS, ICML, ICLR (papers with code/documentation focus)

**Target journals:**
TSE, TOSEM, EMSE, JSS, IST, ASE (Automated Software Engineering journal)

### 4.2 Exclusion Criteria

A study will be excluded if it meets **any** of the following:

| # | Criterion |
|---|-----------|
| EC1 | **Technical reports, white papers, or concept papers** without peer review. |
| EC2 | **Position papers** or vision papers without implementation or empirical evaluation. |
| EC3 | **No implementation details** provided — system cannot be assessed technically. |
| EC4 | The tool or system relies solely on **non-AI methods** (static analysis, template-based, regex) with no learned model component. |
| EC5 | Documentation is **not the primary focus** — studies where documentation is a minor side output of a code generation or testing system. |
| EC6 | **Duplicate publication** — keep the most complete version (typically the journal extension over conference paper). |
| EC7 | **Non-English** language. |
| EC8 | **Out of scope domain** — documentation for hardware, natural language text, or non-software artifacts. |

---

## 5. Study Selection Process

### 5.1 Deduplication

After all database searches are complete, all records will be merged into a single reference manager (Zotero). Deduplication will be performed using Zotero's built-in duplicate detection, with manual verification of near-duplicate titles. The deduplication log will record: total records pre-dedup, duplicates removed, and total records post-dedup.

### 5.2 Stage 1: Title and Abstract Screening

- All records post-deduplication will be screened by **title and abstract** against IC1–IC6 and EC1–EC8.
- Screening will be performed using the `SLR_Screening_Log.xlsx` sheet.

### 5.3 Stage 2: Full-Text Assessment

- Full texts of all records passing Stage 1 will be retrieved and assessed against all inclusion/exclusion criteria.
- Each record will receive one of two decisions: `INCLUDE` or `EXCLUDE`.

### 5.4 PRISMA Reporting

A PRISMA 2020 flow diagram will be produced documenting record counts at each stage. The live tracker is maintained in the `PRISMA Flow` sheet of `screening/PRISMA_Flow.xlsx`.

---

## 6. Reporting

The final paper sections will include:

1. Introduction
2. Methodology (this protocol summarized)
3. Results (per RQ)
4. Discussion
5. Threats to Validity
6. Conclusion

The PRISMA flow diagram and all other files will remain publicly available in this repository to support reproducibility.

---

## 7. References

- Kitchenham, B., & Charters, S. (2007). *Guidelines for performing systematic literature reviews in software engineering.* Technical Report EBSE-2007-01, Keele University and University of Durham.
- Moher, D., et al. (2009). Preferred Reporting Items for Systematic Reviews and Meta-Analyses: The PRISMA Statement. *PLOS Medicine.*
- Page, M.J., et al. (2021). The PRISMA 2020 statement: an updated guideline for reporting systematic reviews. *BMJ.*

---

*This protocol is version-controlled. Do not edit this file. For amendments, create `review_protocol_v1.1.md` and log changes in `CHANGELOG.md`.*
