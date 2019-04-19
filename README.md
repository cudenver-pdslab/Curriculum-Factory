# Curriculum Factory  
## Curriculum-Based Training Technique for Convolutional Neural Networks 

<div align="center">
  <img src="https://github.com/cudenver-pdslab/Curriculum-Factory/blob/master/Artifacts/curriculum_learning.png">
</div>

This repository contains a number of different model weights frozen using our training implementation called Curriculum-Factory. The abstract of a the paper describing the techniques is below. The paper is submitted to [BMVC 2019](https://bmvc2019.org/).

# Abstract 

We present a new system that automatically generates input path (syllabus) a convolutional neural network follows through a curriculum learning. Our system utilizes information-theoretic content measures of training samples to form syllabus at training time. Every sample is treated as 2D random variable where a datapoint contained in the sample (such as a pixel) is modelled as an independent and identically distributed random variable (i.i.d) realization. We use information theory methods to rank and determine when a sample is fed to a network by measuring its pixel composition and its relationship to other samples in the training set. Comparative evaluation of multiple state-of-the-art networks, including, GoogleNet, and VGG, on benchmark datasets demonstrate a syllabus that ranks samples using measures such as Joint Entropy between adjacent samples, can improve learning and remarkably reduce the amount of training steps required to achieve desirable training accuracy. We present results that indicate our approach can reduce training loss by as much as a factor of 11 compared to conventional training. 


