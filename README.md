
# Hand Gesture Recognition using Recurrent Neural Network (RNN)

This repository contains keras implementation of two deep learning models for hand gesture recognition presented in the article  [A Comparison of Bidirectional GRU and LSTM for Hand Gesture Recognition Using Leap Motion](https://ieeexplore.ieee.org/document/10023591) by Muhammad Saad, Tianbao Yang, Hui Zhou.


## Getting Started

American Sign Language (ASL) Dataset is utillized for training and testing of our model. We have presented the following two bidirectional recurrent neural network models.
#### a) Bidirectional Gated Recurrent Unit (Bi-GRU)
#### b) Bidirectional Long Short Term Memory (Bi-LSTM)

[Downlaod Dataset](https://bitbucket.org/visionlab-sapienza/2018-jrl-ieee-tmm_-application-dataset/src/master/)

For more information about dataset [click](https://ieeexplore.ieee.org/document/8410764) here 

| File                       |        Description         |
| :-------- | :------------------------- |
| `loading_asl_dataset.ipynb` | This notebook contains code for getting ASL dataset and store into a single pickle file for further use. |
| `RNN_models.ipynb` | This notebook contains model creation and training. You can generate models by simply running the function of the desired model and can use the dataset processed in the earlier notebook to train that model.  |

## Model Overview
![Model Overview](https://github.com/saad-lab/Hand_Gesture_Recognition_Using_RNN/blob/5fc5594909bbb0335c87cc455b8e04e153565091/model.png)




## Model Input 

Hand skeletal representations are lightweight and very sparse compared to image and video representations. Some sensors directly provide streams of body skeletons or hand skeletons e.g. Leap Motion, Kinect camera, RealSense camera etc. In this work we have used ASL-Dataset, which is skeletal data of hand gestures recorded with leap motion sensor.

![Hand features used in dataset](https://github.com/saad-lab/Hand_Gesture_Recognition_Using_RNN/blob/c63c2c0b3d413f97750a205a86a8d6c253193b71/features.png)

The input to the model is an array of the following shape

(samples, timestamps, attributes)

where 

samples = 810, total number of examples in train dataset

timestamps = 200, number of time instances in each sample

attributes = 32, these are the number of features in one timestamp

## Requirements
The notebook will run fine with:

`python 3`

`tensorflow` `keras`

Usual pip modules: `sklearn` `nump` `matplotlib` `seaborn`


## Citation

#### If you find this code useful kindly cite the below article.


@INPROCEEDINGS{10023591,
  
  author={Saad, Muhammad and Yang, Tianbao and Zhou, Hui},
  
  booktitle={2022 37th Youth Academic Annual Conference of Chinese Association of Automation (YAC)}, 
  
  title={A Comparison of Bidirectional GRU and LSTM for Hand Gesture Recognition Using Leap Motion}, 
  
  year={2022},
  

  pages={1427-1433},
  
  doi={10.1109/YAC57282.2022.10023591}}
