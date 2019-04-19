# Curriculum Factory  
## Curriculum-Based Training Technique for Convolutional Neural Networks 

<div align="center">
  <img src="https://github.com/cudenver-pdslab/Curriculum-Factory/blob/master/Artifacts/curriculum_learning.png">
</div>

This repository contains a number of different model weights frozen using a new technique called Curriculum-Factory. The abstract of a the paper describing the techniques is below. The paper is submitted to [BMVC 2019](https://bmvc2019.org/).

# Abstract 

We present a new system that automatically generates input path (syllabus) a convolutional neural network follows through a curriculum learning. Our system utilizes information-theoretic content measures of training samples to form syllabus at training time. Every sample is treated as 2D random variable where a datapoint contained in the sample (such as a pixel) is modelled as an independent and identically distributed random variable (i.i.d) realization. We use information theory methods to rank and determine when a sample is fed to a network by measuring its pixel composition and its relationship to other samples in the training set. Comparative evaluation of multiple state-of-the-art networks, including, GoogleNet, and VGG, on benchmark datasets demonstrate a syllabus that ranks samples using measures such as Joint Entropy between adjacent samples, can improve learning and remarkably reduce the amount of training steps required to achieve desirable training accuracy. We present results that indicate our approach can reduce training loss by as much as a factor of 11 compared to conventional training. 


<div align="center">
  <img src="https://github.com/cudenver-pdslab/Curriculum-Factory/blob/master/Artifacts/curriculum_factory_github.png">
</div>

## Performance Metric

## Training Preformance 

<div align="center">
  <img src="https://github.com/cudenver-pdslab/Curriculum-Factory/blob/master/Artifacts/CIFAR10AND100.png">
</div>


### Classificatoin Accurcay on CIFAR10 and CIFAR100 datasets 

| Network     | CIFAR10 (test acc. %)  | CIFAR100 (test acc. %) | Curriculum |
| ---             | ---    | ---       | ---          |
| GoogleNet	| 0.528	| 0.433	| None |
| GoogleNet-MI |	<strong> 0.615	<strong>| 0.358 |	[Mutual Information (MI)](https://en.wikipedia.org/wiki/Mutual_information)|
| GoogleNet-MIN |	0.456 |	0.146 |	[Mutual Information Normalized (MIN)](https://en.wikipedia.org/wiki/Mutual_information) |
| GoogleNet-IV |	<strong>0.671<strong> | <strong>0.456<strong>|	[Information Variation (IV)](https://en.wikipedia.org/wiki/Variation_of_information) |
|GoogleNet-JE|	0.586|	<strong>0.489<strong>|	[Joint Entropy (JE)](https://en.wikipedia.org/wiki/Joint_entropy)|
|ResNet|	0.954|	0.791	|None|
|ResNet-MI	|0.945	|<strong>0.842<strong>|	MI|
|ResNet-MIN|	<strong>0.973<strong>|	0.789|	MIN|
|ResNet-IV|	0.943	|<strong>0.849<strong>|IV|
|ResNet-JE|	0.924|	<strong>0.851<strong>	|JE|
|VGG	|0.922|	0.645|	None|
|VGG-MI	|0.945|	0.512|	MI |
|VGG-MIN|	<strong>0.904<strong>	|0.602|	MIN|
|VGG-IV|	0.897|	0.698|	IV|
|VGG-JE|	<strong>0.943<strong>|	0.631|	JE|

# Model Zoo 

