# BaciCausalLM

This repository provides the supplementary materials and the pretrained language model associated with the corresponding research article.

## Supplementary Materials

The following supplementary tables are referenced in the paper:

- **Table S1**: Supplementary material described in the article  
- **Table S2**: Supplementary material described in the article  
- **Table S3**: Supplementary material described in the article  
- **Table S4**: Supplementary material described in the article  
- **Table S5**: Supplementary material described in the article  

These tables contain additional experimental details and results that support the main findings of the study.

## Pretrained Model

The trained model used in this work is publicly available on Hugging Face:

- **Model name**: BaciCausalLM  
- **Model link**: https://huggingface.co/BillyLiang/BaciCausalLM

The model can be loaded using the Hugging Face `transformers` library.

### Example Usage

```python
from transformers import AutoTokenizer, AutoModelForCausalLM

tokenizer = AutoTokenizer.from_pretrained("BillyLiang/BaciCausalLM")
model = AutoModelForCausalLM.from_pretrained("BillyLiang/BaciCausalLM")

inputs = tokenizer("Your input text here.", return_tensors="pt")
outputs = model.generate(**inputs)
print(tokenizer.decode(outputs[0], skip_special_tokens=True))
