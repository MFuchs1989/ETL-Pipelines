
# ETL-Pipelines with Python


![etl_main_pic](images/pipelines.png)

A rule of thumb says that a data scientist spends 80% of his time on data preparation. The same amount of code is generated at this point. If you are working on a customer project that is only interested in the results, the notebook in which you are working, for example, is quickly overcrowded with syntax that only refers to the preparation of the data. For such a case it is a good idea to write an ETL-script. 


## Table of Contents
1. [Introduction](#introduction)
2. [Software Requirements](#software_requirements)
3. [Folder Structure](#folder_structure)
4. [Getting Started](#getting_started)
5. [Running APP](#running_app)
    1. [Detect Humans Face](#detect_humans_face)
    2. [Classify Dog Breeds](#classify_dog_breeds)
6. [Project Results](#project_results)    
7. [Authors](#authors)
8. [Project Motivation](#motivation)
9. [Acknowledgements](#acknowledgement)




<a name="introduction"></a>

## Introduction

In this repository I have stored several variants of ETL pipelines. They serve as a template and can be extended as desired.

<a name="software_requirements"></a>

## Software Requirements

Required libraries:

+ Python 3.x
+ Numpy
+ Pandas


Please run ```pip install -r requirements.txt```



<a name="folder_structure"></a>

## Folder Structure

```
├───1_Simple_Pipeline
│   ├───data
│   │   ├───input
│   │   └───output
│   └───notebooks
├───2_Pipeline_with_join
│   ├───data
│   │   ├───input
│   │   └───output
│   └───notebooks
├───3_Pipeline_with_join2
│   ├───data
│   │   ├───input
│   │   └───output
│   └───notebooks
└───4_Pipeline_with_intermediate_storage
    ├───data
    │   ├───input
    │   ├───input_modified
    │   └───output
    └───notebooks
```

I have built 4 different ETL variants. 

+ 1_Simple_Pipeline
+ 2_Pipeline_with_join
+ 3_Pipeline_with_join2
+ 4_Pipeline_with_intermediate_storage

The basic structure of all four variants is the same. 
Each variant includes a data folder and a folder for the notebooks. 
With the help of the notebooks I developed the .py file. The etl_pipeline.py files are always stored in the data-folder.



<a name="getting_started"></a>

## Getting Started

1. Make sure Python 3 is installed.
2. Clone the repository and navigate to the respective project's root directory in the terminal
3.  ETL execution
    1. from jupyter notebook: The ETL file can be executed directly from a Jupyter notebook. A sample procedure can be found under notebooks/Test_Notebook.
    2. from command line: Use a command line of your choice and navigate to the respective project's root directory. Run the following commands:
        ```cd "path/to/root directory"```
        ```python etl_pipeline.py"```
3. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip). Unzip the folder and place the three files (test, train and valid) in the cloned repository in the folder ```data/dog_images```. If one of these folders does not yet exist, please create it manually. 
4. Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip). Unzip the folder and place it in the cloned repository in the folder ```data/lfw```. If one of these folders does not yet exist, please create it manually. 
5. Download the [VGG-19](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG19Data.npz) and [InceptionV3](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogInceptionV3Data.npz) bottleneck features and place them in the cloned repository in the folder ```bottleneck_features```. If this folder does not yet exist, please create it manually. 
6. Start the notebook ```dog_app.ipynb```.



<a name="running_app"></a>

## Running APP



## Running APP

<a name="detect_humans_face"></a>

### Detect Humans Face

I used OpenCV's implementation of [Haar feature-based cascade classifiers](https://docs.opencv.org/master/d7/d8b/tutorial_py_face_detection.html) to detect human faces in images.

![pic_readme1](images/pic_readme1.png)


<a name="classify_dog_breeds"></a>

### Classify Dog Breeds

I used transfer learning to create a convolutional neural network (CNN). I used this to determine the breed of dog from dog pictures. 

+ If a dog is recognised in the image supplied, the algorithm returns the corresponding breed:

![pic_readme2](images/pic_readme2.png)

![pic_readme3](images/pic_readme3.png)

+ If a human is recognised in the image provided, the algorithm returns the resembling dog breed:

![pic_readme4](images/pic_readme4.png)


+ If neither a human nor a dog can be seen in the picture, the algorithm returns the following error message: "Error: Please input an image of a human or a dog."

<a name="project_results"></a>

## Project Results

In summary, the CNN model I created with transfer learning far surpassed the CNN created from scratch in terms of performance. 
The accuracy of the InceptionV3-model (pre-trained on ImageNet) reached 79.55% while the CNN from scratch was about 5%.
The ImageNet dataset contains more than one million training images on which the InceptionV3 model was trained. This results in an extreme increase in performance compared to CNN from scratch. 
The accuracy of 5% could possibly have been increased again if data augmentation had been used in the model training.
When tested on new images, the CNN model with transfer learning performed as I expected, not perfect but good enough. 

<a name="authors"></a>

## Authors

+ [Michael Fuchs](https://github.com/MFuchs1989)

<a name="motivation"></a>

## Project Motivation: 

Udacity has given students the freedom to choose the area in which they would like to complete their capstone project. Possible technical fields would have been:

+ [Robot Motion Planning](https://docs.google.com/document/d/1ZFCH6jS3A5At7_v5IUM5OpAXJYiutFuSIjTzV_E-vdE/pub)
+ [Healthcare](https://docs.google.com/document/d/1WzurKKa9AX2DnOH7KiB38mvozdOSemfkGpex8hdTy8c/pub)
+ [Computer Vision](https://docs.google.com/document/d/1y-XfjkPFgUQxFIQ9bBncUSjs4HOf5E-45FrLYNBsZb4/pub)
+ [Education](https://docs.google.com/document/d/1vjerjRQnWs1kLbZagDYT6rNqiwAG23Yj45oUY88IAxI/pub)
+ [Investment and Trading](https://docs.google.com/document/d/1ycGeb1QYKATG6jvz74SAMqxrlek9Ed4RYrzWNhWS-0Q/pub)

As I am personally very interested in Deep Learning and have already completed my Nanodegree in Computer Vision via Udacity, I found it exciting to complete my capstone project in this area as well. 
So I choose to use Convolutional Neural Networks to Identify Dog Breeds.

<a name="acknowledgement"></a>

## Acknowledgements

I thank [Udacity](https://www.udacity.com/) for providing this challenge and learning experience. 