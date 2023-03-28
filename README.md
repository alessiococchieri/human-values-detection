# Human Values Detection Behind Arguments
In the current work, we are tackling Task 4 of the Touché Competition: [Human Value Detection 2023](https://touche.webis.de/semeval23/touche23-web/index.html)
## Task
The task consits of a **multilabel text classification**. Given a textual argument and a human value category, classify whether or not the argument draws on that category.

Arguments are given as a triplet: 
- **Conclusion**: Conclusion text of the argument
- **Stance**: Stance of the Premise towards the Conclusion; one of "in favor of", "against"
- **Premise**: Premise text of the argument

## Data 
We are using the data available on [Zenodo](https://zenodo.org/record/7550385#.Y8wMquzMK3I).
We are referring only to the following data: `arguments-training.tsv`, `arguments-validation`, `labels-training.tsv`, `labels-validation.tsv`


***NOTE***: *Since test data is provided without labels, we did not consider it for our analysis. In this regards **the performances of the tested models have been evaluated only on the validation data**.*


## Tested models
- SVM
- BERT-base
- BERT-large
- RoBERTa-base
- RoBERTa-large
- DistilBERT
- XLNet-base
- XLNet-large

## Results
Compared to the [original paper](https://aclanthology.org/2022.acl-long.306.pdf), the macro-averaged F1 Score has been improved: 
- **by more 20%** for the SVM model
- **up to 47%** for transformers

| MODEL               | SVM  | BERT-base | BERT-large | DistilBERT | RoBERTa-base | RoBERTa-large | XLNet-base | XLNet-large |   
|:-------------------:|:----:|:---------:|:----------:|:----------:|:------------:|:-------------:|:----------:|:-----------:|
| F1 avg macro (validation) | 0.37 | 0.42      | 0.44       | 0.43       | 0.47         | 0.50          | 0.44       | 0.50        |   

