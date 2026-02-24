# Tiny-Aya-Water Blind Spot Analysis

This repository contains an evaluation study of the language model:

**CohereLabs/tiny-aya-water**  
https://huggingface.co/CohereLabs/tiny-aya-water

The objective of this project is to identify and document systematic blind spots in the model through targeted prompting and structured failure analysis.

---

## Project Overview

Large Language Models often perform well on benchmark datasets but can exhibit consistent weaknesses when tested under controlled adversarial conditions.

This repository provides:

- A structured blind-spot evaluation dataset
- A reproducible evaluation notebook
- Categorized model failures
- A public Hugging Face dataset artifact

The focus areas include:

- Logical reasoning
- Arithmetic reasoning
- Transitive inference
- Coreference resolution
- Instruction following
- Counterfactual reasoning
- Historical factual accuracy
- Translation robustness
- Output format compliance

---

## Repository Structure
→ tiny-aya-water-blind-spots.ipynb # Evaluation notebook
→ blind_spots_tiny_aya.csv # Structured dataset
→ README.md # Project documentation


---

## Dataset

The structured dataset is publicly available on Hugging Face:

→  https://huggingface.co/datasets/chrishounwanou/tiny-aya-water-blind-spots

### Dataset Columns

- `input` - Prompt given to the model  
- `expected_output` - Ground truth or logically correct answer  
- `model_output` - Actual generated response  
- `failure_type` - Categorized model weakness  

---

##  Reproducibility

### 1. Install Dependencies

```bash
pip install transformers accelerate torch bitsandbytes huggingface_hub

```

### 2. Authentication

The model requires authentication.

→ Create a Hugging Face token:

    https://huggingface.co/settings/tokens

Then login

### 3. Model Loading (8-bit Quantization)

The model was loaded using 8-bit quantization to reduce memory usage.

### 4. Evaluation Function

All prompts were evaluated using the following controlled generation setup: generate_reponse (prompt)

---

## Observed Failure Categories

The evaluation identified consistent blind spots in:

→ Multi-step reasoning
→ Arithmetic execution
→ Logical entailment
→ World knowledge override vs premise reasoning
→ Coreference disambiguation
→ Instruction-following precision
→ Output formatting constraints
→ Repetition loops
→ Historical factual hallucinations

---

## Model Reference

Model evaluated:

→ https://huggingface.co/CohereLabs/tiny-aya-water

---

## License 

This repository contains evaluation artifacts and structured prompts for research and educational purposes.
