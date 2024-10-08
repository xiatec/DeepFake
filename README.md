# Deepfake Image Detector

## Executive Summary

This project aims to combat the rising risks associated with accessible generative AI, specifically deepfakes, by creating a robust deepfake detector using convolutional neural networks (CNNs). The best-performing model achieved a validation accuracy of 0.965 and precision of 0.992, making it a powerful tool for distinguishing between real and fake images.

## Key Features

- Utilizes different CNN architectures
- Achieves high accuracy and precision in deepfake detection
- Provides pre-trained models for out-of-the-box solutions
- Includes both a detector mode and a game mode for user interaction

## Model Performance

The EfficientNet model demonstrated the best performance:

- Validation Accuracy: 0.965
- Validation Precision: 0.992

## Getting Started

### Prerequisites
```
pip install streamlit
pip install tensorflow  
```

### Installation

1. Clone the repo
```
git clone https://github.com/xiatec/DeepFake.git
```

2. Navigate to the models folder and unzip:

```
cd deepfake-image-detector/code/PretrainedModel/
unzip dffnetv2B0.zip
```

3. Run the Streamlit app:

```
streamlit run main.py
```

4. Activate your virtual environment and run the app:

```
source activate your_envs
streamlit run multipage_app.py
```

## Usage

The application offers two modes:

1. Detector: Upload images to check if they are deepfakes
2. Game: Test your ability to distinguish between real and fake images

Note: This detector is optimized for photo-realistic images of humans and may struggle with cartoons or drawn images.

## Technical Details

### Data Source

The project uses the OpenForensics dataset, an open-source collection of labeled real and fake images.

### Model Architecture

The project experimented with two types of CNN architectures:
1. Sequential models
2. EfficientNet models

### Data Preprocessing
- Data was taken from OpenForensics (an open-source dataset of labeled real and fake images) link: https://zenodo.org/records/5528418#.ZGaehnbMKHv

- Images were formatted to (256, 256) dimensions
- Data augmentation techniques were applied, including rotation, flipping, and contrast adjustment

<!-- ### Training Process

```python
model.fit(
    train_ds,
    validation_data=val_ds,
    epochs=50,
    callbacks=[early_stopping, model_checkpoint]
)
``` -->
<!-- 
## Results

The EfficientNet_v2B0 model achieved the following results:

- Training Accuracy: 0.9176
- Training Precision: 0.9100
- Training Recall: 0.9270
- Training AUC: 0.9747
- Validation Accuracy: 0.8216
- Validation Precision: 0.7723
- Validation Recall: 0.9139
- Validation AUC: 0.9169 -->

<!-- ## Future Improvements

- Incorporate a wider variety of altered images in the training data
- Experiment with longer training periods and more powerful computing resources
- Explore ensemble methods combining multiple model architectures -->
