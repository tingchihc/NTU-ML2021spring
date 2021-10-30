slide p.17: https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/small-gradient-v7.pdf

## Review: Optimization with Batch

![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/batch.png)  

## 1. Small Batch & Large Batch

 * Smaller batch size has better performance
 * What's wrong with large batch size? A: Optimization Fails
 * "Noisy" update is better for training
 * Small batch is better on testing data
 
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/svl.png)

## 2. Momentum
Slide p.32-p.35

 * Critical points have zero gradients.  
 * Critical points can be either saddle points or local minima.  
 * Local minima may be rare.  
 * Smaller batch size and momentum help escape critical poins.  
