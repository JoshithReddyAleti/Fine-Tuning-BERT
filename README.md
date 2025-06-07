# Fine-Tuning-BERT
# BERT Project with Hugging Face  
**Authored by Joshith Reddy**

## Overview  
This repository contains a Jupyter notebook that walks through:

1. **Fine-tuning** BERT for sentiment analysis (IMDb)  
2. **Debugging** common training issues  
3. **Evaluating** with Accuracy, F1, Log Loss, Exact Match, and MSE  
4. **Creative application**: Named Entity Recognition (CoNLL-2003)

## Prerequisites  
- Python 3.8 or higher  
- Git  
- A Hugging Face account (for model downloads)

## Setup

1. **Clone** this repository  
2. **Enter** the project folder  
3. **Create & activate** a virtual environment  
   - Windows (PowerShell):  
     ```
     python -m venv venv  
     .\venv\Scripts\Activate.ps1

     ```  
4. **Install** dependencies  

pip install transformers datasets torch scikit-learn evaluate scipy seqeval python-dotenv

5. **Configure** your Hugging Face token  
- Create a file named `.env` at the project root containing:  
  ```
  HF_TOKEN=hf_your_api_token_here
  ```

## Usage

1. **Launch** JupyterLab or Jupyter Notebook:  

jupyter notebook Fine-Tuning-BERT.ipynb

2. **Run** each cell in order. Key sections:  
- **Part 1**: IMDb fine-tuning  
- **Part 2**: Debugging guidance  
- **Part 3**: Extended evaluation metrics  
- **Part 4**: Named Entity Recognition

3. **Inspect** outputs and logs:  
- Model checkpoints saved under `./results` and `./results-ner`  
- Final models in `./bert-finetuned-*` and `./distilbert-finetuned-*`

## Directory Structure

- `BERT_Project_Extended.ipynb` – the main notebook  
- `results/` – classification checkpoints and logs  
- `results-ner/` – NER checkpoints and logs  
- `bert-finetuned-imdb/`, `distilbert-finetuned-imdb/`, `bert-regression-stsb/` – saved models  
- `.env` – your Hugging Face token (excluded from Git)

## Metrics

- **Classification**: Accuracy, F1, Log Loss  
- **Question Answering**: Exact Match, F1  
- **Regression**: Mean Squared Error  
- **NER**: Precision, Recall, F1, Token Accuracy via Seqeval  

## Next Steps

- Experiment with other Hugging Face models (RoBERTa, ALBERT)  
- Integrate data augmentation or domain-specific pretraining  
- Deploy the fine-tuned model via a simple API (FastAPI, Flask)
