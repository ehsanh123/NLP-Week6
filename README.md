# README - Week 6 NLP Class

## Introduction
This project is focused on training a machine translation model using an existing English-to-Spanish translator. Unlike word-to-word translation, this model performs sentence-to-sentence translation by leveraging deep learning techniques. The approach uses LSTMs (Long Short-Term Memory) within a sequence-to-sequence (Seq2Seq) architecture to enhance the accuracy of translations.

## Prerequisites
Before running the notebook, ensure you have the following dependencies installed:

```bash
pip install tensorflow keras numpy
```

Alternatively, if using Google Colab, install the required packages directly in the notebook.

## Dataset
The model requires a parallel dataset of English and Spanish sentences for training. If not provided in the notebook, you can download a dataset from:

- [ManyThings.org](https://www.manythings.org/anki/)

## Model Architecture
The translation model follows a sequence-to-sequence (Seq2Seq) structure:

1. **Preprocessing**: Tokenization, padding, and cleaning of input sentences.
2. **Encoder**: Uses an embedding layer and an LSTM to process the input sequence.
3. **Decoder**: Another LSTM that generates translated sentences.
4. **Training**: The model is trained using sparse categorical cross-entropy loss.
5. **Prediction**: Translated sentences are generated based on the trained model.

## Running the Notebook
1. Load the dataset and preprocess it.
2. Define and train the sequence-to-sequence LSTM model.
3. Use the trained model to translate English sentences into Spanish.

## Example Usage
After training, you can test the translation model with:

```python
english_text = "How are you?"
predicted_translation = translate(english_text)
print("Spanish:", predicted_translation)
```

## Limitations and Future Improvements
- The model requires a significant amount of training data for optimal performance.
- Further improvements can be made using transformer-based models like BERT or MarianMT.

This project provides a foundation for building more advanced NLP-based translation systems.

