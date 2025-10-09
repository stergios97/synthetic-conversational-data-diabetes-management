# Synthetic Patient–Agent Dialogues for Type 2 Diabetes Management

# Overview
This repository contains the code, data, and supporting materials for the paper **"A Synthetic Conversational Dataset for Type 2 Diabetes Management"**, submitted to **LREC 2026**.

**Note: This repository is part of an anonymous submission. Full dataset and code documentation, as well as citation details will be provided upon acceptance of the paper.**

The repository includes:
- **Synthetic Data**: Persona biographies and multi-turn patient–agent conversations, along with the prompts used for their generation.
- **Annotation Resources**: The complete SPO annotation schema, detailed annotation guidelines, and the annotated datasets (train, validation, and test splits).
- **Conversational Triple Extraction (CTE)**: Source code and baseline models for rule-based, prompt-based, and fine-tuned approaches.
- **Evaluation Materials**: The SPACEQ questionnaire and corresponding rating rubric used for LLM- and expert-based evaluation of dialogue quality.

To ensure anonymity for review, all identifying information (authors, affiliations, and institutional details) has been removed.

# Contents
## 1. Dataset

The `dataset/` directory includes all data resources used and described in the paper.

### 1.1 `dataset/dialogues/`

Contains all generated and annotated dialogues between the synthetic patients and the conversational agent.

- **`raw_conversations.txt`** – The full set of generated synthetic conversations before annotation.  
- **`annotated/`** – The annotated dialogues for the Conversational Triple Extraction (CTE) task:
  - `train.csv` – Training split  
  - `validation.csv` – Validation split  
  - `test.csv` – Test split  

### 1.2 `dataset/personas/`

Stores the patient persona profiles used to guide conversation generation.

- **`personas_bios.txt`** – Full textual biographies of each synthetic patient persona.  
- **`personas_metadata.json`** – Structured metadata describing demographic and lifestyle attributes (e.g., age, gender, ethnicity, place of birth).

### 1.3 `dataset/prompts/`

Includes all prompt templates used throughout the data generation and annotation process.

- **`persona_generation_prompts.json`** – Prompts used to generate the synthetic patient persona descriptions.  
- **`dialogue_generation_prompts.json`** – Prompts used to generate the multi-turn dialogues between each patient and the conversational agent.  
- **`annotation_prompt.txt`** – Prompt used for automated SPO annotation via large language models.  
- **`profile.json`** – Supporting configuration file containing persona attribute fields used during prompt formatting.

---

## 2. Documentation

- **`docs/annotation_guidelines.pdf`**  
  Comprehensive guidelines for annotating synthetic patient–agent dialogues with Subject–Predicate–Object (SPO) labels.  
  This document explains the labeling schema, token-level annotation conventions, and includes detailed examples.

- **`docs/questionnaire_SPACEQ.pdf`**  
  The *Synthetic Patient–Agent Conversation Evaluation Questionnaire (SPACEQ)* used in the human evaluation study.  
  It contains the questionnaire items and rating rubric, inspired by Holmes et al.’s Chatbot Usability Questionnaire (CUQ).

---

## 3. How to Use

All dataset files are stored in plain text or CSV format and can be accessed directly without running any code.

Researchers can reproduce the dialogue generation and annotation processes using the provided prompts.

Code for conversational triple extraction baselines (**rule-based**, **GPT-based**, and **fine-tuned BERT**) is included under the `code/` directory.

## Quick navigation

| Area | Path |
|---|---|
| Raw dialogues | [`dataset/dialogues/raw_conversations.txt`](dataset/dialogues/raw_conversations.txt) |
| Annotated train | [`dataset/dialogues/annotated/train.csv`](dataset/dialogues/annotated/train.csv) |
| Annotated validation | [`dataset/dialogues/annotated/validation.csv`](dataset/dialogues/annotated/validation.csv) |
| Annotated test | [`dataset/dialogues/annotated/test.csv`](dataset/dialogues/annotated/test.csv) |
| Persona bios | [`dataset/personas/personas_bios.txt`](dataset/personas/personas_bios.txt) |
| Persona metadata | [`dataset/personas/personas_metadata.json`](dataset/personas/personas_metadata.json) |
| Persona prompts | [`dataset/prompts/persona_generation_prompts.json`](dataset/prompts/persona_generation_prompts.json) |
| Dialogue prompts | [`dataset/prompts/dialogue_generation_prompts.json`](dataset/prompts/dialogue_generation_prompts.json) |
| Annotation prompt | [`dataset/prompts/annotation_prompt.txt`](dataset/prompts/annotation_prompt.txt) |
| Annotation guidelines | [`docs/annotation_guidelines.pdf`](docs/annotation_guidelines.pdf) |
| SPACEQ questionnaire | [`docs/questionnaire_SPACEQ.pdf`](docs/questionnaire_SPACEQ.pdf) |

# Requirements
This repository contains scripts implemented using Python 3.12.3 and Python 3.13.5.

Key packages include: 
```bash
numpy pandas torch spacy scikit-learn transformers optuna matplotlib openai contractions deepeval
```

# Reproducibility Note
All scripts used to generate and evaluate the dataset are included for transparency.  

The code is provided for inspection purposes only and does not need to be executed to use the dataset.

# License
To be specified after acceptance.

# Citation
Citation information will be added upon acceptance of the paper.


