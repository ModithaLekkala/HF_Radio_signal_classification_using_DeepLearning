# HF_Radio_signal_classification_using_DeepLearning

# Deep Learning for HF Radio Signal Type Classification

### Project Overview
The "Deep Learning for HF Radio Signal Type Classification" project focuses on developing and optimizing deep learning models to accurately classify high-frequency (HF) radio signals. The primary objective is to achieve high classification accuracy across different signal-to-noise ratio (SNR) conditions using advanced deep learning techniques.

### Dataset
- **Total Signals:** 172,800
- **IQ Samples per Signal:** 2,048
- **Channels:** 2 (I and Q)
- **Classes:** 18
- **Dataset Link:** https://panoradio-sdr.de/radio-signal-classification-dataset/

### Data Splits
- **Training Data:**
  - **X_train:** (144,000, 2,048, 2)
  - **Y_train:** (144,000, 18)
- **Testing Data:**
  - **X_test:** (28,800, 2,048, 2)
  - **Y_test:** (28,800, 18)

### Detailed Description
- **X_train/X_test:** Arrays containing the IQ data for training and testing, respectively. Each signal consists of 2,048 samples across two channels (I and Q).
- **Y_train/Y_test:** Arrays containing one-hot encoded labels for the signals, with each signal classified into one of 18 classes.

### Models and Techniques
- **Deep Convolutional Neural Network (Deep CNN):** Designed for feature extraction and classification of radio signals.
- **ResNet (Residual Network):** Utilizes residual connections to train very deep networks efficiently.
- **Genetic Neural Architecture Search (GNAS):** Applied to optimize the hyperparameters of both Deep CNN and ResNet models.
- **Haar Wavelet Transformation:** Enhances feature extraction by transforming the signals.

### Performance Evaluation
- Models are evaluated based on training and testing accuracies across different SNR levels.
- Comparisons are made between standard models and those optimized using GNAS.

### Key Findings
- **Deep CNN Model:**
  - Performs well for high SNR values (0, 5, 10, 15, 20, 25).
  - Performance decreases for low SNR values (-10, -5).
- **ResNet Model:**
  - Small model size (3.45 MB) and few trainable parameters.
  - No reduction in size or improvement in accuracy after applying GNAS.
- **Haar Wavelet Integration:**
  - Improves performance by enhancing feature extraction.
- **Model Performance Comparison:**
  - IQ deepCNN: Training accuracy: 93.22%, Testing accuracy: 92.64%.
  - IQ ResNet: Training accuracy: 72.21%, Testing accuracy: 74.66%.
  - Haar deepCNN: Training accuracy: 94.18%, Testing accuracy: 93.77%.
  - Haar ResNet: Training accuracy: 81.71%, Testing accuracy: 84.25%.
  - NAS IQ deepCNN: Training accuracy: 96.36%, Testing accuracy: 90.41%.
  - NAS Haar deepCNN: Training accuracy: 94.43%, Testing accuracy: 94.33%.
  - NAS IQ ResNet: Training accuracy: 58.85%, Testing accuracy: 63.01%.
  - NAS Haar ResNet: Training accuracy: 79.17%, Testing accuracy: 83.64%.

### Implementation
- **Python and Libraries:** Utilized for model development, training, and evaluation.
- **Tkinter and Matplotlib:** Used to create a user interface (UI) for displaying line and bar graphs for model performance at different SNR levels.
- **CSV Data Handling:** Analysis of data and results storage with precision up to 4 decimal places.

### Challenges
- Improving model performance for low SNR values.
- Optimizing hyperparameters effectively using GNAS.
- Handling large datasets efficiently.

### Future Work
- Further optimization of deep learning models to improve performance in low SNR conditions.
- Exploration of other advanced techniques, such as different wavelet transformations and neural architecture search methods.
- Implementation of the developed models in real-world HF radio signal classification scenarios.
