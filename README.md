This repository implements a robust Speech Emotion Recognition (SER) system using deep learning. The system processes and integrates multiple datasets, applies data augmentation techniques, extracts meaningful features, and trains a neural network to classify audio signals into distinct emotional categories.

### Datasets

This project utilizes the following datasets:

- RAVDESS: A dataset containing emotional speech recordings labeled with numerical codes representing emotions.
- TESS: Includes emotional speech categorized based on filename conventions.
- SAVEE: Features emotional speech with labels encoded in file abbreviations.
The datasets are preprocessed to create a unified structure with emotion labels and corresponding file paths.

### Data Augmentation

To improve model generalization and robustness, the following augmentation techniques are applied:

- Adding Noise: Simulates real-world environmental noise to make the model robust.
- Time Stretching: Alters the duration of audio signals without changing their pitch to simulate speech tempo variations.
- Pitch Shifting: Modifies the pitch of audio to account for variations in speaker vocal characteristics.
Feature Extraction

The system uses Mel-Frequency Cepstral Coefficients (MFCCs) to extract meaningful features from the audio signals. Key steps include:

- Cropping and resampling audio to ensure consistent dimensions.
- Computing MFCCs with 13 coefficients to capture essential vocal features.
- Structuring the extracted features into a 2D array suitable for neural network input.
- Model Architecture

### The deep learning model is built using TensorFlow and consists of:

- LSTM Layers: Two Long Short-Term Memory (LSTM) layers with 128 and 64 units, respectively, to capture temporal features.
- Dense Layer: A fully connected layer with 64 neurons and ReLU activation for higher-level feature extraction.
- Dropout Regularization: A dropout layer with a 30% rate to reduce overfitting.
- Output Layer: A softmax activation layer to classify audio into seven emotional categories: neutral, happy, sad, angry, fear, disgust, and surprise.

### The code also invloves converting to tf-lite 
