## YT  
  * https://www.youtube.com/watch?v=z-Q9ia5H2Ig&feature=youtu.be  

## White Box & Black Box  
  * White box attack: we know the network parameters.  

## Black Box Attack  
  * If you have the training data of the target network  
  * Training a proxy network yourself and using the proxy network to generate attacked objects  

## What if we do not know the training data?  using test data pair(input,output) to attack.  
## Defense passive & proactive  

## Passive Defense (Filter: smoothing)  
  * input(original img + attack signal) -> Filter(e.g. smoothing) -> (img + less harmful) -> Network -> normal output  

## Passive Defense (image compression)  
## Passive Defense (Generator)  
## Passive Defense - Randomization  
  * https://arxiv.org/abs/1711.01991  

## Proactive Defense
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/proactive%20defense.png)  

## Concluding Remarks  
  * Attack: given the network parameters, attack is very easy.  
  * Even black box attack is possible.  
  * Defense: passive and proactive.  
  * Attack/Defense are still envolving.  
