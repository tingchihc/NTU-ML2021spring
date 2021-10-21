# YT  
  * https://www.youtube.com/watch?v=jNY1WBb8l4U  

## Theory behind GAN  


## Tips for GAN  
## JS divergence is not suitable  

 * in most cases, P(G) and P(data) are not overlapped.  
 * (1) The nature of data:  
   * Both P(data) and P(G) are low-dim mainfold in high-dim space.  
   * The overlap can be ignored.  
 
 * (2) Sampling:  
   * Even though P(data) and P(G) have overlap.  
   * If you do not have enough sampling ...  
 
 
## What is the problem of JS divergence?  

 * JS divergence is always log2 if two distribution do not overlap.  
 * Intuition: If two distributions do not overlap, binary classifier achieves 100% accuracy.  
 * The accuracy(or loss) means nothing during GAN training.  

## Wasserstein distance  
 
 * Wasserstein distance: the average distance that the earth mover has to move.  
 * There are many possible "moving plans". Using the "moving plan" with the smallest average distance to define the Wasserstein distance.  
 
![Image of Yaktocat(https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/theory%20gan%20and%20wgan.png)
