# Developing an Automatic Recording Unit (ARU) with a Raspberry Pi

This repository contains the implementation of a convolutional neural network (CNN) for bird vocalization classification into two classes: "NO BIRD" and "BIRD".

## Features

- Uses a 2D CNN architecture for audio classification.
- Implements data augmentation techniques such as noise addition and rolling.
- Provides evaluation metrics including accuracy, precision, recall, and F1-score.
- Includes a report summarizing the study.

## Usage

1. Install the required dependencies using `requirements.txt`.
2. Prepare your audio dataset and organize it into appropriate directories.
```
Data/
├── Audios/
│   ├── audio_1.wav
│   ├── audio_2.wav
│   ├── ...
│   ├── ...
│   └── audio_n.wav
├── Annotations/
│   ├── audio_1.svl
│   ├── audio_2.svl
│   ├── ...
│   ├── ...
│   └── audio_n.svl
├── DataFiles/
│   ├── TrainingFiles.txt (list of the training files without extension)
│   └── TestingFiles.txt (list of the testing files without extension)
├── Model_Output/
│   └── <leave empty>
├── Pickled_Data/
│   └── <leave empty>
└── Saved_Data/
    └── <leave empty>
```

3. Run the notebook.
4. Experiment with different hyperparameters and model architectures for optimization.

## Requirements

- Python 3.x
- Keras
- NumPy
- Matplotlib
- Librosa
- Scipy
- Scikit-Learn

## Data

- The data used to train the model can be accessed [here](https://drive.google.com/file/d/15m8Y1REw0pbPHfnfSH7mAMXToXcuFM6l/view?usp=sharing). The data has been collected in the Intaka Island reserve with the purpose and consists of bird sounds and ambient noises that occur in their natural environment. Intaka Island is a 16-hectare wetland reserve located in the heart of Century City, 7km away from central Cape Town, South Africa. The following picture shows how we covered the Intaka Island.

<div style="text-align: center;">
    <img src="https://drive.google.com/uc?export=download&id=1sBs7vXmzdfXQrisN1hj5VI7K0ZDxKJX-" alt="Alt text"/>
</div>


## Model Performance

### Training curves
<div align="center">
    <img src="https://drive.google.com/uc?export=download&id=1Jkzg1f1gRdN8M6Q_JhKUvcaVoIrs5k1r" alt="Alt text"/>
</div>


### Confusion matrix
<div align="center">
    <img src="https://drive.google.com/uc?export=download&id=1Uvz2rNu7_otTSKAaa3rLiMVDqPpZmso1" alt="Alt text"/>
</div>

### Classification report

|          | precision | recall | f1-score | support |
|----------|-----------|--------|----------|---------|
| NO BIRD  |   0.59    |  1.00  |   0.74   |    32   |
| BIRD     |   1.00    |  0.80  |   0.89   |   110   |
|----------|-----------|--------|----------|---------|
| accuracy |           |        |   0.85   |   142   |
| macro avg|   0.80    |  0.90  |   0.82   |   142   |
| weighted avg | 0.91  |  0.85  |   0.86   |   142   |

## References
