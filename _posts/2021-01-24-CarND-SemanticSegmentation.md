---
layout: post
title: "Semantic Segmentation"
subtitle: "Udacity Self-Driving NanoDegree Term 3 Project on Semantic Segmentation"
date: 2021-01-24 23:45:13 -0400
background: '/img/posts/05.jpg'
---


## Project: Semantic-Segmentation [![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

Overview
---
  This project implements semantic segmentation for Udacity's Self Driving Car Nanodegree using a fully convolutional neural network. The network comprises of an encoder based on VGG-16 model, and a decoder based on transposed convolutions, 1x1 convolutions and skip-layer connections.

Code changes
---
For this project I made the following changes to the starter code.

__*main.py*__

1. I modified the _load_vgg_ method to return the tensors associated with the input image, and the outputs of layer 3, 4 and 7 of the VGG network.
2. I modified the _layers_ method to implement the decoder for the fully convolutional network. The topology of the full network is shown below. Observe the transposed convolution nodes and skip layer connections in the decoder portion of the network.

![Network Graph](/img/posts/Network_Graph.png)

3. I implemented the _optimize_ method to compute the total loss which comprises of both the cross-entropy loss and L2 regularization loss. The training operation is performed by an Adam Optimizer with a tuning hyperparameter of 0.0001.
4. Finally, I implemented the _train_nn_ method to initalize a TensorFlow session, and perform SGD using a minibatch size of 5 samples, and 50 training epochs. I also experimented with 10 and 25 epochs, but settled on 50 epochs based on performance. The total loss for the final selection of minibatch size of 5 and 50 training epochs is shown below.

![Network Loss](/img/posts/Network_Loss.png)

__*Results*__

The performance results for 10, 25 and 50 epochs of training is shown below. As the number of epochs increases the accuracy of the detection increases, as well as the smoothness of the boundaries between road and non-road pixels increases.

![Network Performance](/img/posts/Performance.bmp)

The outputs for all test samples for 50 epochs is stored within _runs/_ folder.
