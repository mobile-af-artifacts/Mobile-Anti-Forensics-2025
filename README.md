# Mobile Anti-Forensics 2025: Datasets and Supplementary Materials

This repository contains the datasets, figures, and supplementary analysis files used in the study:

**"Understanding Mobile Anti-Forensics: Techniques, Evidence Persistence, and the Future of Digital Forensics" (2025)**

---

## Overview

This research provides a comprehensive **Systematic Literature Review (SLR)** of **Anti-Forensics (AF)**, with a particular focus on **Mobile Anti-Forensics (MAF)**.  
The study analyzed **197 primary papers published between 2005 and 2024** to identify AF techniques, platform distribution, and residual forensic artifacts after AF activity.

All data files in this repository directly support the quantitative analyses and visualizations reported in the paper (Sections **RQ1–RQ3**).

---

## Repository Structure

| Section | Description | Files |
|----------|--------------|-------|
| **RQ1 — Anti-Forensic Techniques Examined** | Datasets related to AF taxonomy, high-level categories, and domain-level publication patterns. | `techniques_flat.xlsx`, `Domains.xlsx`, `publishers_domain_distribution_with_CV.csv`, `subcategory_pgfplots_data_top15.csv` |
| **RQ2 — Platform and Device Focus** | Data showing platform/device distribution, category mix, and yearly research trends. | `rq2_device_type_counts.csv`, `rq2_platform_totals_unique_papers.csv`, `rq2_category_mix_by_platform_percent.csv`, `rq2_device_type_share_by_year.csv` |
| **RQ3 — Residual Forensic Artifacts on Mobile Devices** | Data mapping residual artifacts, their storage locations, and platform-level persistence. | `RQ3_mobile_stack_counts.csv`, `RQ3_category_by_type_counts.csv`, `RQ3_platform_by_type_counts.csv`, `RQ3_mobile_long.csv`, `RQ3_mobile_matrix_clean.xlsx` |

Each dataset is cited within the manuscript and directly supports a corresponding figure or table in the published paper.

---

## Research Questions

1. **RQ1:** What anti-forensic techniques and tools have been examined in the literature?  
2. **RQ2:** To what extent have these studies focused on mobile versus non-mobile platforms?  
3. **RQ3:** What forensic artifacts persist after anti-forensic activity on mobile devices?

---

## Key Findings

- **RQ1:** AF research has evolved from data-hiding and wiping methods to AI-driven adversarial deception.  
- **RQ2:** Research remains dominated by desktop and open systems (Windows, Android), with limited cross-platform validation.  
- **RQ3:** AF rarely achieves full erasure; evidence often persists in SQLite databases, logs, and file-system metadata.

---

## Data Format and Usage

All datasets are provided in `.csv` or `.xlsx` format and can be analyzed directly in **Python (pandas)**, **R**, or **Excel**.  
Column names are self-descriptive and correspond to variables referenced in the paper.

Example (Python):
```python
import pandas as pd
df = pd.read_csv("rq2_device_type_counts.csv")
df.head()
