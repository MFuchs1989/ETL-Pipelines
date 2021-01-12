
# ETL-Pipelines with Python


![etl_main_pic](images/pipelines.png)

A rule of thumb says that a data scientist spends 80% of his time on data preparation. The same amount of code is generated at this point. If you are working on a customer project that is only interested in the results, the notebook in which you are working, for example, is quickly overcrowded with syntax that only refers to the preparation of the data. For such a case it is a good idea to write an ETL-script. 


## Table of Contents
1. [Introduction](#introduction)
2. [Software Requirements](#software_requirements)
3. [Folder Structure](#folder_structure)
4. [Getting Started](#getting_started)
5. [Overview of the ETL steps](#overview)
    1. [Simple_Pipeline](#simple_pipeline)
    2. [Pipeline_with_join](#pipeline_with_join)
    3. [Pipeline_with_join2](#pipeline_with_join2)
    4. [Pipeline_with_intermediate_storage](#pipeline_with_intermediate_storage)  
6. [Project Results](#project_results)    
7. [Authors](#authors)
8. [Motivation](#motivation)




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
Inside the data folder I create another folder called 'input'. This is where I put my original /raw files.
The output-folder shown above are automatically created by the ETL.
With the help of the notebooks I developed the .py file. The etl_pipeline.py files are always stored in the data-folder.



<a name="getting_started"></a>

## Getting Started

1. Make sure Python 3 is installed.
2. Clone the repository and navigate to the respective project's root directory in the terminal
3.  ETL execution
    1. from jupyter notebook: The ETL file can be executed directly from a Jupyter notebook. A sample procedure can be found under notebooks/Test_Notebook.
    2. from command line: Use a command line of your choice and navigate to the respective project's root directory. Run the following commands:
        1. ```cd "path/to/root directory"```
        2. ```python etl_pipeline.py"```




5. [Overview of the ETL steps](#overview)
    1. [Simple_Pipeline](#simple_pipeline)
    2. [Pipeline_with_join](#pipeline_with_join)
    3. [Pipeline_with_join2](#pipeline_with_join2)
    4. [Pipeline_with_intermediate_storage](#pipeline_with_intermediate_storage)




<a name="overview"></a>

## Overview of the ETL steps

In the following I show the individual steps that are used in the respective ETL variants:

<a name="simple_pipeline"></a>

### Simple_Pipeline

![Overview_Simple_Pipeline](images/Overview_Simple_Pipeline.png)
![Legend](images/Legend.png)

<a name="pipeline_with_join"></a>

### Pipeline_with_join

![Overview_Pipeline_with_join](images/Overview_Pipeline_with_join.png)
![Legend](images/Legend.png)

<a name="pipeline_with_join2"></a>

### Pipeline_with_join2

![Overview_Pipeline_with_join2](images/Overview_Pipeline_with_join2.png)
![Legend](images/Legend.png)

<a name="pipeline_with_intermediate_storage"></a>

### Pipeline_with_intermediate_storage

![Overview_Pipeline_with_intermediate_storage](images/Overview_Pipeline_with_intermediate_storage.png)
![Legend](images/Legend.png)



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

## Motivation: 

I've been blogging since 2018 on my homepages about all sorts of topics related to Machine Learning, Data Analytics, Data Science and much more.
You are welcome to visit them:

+ [Python Blog](https://michael-fuchs-python.netlify.app/)
+ [R Blog](https://michael-fuchs.netlify.app/)

I also publish individual interesting sections from my publications in separate repositories to make their access even easier. 
