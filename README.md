# ERNIE Fine-Tuning using Unsloth

This repository demonstrates parameter-efficient fine-tuning of ERNIE-4.5 using LoRA adapters via Unsloth for accurate Indian income tax regime question answering (Assessment Year 2024–25).

The project focuses on correcting factual errors commonly observed in web-trained language models, particularly around Old vs New Tax Regime distinctions (for example, Section 80C deductions).

---

## Project Overview

Large language models often produce confident but incorrect answers in regulatory and statutory domains. In Indian income tax law, a frequent failure case is the incorrect claim that certain deductions (such as Section 80C) are available under the New Tax Regime.

This project fine-tunes ERNIE-4.5 using:
- A curated, regime-aware dataset
- Answer-only supervision
- LoRA-based parameter-efficient fine-tuning

The result is a model that produces factually consistent, regime-sensitive answers while retaining general language fluency.

---

## Key Features

- ERNIE-style structured prompts  
  Entity → Attributes → Query → Answer

- Answer-only loss to focus learning on factual correctness  
- Explicit Old vs New regime contrast examples  
- Efficient LoRA fine-tuning (less than 1% trainable parameters)

---

## Example

Query:  
Is Section 80C deduction available under the new tax regime?

Base ERNIE Output:  
Yes, Section 80C deduction is available under the new tax regime.

Fine-Tuned ERNIE Output:  
No. Section 80C deductions are not available under the new tax regime.

---

## Repository Structure

Ernie-Finetuning-using-Unsloth  
├── ernie_finetuning.ipynb  
├── README.md  
├── requirements.txt  

---

## Running the Notebook

1. Open the notebook in Google Colab  
2. Run all cells sequentially  
3. GPU runtime is recommended  

---

## Built With

Python  
PyTorch  
Hugging Face Transformers  
Unsloth  
LoRA (PEFT)  
ERNIE-4.5  
Hugging Face Datasets  
BitsAndBytes  
Google Colab  

---

## Team

Team Name: Butterfly Effect  
Members:  
Madhava Sriram  
Dhruv Meena  
Hardik Gohil
