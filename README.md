# SeqGAN

## Requirements: 
* **Tensorflow r1.0.1**
* Python 2.7
* CUDA 7.5+ (For GPU)

## Introduction
Apply Generative Adversarial Nets to generating sequences of discrete tokens.

![](figures/seqgan.png)

The illustration of SeqGAN. 

Left: D is trained over the real data and the generated data by G. 

Right: G is trained by policy gradient where the final reward signal is provided by D and is passed back to the intermediate action value via Monte Carlo search.  

[SeqGAN: Sequence Generative Adversarial Nets with Policy Gradient](http://arxiv.org/abs/1609.05473) 

train
```
$ python sequence_gan.py
```
The experiment has two stages

* use the positive data provided by the oracle model and Maximum Likelihood Estimation to perform supervise learning. 
* use adversarial training to improve the generator.