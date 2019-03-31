# Flower_Image_Classifier by Udacity
## Table of Contents

- [Project Description](#project Description)
- [Installation](#installation)
- [Change Log](#change-log)
- [How to use](#how-to-use)
- [Note to Windows OS Users](#note-to-windows-os-users)
- [Development Experience](#development-experience)
- [Breaking Changes from Udacity API](#breaking-changes-from-udacity-api)
- [Reporting Issues](#reporting-issues)
- [User Privacy](user-privacy)
- [Disclaimer](#disclaimer)

## Project Description

In this project, I developed code for an image classifier built with PyTorch for 102 flower categories, then convert it into a command line application.

The project is combined with 3 parts:

1. Load and preprocess the image dataset;
2. Train the image classifier on your dataset;
3. Use the trained classifier to predict image content;

## Main files

### Project Jupyter Notebook

The main code of this project is in the file [Image Classifier Project.ipynb](https://github.com/hyw1994/Flower_Image_Classifier/blob/master/Image%20Classifier%20Project.ipynb)

### Command Line Training Application

The command line training application code is in the file [train.py](https://github.com/hyw1994/Flower_Image_Classifier/blob/master/train.py)

Basic usage: `python train.py data_directory`

Prints out training loss, validation loss, and validation accuracy as the network trains

Options:

1. Set directory to save checkpoints: `python train.py data_dir --save_dir save_directory`

2. Choose architecture: `python train.py data_dir --arch "vgg13"`

3. Set hyperparameters: `python train.py data_dir --learning_rate 0.01 --hidden_units 512 --epochs 20`

4. Use GPU for training: `python train.py data_dir --gpu`

### Command Line Predict Application

The command line predict application code is in the file [predict.py](https://github.com/hyw1994/Flower_Image_Classifier/blob/master/predict.py)

Basic usage: `python predict.py /path/to/image checkpoint`

Options:
1. Return top K most likely classes: `python predict.py input checkpoint --top_k 3`
2. Use a mapping of categories to real names: `python predict.py input checkpoint --category_names cat_to_name.json`
3. Use GPU for inference: `python predict.py input checkpoint --gpu`
