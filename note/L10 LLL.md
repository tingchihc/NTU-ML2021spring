## YT  
  * https://www.youtube.com/watch?v=rWF9sg5w6Zk  

## slide  
  * https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/life_v2.pdf  

## Life-long learning  
## LLL in real-world applications  
 * The network has enough capacity to learn both tasks.  
 * old tasks(labelled data) -> Model -> online -> Feedback -> New tasks -> Model  

## Catastrophic forgetting(Multi-task training can be considered as the upper bound of LLL)  
 * Computation issue: Using all the data for training  
 * Storage issue: Always keep the data  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/lll1.png)  
## Evaluation - LLL  
 * https://arxiv.org/pdf/1904.07734.pdf  
 * Accuracy, Backward transfer, Forward transfer  

## Research directions - Catastrophic forgetting  
## Selective Synaptic Plasticity - Regularization based Approach  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/lll2.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/lll3.png)  

## Additional Neural Resource allocation  
  * progressive NN -> the worse thing is to add NN infinity.  
  * PackNet -> the same idea with progressive NN  

## Memory reply  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/lll4.png)  
