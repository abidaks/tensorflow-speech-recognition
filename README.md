# TensorFlow Speech Recognition Challenge
This repo contains the code for winning entry in the [TensorFlow Speech Recognition Challenge](https://www.kaggle.com/c/tensorflow-speech-recognition-challenge) hosted by [kaggle](https://www.kaggle.com). The task was to *build an algorithm that understands simple speech commands*.

The score of this model is: 0.91060.


# Appendix
##  A1.) Model Execution Time
- What software did you use for training and prediction?
  - see Requirements
- What hardware (CPUS spec, number of CPU cores, memory)?
  - a single GCP instance with 4 vCPUs, 18.5 GB memory and 
1 x NVIDIA Tesla K80
- How long does it take to train your model?
  - ~4-8 hours (depends on the model) for a single model
-


## A2.) Requirements:
- tensorflow>=2.3.0
- tensorflow-gpu>=2.3.0
- Keras>=2.4.3
- tqdm>=4.48.0
- scipy>=1.4.1
- numpy>=1.19.1
- pandas>=0.24.2
- pandas-ml>=0.6.1

All packages can be installed via `pip install`. Other versions will probably work too. I tested it with Python 3.7 using Ubuntu 20.04.

Note that installing scipy will take a couple hours. I tried removing this dependency by using the `wave` and `struct` modules but then reading the wavs is super slow (2 hours for all test files).
I tested it with Raspbian GNU/Linux 8 (Jessie) and Python 3.4.2.

## Installing dependencies

run below command to install dependencies
```
> git clone https://github.com/abidaks/tensorflow-speech-recognition
> cd tensorflow-speech-recognition
> pip install requirements.txt
```

## Downloading dataset
Before training the model you need to download the training dataset from [Kaggle](https://www.kaggle.com/c/tensorflow-speech-recognition-challenge/data?select=train.7z) and place it under `/data/`.


## Model training
Run the jupyter notebook `trainer.ipynb` to train the model.


