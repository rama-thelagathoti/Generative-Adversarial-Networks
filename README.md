# Generative-Adversarial-Networks

Introduction

Generative Adversarial Networks (GAN) are first introduced by Goodfellow et al. in the year of 2014 in their article titled “Generative Adversarial Networks”.  These networks may be used to create synthetic (i.e., fake) pictures that are perceptually close to their ground-truth true originals.
To generate fake images, two neural networks are used 
•	A generator that takes an input vector of randomly produced noise and outputs a "imitation" image that appears similar, if not identical, to the real image.
•	A discriminator or opponent who seeks to ascertain whether a particular image is "genuine" or "fake."
We can learn to produce synthetic pictures by training these networks at the same time, with one providing input to the other.
![Picture10](https://user-images.githubusercontent.com/36952323/217415202-cb04a5c8-87fd-4b2c-a789-6640b0b34831.png)

Working principle

The dataset that we will be using for GAN is MNIST dataset which contains 60,000 examples. At first discriminator is trained with MNIST real images so discriminator knows what the real images are and how they look like. At the same time generator is trained with random noise at the beginning. Now generator keeps on running in a training loop and learns what discriminator is expecting. Eventually generator generates an images such that it can fool the discriminator as if it’s a real image.  

Method

Generator and Descriminator networks are as follows

![Picture11](https://user-images.githubusercontent.com/36952323/217415295-954fe227-481e-45d9-b434-4c7e0ef5cddc.png)


![Picture12](https://user-images.githubusercontent.com/36952323/217415383-068bd9ce-c075-4ba9-8557-13562e443177.png)

Random noise generator for training the generator

![Picture13](https://user-images.githubusercontent.com/36952323/217415422-751fdd0e-50e1-4aea-8154-cebcc3ce4050.png)

Tuning parameters

Generator and discriminator are trained at the same time with following parameters
Number of Epochs = 100 
Noise dimensions = 100
Number of examples generated = 64
Due to colab usage limit and resource constraints I have trained both generator and discriminator for 100 epochs. Further, I have saved images at every 15 epochs.
To show how images are trained, I have displayed images at 5 epochs, 25 epochs, 50 epochs, 75 epochs and 100 epochs.  

Generator & Discriminator loss for every Epoch
![Picture14](https://user-images.githubusercontent.com/36952323/217415547-61e0e65c-a34d-4104-bf74-788259a71b2d.png)


Generator & Discriminator loss for every batch operation
 
![Picture15](https://user-images.githubusercontent.com/36952323/217415563-60792e6f-0b41-4d95-bc43-7a74cb024f48.png)

We know that generator and discriminator are competing against each other, at the beginning both of them are in two different extremes. But, ideally after certain epochs they will converge towards a constant parameter.  
From the given plot it is evident that generator loss is gradually decreasing after 50 epochs whereas discriminator loss seems to be increasing after 50 epochs. 

Figure 1: Images at epoch 5
![Picture16](https://user-images.githubusercontent.com/36952323/217415635-3484e3c9-721e-4f53-ad4b-dfe670947b9c.png)

Figure 1: Images at epoch 100
![Picture17](https://user-images.githubusercontent.com/36952323/217415678-f9d14ed8-80ee-49b8-8b5b-15a0f4978996.png)


