# Flower_Image_Classifier by Udacity
## Table of Contents

- [Project Description](#project-description)
- [Project Jupyter Notebook](#project-jupyter-notebook)
- [Command Line Training Application](#command-line-training-application)
- [Command Line Predict Application](#command-line-predicting-application)

## Project Description

In this project, I developed code for an image classifier built with PyTorch for 102 flower categories, then convert it into a command line application.

The project is combined with 3 parts:

1. Load and preprocess the image dataset;
2. Train the image classifier on your dataset;
3. Use the trained classifier to predict image content;

### Dataset
The dataset used in this project can be downloaded [here](https://s3.amazonaws.com/content.udacity-data.com/nd089/flower_data.tar.gz)

To run the project, please download the dataset first and unzip it in the project folder. Then rename the dataset folder to `flowers`

## Project Jupyter Notebook

The main code of this project is in the file [Image Classifier Project.ipynb](https://github.com/hyw1994/Flower_Image_Classifier/blob/master/Image%20Classifier%20Project.ipynb)

## Command Line Training Application

### Main file
The command line training application code is in the file [train.py](https://github.com/hyw1994/Flower_Image_Classifier/blob/master/train.py)

### Usage
Basic usage: `python train.py data_directory`

Prints out training loss, validation loss, and validation accuracy as the network trains

Options:

1. Set directory to save checkpoints: `python train.py data_dir --save_dir save_directory`

2. Choose architecture: `python train.py data_dir --arch "vgg13"`

3. Set hyperparameters: `python train.py data_dir --learning_rate 0.01 --hidden_units 512 --epochs 20`

4. Use GPU for training: `python train.py data_dir --gpu`

## Command Line Predicting Application

### Main file

The command line predict application code is in the file [predict.py](https://github.com/hyw1994/Flower_Image_Classifier/blob/master/predict.py)

### Usage

Basic usage: `python predict.py /path/to/image checkpoint`

Options:
1. Return top K most likely classes: `python predict.py input checkpoint --top_k 3`
2. Use a mapping of categories to real names: `python predict.py input checkpoint --category_names cat_to_name.json`
3. Use GPU for inference: `python predict.py input checkpoint --gpu`
