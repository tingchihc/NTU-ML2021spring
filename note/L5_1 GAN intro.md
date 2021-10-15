# Slide:  
  * https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/gan_v10.pdf  
# YT:  
  * https://www.youtube.com/watch?v=4OWp0wDu6Xw  

## Generative Adversarial Network(GAN)  
## Network as Generator  
 * ex.: input [x,Simple Distribution z] -> Network(Generator) -> output [Complex Distribution y]  
 * z: we know its formulation, so we can sample from it.  

## Why Generator? Why distribution?  
 * Especially for the tasks needs "creativity".  
 * The same input has different outputs.  

## Example: Anime Face Generation  
## 1. Unconditional generation  
 * input: Normal Distribution z (low-dim vector) ex: [0.3,-0.1...-0.7]  
 * output: Complex Distribution y (high-dim vector)  
 * input -> Generator -> output  

## 2. Discriminator - it is a neural network  
 * input: image  
 * output: scalar(larger value means real, smaller value value fake.)  

## 3. Basic idea of GAN  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/GAN%20basic%20idea.png)  

## Algorithm:  
 * Initialize generator and discriminator.  
 * In each training iteration:  

## Step1:  
 * Fix generator G, and update discriminator D.  
 * Database -> Sample (to update D).  
 * Discriminator learns to assign high scores to real objects and low scores to generated objects.  

## Step2:  
 * Fix discriminator D, and update generator G.  
 * Generator learns to "fool" the discriminator.  
