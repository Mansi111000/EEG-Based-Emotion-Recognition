# 🎭 EEG-Based Emotion Recognition

## 📑 Table of Contents
- [📌 Overview](#overview)
- [📂 Dataset Details](#dataset-details)
  - [📝 Online Ratings](#online-ratings)
  - [🧑‍🔬 Participant Ratings](#participant-ratings)
  - [📼 Video List](#video-list)
  - [📊 Participant Questionnaire](#participant-questionnaire)
- [⚙️ Data Preprocessing](#data-preprocessing)
- [🗂️ Dataset Structure](#dataset-structure)
- [🧠 Feature Extraction](#feature-extraction)
- [📈 Machine Learning Models](#machine-learning-models)
- [📊 Accuracy Results](#accuracy-results)
- [🚀 How to Use](#how-to-use)
- [🔮 Future Improvements](#future-improvements)
- [📧 Contact](#contact)

---

## 📌 Overview
This project investigates **EEG-based emotion recognition** using **video stimuli**, both with and without **olfactory enhancement**. The goal is to evaluate the **impact of scent on emotion induction** and **recognition accuracy**, improving affective human-computer interaction (HCI). 

### 🔍 Why is this Important?
- Enhancing **affective computing** to better understand human emotions.
- Improving **human-computer interaction** by incorporating brainwave data.
- Exploring **multisensory integration** to study the effect of smell in emotional experiences.

---

## 📂 Dataset Details
This study uses EEG data collected from an emotion recognition experiment where participants were exposed to video-based stimuli.

### 📝 Online Ratings
- Contains **emotional ratings** (Valence, Arousal, Dominance) provided by participants during an online study.
- Helps analyze the subjective emotional experience of participants.

### 🧑‍🔬 Participant Ratings
- **Trial-by-trial emotional responses** recorded from participants while watching specific videos.
- Essential for linking EEG signals to emotional states.

### 📼 Video List
- A comprehensive list of all **videos used in the self-assessment and experiment**.
- Helps in correlating emotional responses with specific video stimuli.

### 📊 Participant Questionnaire
- **Demographic information** and participant background details.
- Ensures diversity and reliability in data collection.

🔗 **Dataset Source**: *[Provide dataset link if applicable]*

---

## ⚙️ Data Preprocessing
To ensure data quality and improve model performance, several preprocessing steps were performed:

- 🔽 **Downsampling to 128Hz**: Reducing data size while preserving EEG frequency bands.
- 👀 **EOG Artifact Removal**: Eliminating eye movement noise for better signal clarity.
- 📶 **Bandpass Filtering (4-45 Hz)**: Keeping only emotion-related EEG wave frequencies.
- 🔄 **Common Reference Averaging**: Normalizing signals across participants for consistency.
- 🎯 **Trial Segmentation & Baseline Removal**: Ensuring data captures only emotion-induced responses.
- 🆔 **Reordering to Match Experiment ID**: Aligning dataset structure across participants.

---

## 🗂️ Dataset Structure
- **📊 Data Array (40x40x8064)**:
  - 40 trials per participant.
  - 40 EEG + physiological channels.
  - 8064 data points per trial (60 sec @ 128Hz).
- **🏷️ Labels (40x4)**:
  - Emotional dimensions: **Valence, Arousal, Dominance, Liking**.

---

## 🧠 Feature Extraction
### 🔬 EEG Features:
- **Power Bands**: Delta, Theta, Alpha, Beta, Gamma.
- **Differential Entropy (DE)**: Extracted from EEG signals.
- **Statistical Measures**: Mean, Variance, Skewness, Kurtosis.

### ❤️ Emotional Labels:
- **Collected from participant ratings** in the experiment.

### 📡 Physiological Data:
- **EOG and other biosignals** recorded before artifact removal.

### 📽️ Video Metadata:
- **Contextual data**, such as video valence, arousal, and dominance scores.

---

## 📈 Machine Learning Models
We implemented the following **machine learning models** to classify emotions based on EEG data:

- 🤖 **K-Nearest Neighbors (KNN)**
- 🏆 **Support Vector Machine (SVM)**
- 🌳 **Random Forest**
- 📊 **Decision Tree**

---

## 📊 Accuracy Results
| 🏆 Model | 🎯 Train Accuracy | 📊 Test Accuracy |
|--------|--------------|-------------|
| **KNN** | 71.6% / 72.9% | 60.0% / 58.6% |
| **SVM** | 98.5% / 99.1% | 55.9% / 55.9% |
| **Random Forest** | 58.3% / 100% | 55.3% / 62.5% |
| **Decision Tree** | 99.3% / 57.4% | 60.0% / 58.2% |

---

## 🚀 How to Use
Follow these steps to use the project:

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/Mansi111000/EEG-Based-Emotion-Recognition.git
   cd EEG-Based-Emotion-Recognition
   ```
2. **Run Preprocessing and Feature Extraction Scripts**.
3. **Train the models** using the provided Jupyter notebook or Python scripts.

---

## 🔮 Future Improvements
- 🤖 **Deep Learning Integration**: Implementing CNNs and LSTMs for better feature extraction.
- 🧠 **Real-Time EEG Processing**: Developing a real-time emotion recognition system.
- 🔗 **Multimodal Analysis**: Combining EEG data with facial expression or speech recognition.
- 📈 **Dataset Expansion**: Collecting more diverse data for better model generalization.

---

## 📧 Contact
For any queries, reach out via **GitHub Issues** or email.

🚀 **Happy Coding & Research!**
