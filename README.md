# Project_Bird-Song-Classifier-with-Machine-Learning

Refer to the project page on my website for detailed discussion on the project, including steps performed to process and clean the dataset and model reults evaluation.

Project page: https://rachlllg.github.io/project/2023-Bird_Song_Classifier_with_Machine_Learning/

## Background:
This was the final project for the Applied Machine Learning class in my Masters in Data Science program. The original project involved four team members including myself, for the showcase/repo here, I have only presented the work I have done, unless noted otherwise.

The project was very open-ended, the teams are free to select any topic of interest and any dataset pertaining to that topic, with the objective to build a machine learning model.

All work was done in Google Colab (Free), with Python as the programming language. For training the deep neural networks (FFNN, CNN, and RNN), GPU is recommended to speed-up the processing time. Notable Python packages used:
- standard: numpy, pandas
- audio processing: librosa
- modeling: scikit-learn, tensorflow
- visualization: matplotlib, seaborn

## Dataset:
The dataset was sourced from the BirdCLEF 2023 kaggle competition hosted by the Cornell Lab of Ornithology.

Source: <https://www.kaggle.com/competitions/birdclef-2023/overview>

The primary feature is short recordings of individual bird calls for 264 different bird species. The audio recordings were sourced from <https://xenocanto.org> and all audio files were downsampled to 32 kHz where applicable and stored in the ogg format. Supplemental features include secondary bird species, call type, location, auality rating, and taxonomy. The original dataset could be downloaded from the competition page after user sign-in and agree to the competition rules. 

For the purpose of this project, only 3 bird species were selected (primarily due to limitation in computing resource). The 3 selected species are barswa, comsan, and eaywag1. As the test data provided by the competition lacked labels, and only 3 out of the 264 species from the original dataset were selected, I utilized only the training dataset as provided by the competition for this project. To prevent data leakage, the data was split to train and test dataset at 70/30 split (at random). A series of preprocessing and data cleaning were performed before EDA and model building, details of which can be found on the project page. 

## Model:
Many audio features could be extracted from audio files, some commonly used for machine learning are MFCC, mel-spectrogram, spectral centroid, chroma, and RMS. I explored and experimented different features and with different feature engineering techniques, and then built various models with different combinations of audio features as input using below listed machine learning algorithms, with sequential and functional API architectures, with and without augmentation, with and without learned embeddings, and with and without transfer learning techniques. Details of feature extraction, feature engineering, and model results can be found on the project page. 
- Ensemble: Random Forest, XGBoost
- Support Vector Machine (SVM)
- Logistic Regression
- Feed Forward Neural Network (FFNN)
- Convolutional Neural Networks (CNN): 1D & 2D
- Recurrent Neural Networks (RNN): LSTM & GRU