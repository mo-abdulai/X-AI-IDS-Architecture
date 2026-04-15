# AGENTS.md

## Purpose
This file gives working guidance for coding agents and contributors in this repository.

## Project Context
- Project: `X-AI-IDS-Architecture`
- Domain: Explainable intrusion detection (NSL-KDD and CICIDS-2017)
- Workflow style: mostly Jupyter notebooks organized by phase

## Repository Layout
- `1_Pre-Modeling-Phase/`: data analysis and preprocessing notebooks
- `2_Modeling-Phase/`: model training/evaluation notebooks and train/test datasets
- `3_Post-Modeling-Phase/`: explainability notebooks and saved trained models
- `Datasets/`: raw benchmark datasets

## Working Rules
- Prefer minimal, targeted edits; do not refactor unrelated cells/files.
- Preserve existing pipeline behavior unless the task explicitly asks for changes.
- Keep class label order consistent in multi-class IDS experiments:
  - `0: Normal`, `1: DoS`, `2: Probe`, `3: R2L`, `4: U2R`
- Add comments for non-obvious logic (especially imbalance handling and evaluation).
- Avoid hardcoding new absolute local paths unless required.

## Modeling & Evaluation Expectations
For multi-class evaluation, include:
- Raw confusion matrix (counts)
- Row-normalized confusion matrix (`normalize='true'`)
- Class-wise precision, recall, F1-score
- `classification_report` output
- Metrics robust to class imbalance (macro and weighted views)

## Imbalance Handling
- Prefer configurable toggles for experiments:
  - class weighting
  - optional SMOTE on training split only
- Do not oversample validation/test sets.
- Keep ablation-friendly controls so paper tables can compare:
  - baseline
  - class weights only
  - SMOTE only
  - class weights + SMOTE

## Notebook Hygiene
- Keep markdown headings clear and ordered.
- Ensure new cells run in sequence without hidden dependencies.
- When adding plots for publication, use readable labels/titles and high-resolution output.

## Deliverable Standard
Any update should provide:
- exact file(s) changed
- what was changed
- why it was changed
- whether execution/testing was run and any limitations
