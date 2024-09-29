# Gesture Recognition
> Make a Smart TV system which can control the TV with user’s hand gestures as the remote control.
---

## Problem Statement
Imagine you are working as a data scientist at a home electronics company which manufactures state of the art smart televisions. You want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:

Thumbs up:  Increase the volume

Thumbs down: Decrease the volume

Left swipe: 'Jump' backwards 10 seconds

Right swipe: 'Jump' forward 10 seconds  

Stop: Pause the movie

## Understanding the Dataset
The training data consists of a few hundred videos categorised into one of the five classes. Each video (typically 2-3 seconds long) is divided into a sequence of 30 frames(images). These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use.

The data is in a zip file. The zip file contains a 'train' and a 'val' folder with two CSV files for the two folders. 

These folders are in turn divided into subfolders where each subfolder represents a video of a particular gesture. Each subfolder, i.e. a video, contains 30 frames (or images). Note that all images in a particular video subfolder have the same dimensions but different videos may have different dimensions. Specifically, videos have two types of dimensions - either 360x360 or 120x160 (depending on the webcam used to record the videos). Hence, you will need to do some pre-processing to standardise the videos. 

## Deep Learning Models used
1. Conv3D
2. CNN with LSTM
3. CNN with GRU
4. CNN with GRU (with trainable weights of Transfer Learning)

## Conclusion
Based on the results CNN with GRU (with trainable weights of Transfer Learning) model
performing well on the dataset provided for Gesture Recognition.
Selected model: **CNN with GRU (with trainable weights of Transfer Learning)**
- Training Accuracy: 0.99
- Validation Accuracy: 0.99
- Batch Size: 5
- Frames: 16
- Number of epochs: 20
- Model File Name: model-00020-0.01408-0.99698-0.02186-1.00000.keras
- Model Loss and Accuracy comparison b/w Train and Validation set:
  ![image](https://github.com/dynamicanupam/Hand-Gesture-Recognition/assets/61014822/8c92e863-bd17-4635-82d0-6c18eaa6a3e6)
