# Are Large Language Models Ready for Healthcare? A Comparative Study on Clinical Language Understanding
This repository contains code for our MLHC 2023 paper [Are Large Language Models Ready for Healthcare? A Comparative Study on Clinical Language Understanding](https://arxiv.org/abs/2304.05368)

## Datasets
All datasets used for experiments can be downloaded in §Blue[/datasets] folder. They include:
| Task | Dataset | Output | Metric |
|------|---------|--------|--------|
| Named Entity Recognition | NCBI-Disease, BC5CDR-Chemical | BIO tagging for diseases and chemicals | Micro F1 |
| Relation Extraction | i2b2 2010-Relation, SemEval 2013-DDI | Relations between entities | Micro F1, Macro F1 |
| Semantic Textual Similarity | BIOSSES | Similarity scores from 0 (different) to 4 (identical) | Pearson Correlation |
| Natural Language Inference | MedNLI | Entailment, neutral, contradiction | Accuracy |
| Document Classification | i2b2 2006-Smoking | Current smoker, past smoker, smoker, non-smoker, unknown | Micro F1 |
| Question-Answering | bioASQ 10b-Factoid | Factoid answers | Mean Reciprocal Rank, Lenient Accuracy |

## Experimental Results
Representative results of each dataset can be found in §Blue[/results] folder. 
For each .csv file, they include the following rows from left to right:
- text: input text for model
- gold label: ground truth answer
- standard prompting input: input text with standard prompting (SP)
- BARD_0/5_SP_pred: 0/5-shot learning prediction result with Bard using SP
- GPT4_0/5_SP_pred: 0/5-shot learning prediction result with GPT4 using SP
- GPT3.5_0/5_SP_pred: 0/5-shot learning prediction result with GPT3.5 using SP
- CoT prompting input: input text with chain-of-thought prompting (CoTP)
- BARD_0/5_CoTP_pred: 0/5-shot learning prediction result with Bard using CoTP
- GPT4_0/5_CoTP_pred: 0/5-shot learning prediction result with GPT4 using CoTP
- GPT3.5_0/5_CoTP_pred: 0/5-shot learning prediction result with GPT3.5 using CoTP
- SQ prompting input: input text with self-questioning prompting (SQP)
- BARD_0/5_SQP_pred: 0/5-shot learning prediction result with Bard using SQP
- GPT4_0/5_SQP_pred: 0/5-shot learning prediction result with GPT4 using SQP
- GPT3.5_0/5_SQP_pred: 0/5-shot learning prediction result with GPT3.5 using SQP
