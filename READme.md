# Single-Step Retrosynthesis Prediction

## Description

This project focuses on developing methods for single-step retrosynthesis prediction in chemical reactions. Given a dataset of chemical reactions in the format "[Reactants' SMILES]>>[Products' SMILES]", the goal is to train a machine learning model that can predict the reactants' SMILES starting from a new product SMILES.

## Project Overview

The project uses a BART (Bidirectional and Auto-Regressive Transformers) model for the task of retrosynthesis prediction. Here's a brief overview of the main components:

1. Data Preparation: The input data is processed to separate reactants and products from the SMILES notation.
2. Model: A pre-trained BART model is used and fine-tuned on the chemical reaction data.
3. Training: The model is trained to predict reactants given products.
4. Evaluation: The model's performance is evaluated on a validation set.
5. Prediction: The trained model is used to predict reactants for new product SMILES.

## Requirements

- Python 3.10+
- PyTorch
- Transformers
- Pandas
- Accelerate

You can install the required packages using:
