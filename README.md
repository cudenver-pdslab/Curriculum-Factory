# Curriculum Factory  
## Curriculum-Based Training Technique for Convolutional Neural Networks 

<div align="center">
  <img src="https://github.com/cudenver-pdslab/Curriculum-Factory/blob/master/Artifacts/curriculum_learning.png">
</div>

This repository contains a number of different model weights frozen using a new technique called Curriculum-Factory. The abstract of a the paper describing the techniques is below. The paper is submitted to [BMVC 2019](https://bmvc2019.org/).

# Abstract 

We present a new system that automatically generates input path (syllabus) a convolutional neural network follows through a curriculum learning. Our system utilizes information-theoretic content measures of training samples to form syllabus at training time. Every sample is treated as 2D random variable where a datapoint contained in the sample (such as a pixel) is modelled as an independent and identically distributed random variable (i.i.d) realization. We use information theory methods to rank and determine when a sample is fed to a network by measuring its pixel composition and its relationship to other samples in the training set. Comparative evaluation of multiple state-of-the-art networks, including, GoogleNet, and VGG, on benchmark datasets demonstrate a syllabus that ranks samples using measures such as Joint Entropy between adjacent samples, can improve learning and remarkably reduce the amount of training steps required to achieve desirable training accuracy. We present results that indicate our approach can reduce training loss by as much as a factor of 11 compared to conventional training. 


<div align="center">
  <img src="https://github.com/cudenver-pdslab/Curriculum-Factory/blob/master/Artifacts/curriculum_factory_2.png">
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
| GoogleNet-MI |	0.615	| 0.358 |	[Mutual Information](https://en.wikipedia.org/wiki/Mutual_information)|
| GoogleNet-MIN |	0.456 |	0.146 |	[Mutual Information Normalized](https://en.wikipedia.org/wiki/Mutual_information) |
| GoogleNet-IV |	0.671 | 0.456 |	[Information Variation](https://en.wikipedia.org/wiki/Variation_of_information) |
|GoogleNet-JE|	0.586|	0.489|	[Joint Entropy](https://en.wikipedia.org/wiki/Joint_entropy)|
|ResNet|	0.954|	0.791	|None|
|ResNet-MI	|0.945	|0.842|	MI|
|ResNet-MIN|	0.973|	0.789|	MIN|
|ResNet-IV|	0.943	|0.849|IV|
|ResNet-JE|	0.924|	0.851	|JE|
|VGG	|0.922|	0.645|	None|
|VGG-MI	|0.945|	0.512|	MI |
|VGG-MIN|	0.904	|0.602|	MIN|
|VGG-IV|	0.897|	0.698|	IV|
|VGG-JE|	0.943|	0.631|	JE|

