# Neural Decoding for Motor Intent

This repository contains an ongoing project exploring neural decoding of motor intent using the PhysioNet Motor Imagery/Movement dataset. The focus of the project is to classify motor intent, specifically distinguishing **left-hand movement** versus **rest**, using EEG data. The project experiments with various approaches to evaluate and improve decoding performance.

---

## Dataset

The experiments utilize the **PhysioNet Motor Imagery/Movement dataset**, which provides EEG recordings from multiple channels during motor imagery and movement tasks. 

For this project:
- Only **8 frontal channels** were used to interpret the task as a cognitive decoding problem.
- A preliminary analysis was also conducted with the full **64-channel** dataset for comparison.

---

## Approaches

The project explores the following approaches:

1. **64-Channel EEGNet**  
   - Implements the EEGNetv4 architecture using the full 64-channel dataset.  
   - The architecture is adapted from the [Braindecode](https://github.com/braindecode/braindecode) implementation.  

2. **8-Channel EEGNet**  
   - Applies the same EEGNetv4 architecture, but only with 8 frontal channels.  
   - Aims to assess the performance of cognitive decoding with reduced spatial information.  

3. **Short-Time Fourier Transform (STFT) + LSTM**  
   - Uses STFT to extract time-frequency features.  
   - Processes the features through an LSTM-based network for decoding.  

4. **EEGNet + LSTM**  
   - Combines EEGNet's convolutional feature extraction with an LSTM layer for temporal decoding.  

---

## Goals

This repository serves as a record of experimentation and ongoing efforts to improve neural decoding approaches. The primary objectives are to:
- Evaluate decoding performance under different architectural constraints.
- Assess the impact of using reduced spatial information (frontal 8 channels).  
- Explore hybrid models (e.g., CNN + LSTM) for decoding temporal and spatial EEG patterns.

---

## How to Use

1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   pip install -r requirements.txt
   run jupyter notebook
