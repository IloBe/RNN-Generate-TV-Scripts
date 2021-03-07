# RNN: Generate TV Scripts
## Introduction
Welcome to this RNN project of the Udacity Deep Learning course. We generate an original TV script by using a recurrent neural network which has been trained on existing Seinfeld TV scripts. In other words, we are using a dataset of scripts about this US sitcom for model learning. 

Have in mind, that for creating a fake script the project iterates over a large amount of data, and it takes a number of hours to train, even on GPU. Therefore, to manage the GPU workspace time given for this project, we build and test the RNN model (including data pre-processing, defining model architecture, etc.) in CPU mode by creating and activating its own new environment, then GPU mode to accelerate training is activated.

This project coding is released under the MIT license.
