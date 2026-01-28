# adme-clearance-eda

# ADME Data Exploration: Microsomal Clearance Analysis

## Overview
This project presents an exploratory data analysis (EDA) of a small-molecule
ADME dataset containing in vitro clearance and related properties for 3,521
compounds. The aim is to understand data structure, assay coverage, and
systematic artefacts in microsomal clearance measurements prior to any
predictive modelling.

This notebook is intended as a first portfolio project demonstrating
data handling, exploratory analysis, and domain-informed interpretation
rather than model building.

---

## Dataset Description
The dataset contains:
- **3521 compounds**
- **10 columns**, including:
  - Compound identifiers and metadata
  - Chemical structure information (SMILES)
  - In vitro ADME endpoints:
    - Human liver microsomal clearance (HLM)
    - Rat liver microsomal clearance (RLM)
    - Solubility
    - Permeability
    - Plasma protein binding

Coverage varies substantially across assays, reflecting realistic
experimental availability rather than missing-at-random data.

---

## Key Analyses
The notebook covers:
- Dataset structure and completeness
- Distribution of ADME endpoints
- Vendor-level compound distribution
- Relationship between HLM and RLM clearance
- Identification of apparent assay-imposed clearance caps
- Explicit flagging of censored HLM and RLM values using boolean indicators

Capped values were **flagged but not removed or altered**, allowing transparent
handling of censored data in downstream analyses.

---

## Key Takeaways
- ADME assay coverage is heterogeneous across endpoints.
- Both HLM and RLM clearance data show evidence of upper assay detection limits.
- Domain knowledge is critical for correctly interpreting apparent value
  pile-ups in clearance data.
- Explicit flagging of censored values enables robust future modelling.

---

## Files
- `01-data-exploration.ipynb` – main exploratory analysis notebook
- `data/` – input dataset (if publicly shareable)

---

## Next Steps
Future work will focus on:
- Feature generation from chemical structure
- Predictive modelling of microsomal clearance
- Appropriate treatment of censored response variables

---

## Author
**Adrian Walker**  
Background in pharmaceutical ADME research with a focus on applying data
science methods to drug discovery datasets.
