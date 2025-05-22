# Robust EEG Signal Classification for Motor Imagery Tasks in BCI

This project implements and evaluates three deep learning architectures — EEGNet, DeepConvNet, and ShallowConvNet — to classify EEG signals for motor imagery tasks using the BCI Competition IV Dataset IIa. These models aim to improve classification accuracy and robustness against signal artifacts and session-based variability.

## 🧠 Project Overview

Motor Imagery-based Brain-Computer Interfaces (MI-BCIs) rely on EEG signal decoding to enable control systems for rehabilitation and assistive technologies. This project explores three convolutional neural network architectures for binary classification between various motor imagery classes: left hand, right hand, foot, and tongue.

## 📊 Dataset: BCI Competition IV Dataset IIa

- **Subjects:** 9
- **Classes:** Left Hand, Right Hand, Foot, Tongue
- **Channels:** 22 EEG channels
- **Sampling Rate:** 250 Hz
- **Time Window Used:** 0s–4s (per trial)
- **Trials per Binary Task per Subject:** 24
- **Total Binary Classification Tasks:** 6 (e.g., LH vs RH, LH vs Foot, etc.)
- **Total Trials:** 1296

## 🔍 Binary Classification Tasks

The following 6 binary motor imagery tasks were created:

1. Left Hand vs Right Hand
2. Left Hand vs Foot
3. Left Hand vs Tongue
4. Right Hand vs Foot
5. Right Hand vs Tongue
6. Foot vs Tongue

Each classification is evaluated separately across all 9 subjects.

## ⚙️ Models Implemented

### EEGNet
A compact CNN tailored for EEG data. Achieved best validation accuracy of **90.2%** in LH vs Tongue task.

### DeepConvNet
A deeper CNN architecture for hierarchical feature extraction. Achieved **91.92%** in LH vs Tongue task — highest among all.

### ShallowConvNet
Focuses on spectral and temporal features. Achieved strong performance at **90.0%** for LH vs Tongue.

## 🧪 Evaluation Methodology

- Data normalized using StandardScaler.
- Tensor shape: (samples, channels, time).
- Split: 75% training, 25% testing.
- Evaluated per-subject to assess generalizability.
- Metrics: Accuracy, Precision, Recall, Confusion Matrix

## 📈 Results Summary

| Model            | Avg Accuracy (%) |
|------------------|------------------|
| DeepConvNet      | 89.35            |
| EEGNet           | 89.16            |
| ShallowConvNet   | 88.96            |
| Baseline (RoCSP) | 86.68            |

## 🚀 How to Run
Open any of the notebooks in the `notebooks/` directory to train and evaluate.

## 📝 Citation

Dataset from BCI Competition IV — Dataset IIa.

## 📬 Contact

For questions, reach out to [abhireddy2748@gmail.com](mailto:abhireddy2748@gmail.com).
