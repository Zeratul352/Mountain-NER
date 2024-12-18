# Mountain NER
 Notebook for training NER model

# Installation
1. Download the notebook
2. Install all requirements
3. Download dataset from https://www.kaggle.com/datasets/geraygench/mountain-ner-dataset/data
4. Specify path to dataset
5. Now you can train your own model!

# How to use
1. Download model from https://drive.google.com/file/d/1p3mCrL0uF45ki1Rsafdf4fTYbPbmA2b8/view?usp=sharing
2. Specify path to model
3. Launch next code:

from transformers import pipeline

model_checkpoint = "D:/models/roberta-base"
token_classifier = pipeline(
     "token-classification", model=model_checkpoint, aggregation_strategy="simple"
)
print(token_classifier("Alps are one of the most beautiful places in Europe"))
