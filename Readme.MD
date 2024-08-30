# Sequence-to-Sequence RNN for Sentence Transformation

This project implements a Sequence-to-Sequence (Seq2Seq) model using Recurrent Neural Networks (RNN) in Keras to learn and transform input sequences to output sequences. The project uses an encoder-decoder architecture, trained on character-level sequence data, to map an input string to its transformed version.

## Project Overview

The main task of this project is to predict an output string given an input string using a character-level Seq2Seq model. The model is trained using one-hot encoded vectors representing characters, where each character corresponds to an integer value. The Seq2Seq model utilizes a simple RNN for both the encoder and decoder components.

### Features
- The model maps each character to its corresponding index using one-hot encoding.
- The RNN-based encoder processes the input sequence and outputs a state vector that encapsulates information from the input.
- The decoder generates the transformed output sequence, one character at a time, using the encoder's state vector.
- The model is trained on provided dataset with input-output string pairs.

### Dataset
The training and evaluation datasets (`train_data.csv` and `eval_data.csv`) contain input and output sequences. These are character-level transformations, where each sequence consists of lowercase English letters.

### Key Components
- **Encoder**: Uses a SimpleRNN to process the input sequence and generate a state vector. This state is used by the decoder to generate the output sequence.
- **Decoder**: The decoder generates the output sequence one step at a time, conditioned on the state provided by the encoder.
- **Evaluation**: The performance of the model is evaluated based on how many characters match between the predicted and actual output sequence.

## Getting Started

### Prerequisites

The following libraries are required:
- Python 3.x
- TensorFlow/Keras
- NumPy
- Pandas
- Matplotlib

You can install the dependencies using pip:

```bash
pip install tensorflow keras numpy pandas matplotlib
