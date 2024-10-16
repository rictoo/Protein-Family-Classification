# Protein Family Classification of Amino Acid Sequences

A deep learning-based approach to classify amino acid sequences into protein families, utilising both Bidirectional LSTM and Transformer architectures, with a focus on the PFam dataset.

## Dataset Overview

The dataset in question comprised approximately 1 million amino acid sequences, each labelled with a specific protein class. In our analysis of the training data, we observed that the median sequence length stands at 119.0 amino acids. The labels in the training data encompassed 17,929 unique protein family classes.

## Model Overview

The challenge was framed as a sequence classification problem, leading to the use of both a bidirectional LSTM and a Transformer architecture. In this experiment, the Bidirectional LSTM model, with an accuracy of 95.81% on the test set, surpassed the Transformer model, which achieved an accuracy of 86.63% on the test set. This variance might be attributed to suboptimal hyperparameters in the Transformer model. Adjusting the number of attention heads, altering the learning rate, or modifying the dropout could potentially increase its performance.

## Repository Structure

- `src`: Contains the Jupyter notebook detailing the experiments and findings.
- `models`: Contains the trained tokeniser, LSTM and Transformer models.
- `data`: The `data/unprocessed` directory is initially empty. To run the experiments, it expects the extracted PFam dataset from [this link](https://www.kaggle.com/datasets/googleai/pfam-seed-random-split). After downloading and extracting the dataset, place the `train`, `dev`, and `test` directories directly into the `data/unprocessed` directory.
