# SPEECH-EMOTION-DETECTION-USING-CNN-AND-LSTM
🎙️ Speech Emotion Recognition using CNN and LSTM
📘 Overview

This project implements a Speech Emotion Recognition (SER) system using Convolutional Neural Networks (CNNs) and Long Short-Term Memory (LSTM) networks to detect human emotions from speech.
The model is trained on the RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song) dataset, which contains 7356 labeled audio files of professional actors expressing different emotions.

👨‍💻 Team

Team 1 — CST461 Deep Learning

Nihar Jani

Parth Oza

Tochukwu Ezekwere

🧠 Abstract

The goal of this project is to classify human emotions such as happy, sad, angry, and neutral from speech audio.
By combining the spatial feature extraction power of CNNs with the temporal modeling capabilities of LSTMs, this project aims to create a robust and efficient model for emotion recognition, with potential applications in:

Human-Computer Interaction

Mental Health Monitoring

Customer Service Enhancement

Emotion-Aware AI Systems

📂 Dataset

Dataset: RAVDESS: Ryerson Audio-Visual Database of Emotional Speech and Song

Emotions Included:

Neutral

Calm

Happy

Sad

Angry

Fearful

Disgust

Surprised

For this project, we focused on four emotions: Angry, Sad, Neutral, and Happy.

⚙️ Methodology
🧩 1. Data Preprocessing

Feature Extraction: Using the librosa library to compute:

Mel-Frequency Cepstral Coefficients (MFCC)

Chroma features

Mel Spectrogram

Spectral Contrast

Tonnetz

Data Splitting: 75% training / 25% testing

Augmentation: Noise injection, pitch shifting, and time stretching to increase dataset diversity.

🧱 2. Model Architectures
🌀 CNN Model

Conv Layer 1: 128 filters, kernel size 5, ReLU + MaxPooling + Dropout

Conv Layer 2: 128 filters, kernel size 5, ReLU

Flatten + Dense Layer: Fully connected with Softmax activation for 8 emotion classes

Optimizer: RMSProp (lr=0.00005)

Loss: Sparse categorical cross-entropy

Epochs: 500, Batch size: 20

🔁 LSTM Model

Input: MFCC feature arrays reshaped for sequential input

Layers:

LSTM layers for temporal learning

Dense layers for classification

Batch Normalization + Dropout for stability

Optimizer: Adam

Loss: Categorical cross-entropy

Metrics: Accuracy, F1-score, Confusion Matrix

📊 Results
Model	Accuracy	Remarks
CNN	High accuracy on 4-class subset	Good feature learning from spectral data
LSTM	Strong temporal performance	Captures sequential emotion patterns
💬 Discussion

The models successfully classify key emotions with high accuracy using extracted spectral and temporal features.

Limitations include:

Restricted emotion set (4 emotions)

Limited cultural generalization

Potential privacy concerns in real-world use

🚀 Future Work

Expand to full 8 emotions from RAVDESS

Add multi-modal analysis (facial expressions + voice)

Implement real-time emotion recognition

Explore transfer learning and explainable AI techniques

🧰 Technologies Used

Python 3

TensorFlow / Keras

Librosa

Scikit-learn

NumPy, Pandas, Matplotlib

📁 Project Files

Speech Emotion Recognition using CNN.ipynb — CNN model implementation

SpeechEmotionRecognition_model_LSTM.ipynb — LSTM model implementation

FINAL_TEAM1.pdf — Full project report

📚 References

Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)

McFee, B. et al. (2015). librosa: Audio and Music Signal Analysis in Python.

Chollet, F. et al. (2015). Keras Library — GitHub

Pedregosa, F. et al. (2011). Scikit-learn: Machine Learning in Python.

Internal Notebooks: Speech Emotion Recognition using CNN and LSTM Models

🧑‍⚕️ Applications

Mental health monitoring systems

Sentiment analysis

Voice assistants and chatbots

Customer support call analysis

📸 Sample Visualization

Spectrogram and MFCC feature maps are generated to visualize emotion-specific patterns in audio data.

🏁 Conclusion

The combination of CNN and LSTM architectures delivers strong results in emotion classification from speech signals.
This project demonstrates the potential for emotion-aware systems that can understand human feelings and respond empathetically.
