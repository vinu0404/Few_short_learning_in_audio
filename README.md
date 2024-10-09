# Few-Shot Language Agnostic Keyword Spotting (FSLAKWS) 

This project is designed to detect the presence of multiple specific keywords within audio files using advanced spectrogram analysis and Siamese neural networks. The system preprocesses audio data, removes noise, and utilizes few-shot learning for efficient training with limited examples.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Code Components](#codecomponents)
- [Future Scope](#futurescope)

## Overview
The Multi-Keyword Audio Recognition System aims to identify specific keywords within audio recordings. The project processes audio files by converting them into spectrograms, applying noise filters, and using a Siamese neural network to identify keywords through similarity measures. The system supports training with minimal examples using few-shot learning techniques.

## Features
- **Noise Filtering**: Reduces noise in audio files for better keyword detection.
- **Spectrogram Analysis**: Converts audio files into mel spectrograms for visual analysis.
- **Few-Shot Learning**: Efficiently trains the model with limited examples.
- **Siamese Neural Network**: Leverages similarity-based learning to detect multiple keywords.

## CodeComponents

1. **Audio Preprocessing**
   - **Functions**:
     - `audio_to_spectrogram`: Converts audio files into mel spectrograms.
     - `remove_noise`: Applies noise reduction techniques to the audio files.

2. **Data Preparation**
   - **Function**:
     - `load_data`: Loads spectrogram images and their corresponding labels from a specified directory.   [DATASET](https://drive.google.com/drive/folders/1Y6SYXwg-A-OqZSRpr_jeox5MkuGqZ7mN?usp=sharing)
     - `create_pairs`: Generates pairs of spectrograms for training the Siamese network, including positive and negative pairs.

3. **Model Architecture**
   - **Siamese Network**:
     - **Function**:
       - `create_base_network`: Defines the base CNN model architecture for feature extraction.
       - `build_siamese_model`: Constructs the Siamese network that compares two spectrograms to determine similarity.

4. **Training and Saving the Model**
   - **Function**:
     - `train_model`: Compiles the model, trains it on the prepared pairs of spectrograms, and saves the trained model.

5. **Prediction**
   - **Script**:
     - `predict.py`: Uses the trained model to predict whether an audio file contains specific keywords based on its spectrogram representation.

### Project Flow
1. Audio files are processed and converted into spectrograms.
2. Spectrograms are loaded, and training pairs are created.
3. A Siamese network is trained on these pairs to recognize keywords.
4. The trained model is saved for future predictions.
5. New audio files can be inputted to determine if they contain specific keywords.

### Dependencies
- `numpy`
- `opencv-python`
- `librosa`
- `tensorflow`
- `sklearn`

## FutureScope

The Few-Shot Language Agnostic Keyword Spotting (FSLAKWS) project has significant potential for future enhancements, including:

1. **Increase Model Accuracy**:
   - Will Increase model accuracy as this model has low accuracy due to low availibilty of data.

2. **Expanded Keyword Database**: 
   - Integrate a broader range of keywords and phrases to improve versatility and adaptability in various applications.

3. **Multi-Language Support**: 
   - Enhance the model's capability to recognize keywords in multiple languages, making it more globally applicable.

4. **Real-Time Processing**: 
   - Optimize the model for real-time audio processing, enabling immediate keyword detection in live environments.
