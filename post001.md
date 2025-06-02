---
layout: post
title: "Action Recognition Modeling and Integration"
date: 2025-06-01
author: JCP
---

## Features Developed This Month

This month we developed a system to create and train action recognition models using MediaPipe and data augmentation techniques to produce accurate models with less than 50 samples. We were able to introduce the model we trained into the main application that performs object detection. 

## Visual Components

[We'll add images/diagrams here]

## Retrospective

### What went right this month?

This month we were fortunate to have a lot of time available to dedicate to our project due to our work schedule opening up time for us to work on our studies. Knowing how challenging it is to annotate images for model training from a previous project, we decided to make this the focus of the effort. Our efforts began by examining other action recognition projects and looking for trends in the model composition and sample types. Thanks to "Python Feature Engineering Cookbook" by Soledad Galli which was recommended further reading material from our Machine Learning course, we were able to find ways to augment the sample data (JSON format) by adding versions of each sample at different time scales, rotating the position of the base, introducing noise, and fliping the images through into our action recognition model training algorithm. 

### What went wrong this month?
Initially, we were not successfull with the model training algorithm. Our approach was to train only a single action thinking this would be the most efficient way to produce a lightweight model. However, because we did not train the model on what an action is NOT - it was performing poorly by classifying each action as the same event, simply because there was motion. We then had issues with where our position was before we began the action we were training on. In moving to the starting position there was data being recorded that had nothing to do with the gesture we wanted to record. We solved this by creating a countdown timer to allow us to get into place and position before beginging the action. Finally, after adding 5 more actions to train on we reduced our false positive rate to an acceptable level and the model began performing with high confidence scores in the training and validation process. 

 When we attempted to integrate the action recognition feature into our main application we had to do quite a bit of troubleshooting to understand what variables were afecting each models performance. The size of the video frame in the main application did not match the size of the training application. I assumed this was just a display setting, not something the models would consider when performing inference. Once I matched the main application size and frame rate to the action recognition models training data we were able to get successfull detections of both the action and object detection models. Which is curious, why did the object detection model not perform differently? 

 Also, our Verion 3 prototype perfomed great with just CPU processing. For this version we have had to leverage CUDA for performance enhancements since the action recogition and object detection concurent inference tasks are not running optimally.

I was able to get this to work at an MVP level within a few hours of the submission after hectic week where I also had to present my capstone project proposal and attend a defense. 

### How can you improve moving forward?

Going forward I will need to give a full effort to the development process. Right now the prototype works, but it seems to be very heavy on resource consumption. 
