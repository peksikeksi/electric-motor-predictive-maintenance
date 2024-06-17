# Electric Motor Preventive Maintenance Project
Welcome to my electric motor preventive maintenance project! This repository contains code and resources for an electric motor preventive maintenance project, focusing on acoustic analysis of electric engine operational states using machine learning techniques.

## Dataset Overview

This information was taken from the original dataset page on kaggle [1, 2]. The IDMT-ISA-ELECTRIC-ENGINE dataset contains sound files of three similar units of an electrical engine (2ACT Motor Brushless DC 42BLF01, 4000 RPM, 24VDC), simulating different acoustic conditions. The operational states "good", "heavy load", and "broken" were provoked by changes in supply voltage and loading weight, leading to variations in operating sounds.
* File duration: 42.32 minutes
* Operational State "good": 774 files
* Operational State "broken": 789 files
* Operational State "heavy load": 815 files
* Total WAV Files: 2378
* Sampling rate: 44.1 KHz
* Resolution: 32-bit
* Mono audio

Credit: Authors Sascha Grollmisch, Jakob Abeßer, Judith Liebetrau, Hanna Lukashevich (Fraunhofer IDMT)

## Project Overview
### Approaches Used:
1. RNN LSTM with Waveform Data:
   * Initial approach using RNN LSTM with waveform data.
   * Performance outcome: Accuracy on the test set around 41%

2. Custom CNN with Spectrogram Data:
   * Created a custom CNN model using spectrogram data.
   * High-performance outcome: Accuracy on the test set equal to 100%
  
3. Transfer Learning with EfficientNetB4:
   * Used transfer learning with EfficientNetB4 trained on the ImageNet dataset.
   * Additional data preparation step: Oringinal model was trained on three channels (RGB), while spectrogram has only one channel.
   * Performance outcome: Accuracy on the test set around 98%

Note: Spectrgram-based approach yielded the best results for this case.

## Future Developement
* Experiment with different strategies (augmentation, regularization...) in order to improve the waveform-based approach.
* Try a feature extraction approach
* Experiment with combined/ensemble methods

## References and Cool Links

[1] [Electrical motor Sound Data](https://www.kaggle.com/datasets/pythonafroz/electrical-motor-operational-state-sound-data/data)

[2] Sascha Grollmisch, Jakob Abeßer, Judith Liebetrau, Hanna Lukashevich "Sounding Industry: Challenges and Datasets for Industrial Sound Analysis", Proceedings of the 27th European Signal Processing Conference (EUSIPCO), A Coruña, Spain, 2019.

[3] [Audio Classification (CNN)](https://github.com/jeffprosise/Deep-Learning/blob/master/Audio%20Classification%20(CNN).ipynb)

[4] [CNNs for Audio Classification](https://towardsdatascience.com/cnns-for-audio-classification-6244954665ab)

[5] [What is RNN (Recurrent Neural Network)?](https://aws.amazon.com/what-is/recurrent-neural-network/#:~:text=A%20recurrent%20neural%20network%20(RNN,complex%20semantics%20and%20syntax%20rules. )

[6] [Introduction to Recurrent Neural Network](https://www.geeksforgeeks.org/introduction-to-recurrent-neural-network/)
