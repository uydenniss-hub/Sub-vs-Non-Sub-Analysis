# Chapters per Story Analysis: Subscriber vs Non-Subscriber

This project analyzes story depth for subscribers compared to non-subscribers using a dataset of **500 rows** and **324 stories** (snapshot 2025-09-17).

## Key Results
- **Average chapters per story**
  - Subscribers: **1.388**
  - Non-subscribers: **1.561**
- **Distribution**
  - One-chapter stories: Subs 77.5%, Non-subs 75.8%
  - 3+ chapters: Subs 10.0%, Non-subs 12.3%
- **Cohorts**
  - Account age: median 0 months for both
  - Remaining credits: Subs 440 vs Non-subs 5 (median)

## Method
- Cleaned and typed fields with **pandas** and **openpyxl**.
- Built an unbiased per-story metric: distinct chapter numbers per `(Is Subscriber, StoryId)`.
- Aggregated averages and medians across groups.
- Visualized distributions using **seaborn** and **matplotlib**.

## Deliverables
- Reproducible code and notebooks for EDA and plotting.
- Visuals comparing chapter depth and cohort stats.
- Written analysis with experiment-ready recommendations:
  - Continuation nudges
  - Resume surface
  - Next-chapter scaffolds
  - Credit-urgency prompts

## Tools
- Python
- pandas
- seaborn / matplotlib
- openpyxl for Excel I/O

## How to Reproduce
```bash
# create environment
python -m venv .venv && source .venv/bin/activate
pip install pandas seaborn matplotlib openpyxl
