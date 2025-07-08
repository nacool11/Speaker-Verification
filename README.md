# Speaker Verification Project

## Overview

This project implements a speaker verification system using various machine learning models. The system processes audio files, extracts relevant features, and trains models to verify speaker identities.
![image](https://github.com/user-attachments/assets/91a3954e-81da-4172-a0a1-30b883f53947)


## Dataset Description

- **Number of Files:** 2,944 audio files from 25 speakers
- **Total Duration:** 24,330.3 seconds
- **Format:** `.wav` (Waveform Audio File Format)
- **Duration:** Varies, with an average of 8.26 seconds
- **Minimum Duration:** 3.96 seconds
- **Maximum Duration:** 69.04 seconds
- **Content:** Speech samples with different speeds and pitches
![image](https://github.com/user-attachments/assets/35489bf1-5c97-493d-b281-a83fa40c1d89)

## Data-Set Access Link:
[Link](https://drive.google.com/file/d/1zo6dYvZM9iH9-kKfQuDM-28isKdWVqbw/view?usp=sharing)

## Exploratory Data Analysis

1. **Audio Normalization:** Ensuring all audio files are sampled at 16 kHz for consistency.
2. **Segmentation:** Dividing audio files into 3-second and 8-second segments for uniformity.
3. **Padding:** Zero-padding shorter segments to match required lengths.
4. **Noise Reduction:** Band-pass filtering was used to reduce background noise.

## Feature Extraction

In addition to **MFCCs**, the following features were extracted to enhance model performance:

- **Chroma Features**
- **Spectral Contrast**
- **Spectral Centroid**
- **pMFCC**
- **Mel Spectrogram**
- **Pitch-related Features (e.g., pitches, pitch\_mean)**

## Models Implemented

- **Random Forest:** Ensemble learning method for improved performance.
- **K-Nearest Neighbors (KNN):** Utilized for proximity-based speaker classification.
- **Support Vector Machine (SVM):** Used for distance-based speaker comparison.
- **Gaussian Mixture Models (GMMs):** Each speaker was trained with a GMM model for log-likelihood scoring. Models were serialized in `.pkl` format for efficiency.

## Results

- **Seen Users:** Accuracy of **91%** achieved with GMM (n\_components = 64)
- ![image](https://github.com/user-attachments/assets/e2012e84-084a-4a90-91ee-da0a00126cf9)

- **Unseen Users:** Accuracy of **71.7%** achieved with GMM (n\_components = 64)
- ![image](https://github.com/user-attachments/assets/8ab869d6-3bb1-4abb-a5ee-2ac3a1654cf5)


## Challenges

- Variations in pitch, tone, and background noise introduced inconsistencies.
- Data imbalance caused training bias, reducing model performance.

## Conclusion

Traditional machine learning models yielded limited accuracy, emphasizing the need for advanced deep learning models or enhanced feature engineering to improve speaker verification outcomes.

## Tools & Libraries

- **Librosa**: Audio processing and feature extraction
- **Scikit-learn**: Model training and evaluation
- **Matplotlib**: Visualization
- **Pandas & Numpy**: Data manipulation and analysis
- **Scipy**: Scientific computing
- **Pickle**: Model saving and loading

## References

1. **Tim Sainburg's Noise Reduction Library:** [Link](https://doi.org/10.5281/zenodo.3243139)
2. **Speaker Recognition Using Machine Learning Techniques by Abhishek Manoj Sharma:** [Link](https://doi.org/10.31979/etd.fhhr-49pm)

## NOTE
[The given repository doesn't contain model.pkl file as it exceeds the limited memory upload i.e. > 25mb]
[Model Link](https://drive.google.com/file/d/1z9gmK3SE3m-EThRqLbY2JMKDItHEV4Vd/view?usp=sharing)

