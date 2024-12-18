# Ship Audio Classification Project

This repository contains a project focused on classifying underwater ship audio into categories such as `SpeedBoat`, `KaiYuan`, and `UUV` using deep learning models. The project includes data preprocessing, model training, and evaluation of two architectures: a Convolutional Neural Network (CNN) and a Transformer-based model.

## Project Structure

```
/<repository_name>
├── data/               # Data
│   ├── __noise_target 
│   ├── SpeedBoat      
│   ├── __KaiYuan      
│   ├── UUV           
│   └── KaiYuan         
├── ship_audio_classification.ipynb
├── README.md           # Project overview
└── requirements.txt    # Python dependencies
```

## Models Implemented

### Convolutional Neural Network (CNN)
- Designed for extracting local features from spectrograms.
- Better accuracy for the `KaiYuan` class.
- Efficient training with lower computational requirements.

### Transformer-based Model
- Incorporates long-range dependencies for improved balance across classes.
- Shows higher recall for `SpeedBoat` and `UUV` classes.

## Dataset
The dataset comprises spectrograms generated from underwater audio signals of various ship types. The data is organized into the following classes:

- `SpeedBoat`
- `KaiYuan`
- `UUV`

### Preprocessing
1. Convert time-domain audio into frequency-domain spectrograms.
2. Normalize and standardize spectrogram values.
3. Handle imbalances and prepare training, validation, and test splits.

## Training and Evaluation

### Training
- Models were trained using PyTorch with a dataset of spectrograms.
- Data split into 70% training, 15% validation, and 15% testing.
- Hyperparameters:
  - Optimizer: Adam
  - Learning Rate: 0.001
  - Epochs: 3

### Evaluation
Models were evaluated using:
- Classification metrics (precision, recall, F1-score).
- Confusion matrices.

### Results
- CNN achieved an accuracy of **50%**.
- Transformer achieved an accuracy of **46%**.

## Recommendations for Future Work

### Data Improvements
- Expand the dataset with more balanced samples.
- Enhance noise handling and augmentation.
- Collect samples from diverse acoustic conditions.

### Model Enhancements
- Hybrid CNN-Transformer architectures.
- Pre-training on larger acoustic datasets.
- Use of deeper network architectures.

### Evaluation Enhancements
- Test models in real-world conditions.
- Evaluate robustness to noise.
- Implement a confidence scoring system for predictions.

## Getting Started

### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- PyTorch 1.10+
- Required dependencies listed in `requirements.txt`.

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/AyanSanaullah/Ship-Audio-Classification-Project/
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Usage

#### Running the Notebook
The Jupyter notebook `assignment.ipynb` contains the code for:
- Data loading and preprocessing.
- Model training and evaluation.

#### Training the Models
Navigate to the `data/` directory and execute:
```bash
python UUV
```

#### Viewing Results
Model performance metrics and confusion matrices are displayed during evaluation.

## License
This project is licensed under the Apache 2.0 License. See the `LICENSE` file for details.

