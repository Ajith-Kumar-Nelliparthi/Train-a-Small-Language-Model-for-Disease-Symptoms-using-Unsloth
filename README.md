# Train a Small Language Model for Disease Symptoms using Unsloth

This project demonstrates how to fine-tune the [microsoft/phi-2](https://huggingface.co/microsoft/phi-2) language model using the [Unsloth](https://github.com/unslothai/unsloth) library for the task of mapping disease names and symptoms to diagnosis codes and suggested treatments.

## Features

- Loads and formats a disease symptoms dataset ([QuyenAnhDE/Diseases_Symptoms](https://huggingface.co/datasets/QuyenAnhDE/Diseases_Symptoms))
- Fine-tunes Phi-2 using LoRA adapters with Unsloth for efficient training
- Merges LoRA weights into the base model for easy deployment
- Compares outputs of the original and fine-tuned models

## Usage

1. **Install dependencies**  
   The notebook installs all required libraries, including Unsloth, Transformers, Datasets, and others.

2. **Prepare the dataset**  
   The dataset is loaded and formatted into instruction-based prompts for training.

3. **Fine-tune the model**  
   The notebook fine-tunes Phi-2 using Unsloth's efficient training pipeline.

4. **Merge and save the model**  
   After training, LoRA weights are merged and the model is saved for inference.

5. **Inference and Evaluation**  
   The notebook demonstrates how to generate predictions using both the original and fine-tuned models.

## Example Prompt

```
### Instruction:
Given the disease name and its symptoms, provide the diagnosis code and suggested treatments.

### Input:
Name: Panic disorder
Symptoms: Palpitations, Sweating, Trembling, Shortness of breath, Fear of losing control, Dizziness

### Response:
Code: ICD-10-CM F41.1
Treatments: Cognitive-behavioral therapy, medication
```

## Files

- `finetuned_model.ipynb` — Main notebook for data preparation, training, and evaluation

## References

- [Unsloth GitHub](https://github.com/unslothai/unsloth)
- [Phi-2 Model Card](https://huggingface.co/microsoft/phi-2)
- [Datasets Library](https://huggingface.co/docs/datasets)