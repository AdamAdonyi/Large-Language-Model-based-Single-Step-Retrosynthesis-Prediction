# Single-Step Retrosynthesis Prediction

<img src="https://github.com/AdamAdonyi/Single-Step-Retrosynthesis-Prediction/blob/main/retro_picture.png">


## Description

This project focuses on developing methods for single-step retrosynthesis prediction in chemical reactions. Given a dataset of chemical reactions in the format "[Reactants' SMILES]>>[Products' SMILES]", the goal is to train a machine learning model that can predict the reactants' SMILES starting from a new product SMILES.

## Project Overview

The project uses a [BART](https://huggingface.co/facebook/bart-large) (transformer encoder-decoder (seq2seq) model with a bidirectional (BERT-like) encoder and an autoregressive (GPT-like) decoder) model for the task of retrosynthesis prediction. Originally, it was release in [2019](https://arxiv.org/abs/1910.13461) and trained on English language. Here's a brief overview of the main components

1. Data Preparation: The input data is processed to separate reactants and products from the SMILES notation.
2. Model: A pre-trained BART model is used and fine-tuned on the chemical reaction data.
3. Training: The model is trained to predict reactants given products. (only 3 epochs)
4. Evaluation: The model's performance is evaluated on a validation set.
5. Prediction: The trained model is used to predict reactants for new product SMILES.


## Usage

1. Prepare your data in a CSV format with reactions in the form "[Reactants' SMILES]>>[Products' SMILES]".
2. Run the data preparation script to process the input data.
3. Train the model using the training script.
4. Use the trained model to make predictions on new product SMILES.
   Since the prediction was a hard job for the public GPU (kaggle, colab) I cut the dataset into 3 parts to be able run the process without any kind of problem.


## Model

The project uses a [BART](https://huggingface.co/facebook/bart-large) (Bidirectional and Auto-Regressive Transformers) model from the Hugging Face Transformers library. The model is fine-tuned on the chemical reaction data to learn the mapping from products to reactants. To be able to use the model you need a wandb.ai profile and a generated key which is free and easy to use. After the first run, the given error message guide you to the homepage in case of lack of the key.


## Further resources to explore the topic:
[reaction_prediction_seq2seq](https://github.com/pandegroup/reaction_prediction_seq2seq)


## Evaluation

The model's performance is evaluated using metrics such as validation loss. You can find the evaluation results in the training output.

