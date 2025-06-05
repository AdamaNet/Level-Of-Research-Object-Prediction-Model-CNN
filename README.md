# Multimodal Object Prediction Model - Deep Learning Method (CNN)

## Project Overview

This project is a deep learning model based on multimodal data, designed specifically for predicting the status or grade of objects. The model integrates numerical and image features using a Convolutional Neural Network (CNN) architecture to achieve accurate object classification.

## Model Features

- **Multimodal Fusion**: Processes both numerical and image data simultaneously to improve prediction accuracy
- **Automated Feature Extraction**: Extracts key features automatically through image preprocessing
- **High-Accuracy Classification**: Uses CNN models to identify different object levels
- **Visual Analysis**: Provides feature importance and sensitivity analysis visualizations

## System Requirements

- Python 3.8
- Required dependencies listed in the `requirements.txt` file

## Installation Guide

1. Clone the repository locally:

```bash
git clone https://github.com/qwerfgb/Level-Of-Research-Object-Prediction-Model-CNN
cd Level-Of-Research-Object-Prediction-Model-CNN
```

2. Install the dependencies:

```bash
pip install -r requirements.txt
```

## Data Input

The model requires two types of input data, both in Excel format:

1. **Numerical Feature Data**: Contains quantitative indicators related to the objects
2. **Image Feature Data**: Features extracted from raw images using `data/PreprocessImage.py`

### Image Preprocessing Pipeline

Raw image data should be stored in separate folders named after their corresponding object levels. Use `data/PreprocessImage.py` for feature extraction:

1. Read images from categorized folders
2. Extract image features
3. Save the features as an Excel file for model input

## Project Structure

```
Level-Of-Research-Object-Prediction-Model-CNN/
│
├── data/                          # Data processing module
│   ├── __init__.py                # Initialization file
│   └── PreprocessImage.py         # Image feature extraction script
│
├── model/                         # Model definition module
│   ├── __init__.py                # Initialization file
│   └── CNN.py                     # CNN classification model
│
├── README.md                      # Project documentation
└── requirements.txt               # Dependency list
```

## Output Results

After training, the model will generate the following outputs:

1. Training and validation accuracy and loss curves
2. Detailed classification performance report (accuracy, precision, recall, F1 score)
3. Feature importance ranking and visualization charts
4. Feature sensitivity analysis

## Notes

- Python version requirement: 3.8
- All required packages are listed in `requirements.txt`
- During preprocessing, images must be categorized into folders based on object levels
- Extracted feature Excel files must match the input format expected by the model
- Label values should be integers from 1 to n, representing different object levels
