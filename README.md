# English to Arabic Translation Using Seq2Seq LSTM  

This repository contains a sequence-to-sequence (Seq2Seq) model built using Long Short-Term Memory (LSTM) networks for translating English text into Arabic. The model was trained using a dataset obtained from [ManyThings.org](https://www.manythings.org/anki/), specifically the Arabic-English dataset (ara-eng.zip). 

![_31643cd0-3852-4910-92e6-d3ce17ffeb59](https://github.com/user-attachments/assets/e4da4f27-7fa1-4045-88e2-52b281219ffa)


## Table of Contents  

- [Dataset](#dataset)  
- [Preprocessing](#preprocessing)  
- [Model Architecture](#model-architecture)  
- [Training](#training)  
- [Results](#results)  
- [Usage](#usage)  
- [Contributing](#contributing)  
- [Acknowledgements](#acknowledgements)  

## Dataset  

The dataset used for training consists of:  
- **Number of samples**: 10,000  
- **Number of unique input tokens**: 38  
- **Number of unique output tokens**: 74  
- **Max sequence length for inputs**: 35  
- **Max sequence length for outputs**: 53  

The dataset includes paired sentences in English and Arabic, allowing the model to learn the mapping between the two languages.  

<img src="https://github.com/user-attachments/assets/124da8d3-5c47-4e42-a57d-3f4926a0de7a" alt="image" width="980" height="260" />

## Preprocessing  

Before training the model, several text-cleaning methods were applied to the dataset:  

1. **Remove Punctuation**: All punctuation marks were removed to clean the text.  
2. **Convert to Lowercase**: The text was converted to lowercase for uniformity.  
3. **Remove Diacritics (Tashkeel)**: Diacritics were removed to simplify the Arabic text.  

## Model Architecture  

The model is structured as follows:  

- **Encoder**: Processes the input sequence and returns the internal state.  
- **Decoder**: Generates the output sequence based on the encoded state.  

Here is the summary of the model architecture:  

![image](https://github.com/user-attachments/assets/1ea6e602-f796-4fd3-84d6-be66934bc413)

## Training

The model was trained for **10 epochs**, achieving a validation accuracy of **67%**. The training process involved feeding the cleaned dataset into the model and optimizing the weights using an appropriate loss function and optimizer.

## Results

The model achieved a validation accuracy of **67%** after training for 10 epochs.

## Usage

To use the trained model for translation, load the model and provide an English input text. The decoder will generate the corresponding Arabic translation based on the learned state of the model.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (git checkout -b feature-branch).
3. Commit your changes (git commit -m 'Add new feature').
4. Push to the branch (git push origin feature-branch).
5. Open a pull request.

## Acknowledgements

- ManyThings.org for providing the Arabic-English dataset.
- Keras and TensorFlow for building the deep learning model.
- The contributors for this project.

