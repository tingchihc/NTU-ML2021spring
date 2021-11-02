## YT  
  * https://www.youtube.com/watch?v=utk3EnAUh-g  
  * https://www.youtube.com/watch?v=xrlbLPaq_Og  

## slide  
  * https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/tiny_v7.pdf  

## Network Compression  
  * Less parameters  
  * latency, Privacy  

## 1) Network pruning  
  * Networks are typically over-parameterized (there is significant redundant weights or neurons)  
  * (1. importance of weight, (2. importance of a neuron, (3. fine-tuning  
  * Pre-trained Network(large) -> Evaluate the importance -> Remove(smaller) -> Fine-tune -> small enough? -> Evalute? -> smaller network  
  * Weight pruning:  
    * hard to implement, hard to speedup  
  * Neuron pruning:
    * easy to implement, easy to speedup  

## Lottery Ticket Hypothesis  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/lottery.png)  
 
 
## 2) Knowledge distillation  
  * make student Net to like teacher Net's output  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/knowledge%20distillation1.png)  
  * Temperature for softmax:  this can make model know the distribution  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/kd2.png)  

## 3) Parameter quantization  
  * Using less bits to represent a value  
  * Weight clustering: to make each weights in a network has alike weight.  Maybe save weight in Table.  

## 4) Architecture Design -> Depthwise Separable Convolution  
  * Depthwise -> Pointwise
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/ds1.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/ds2.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/ds3.png)  

## 5) Dynamic Computation -> Dynamic Width, Dynamic Depth  
  * The network adjusts the computation it need  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/dd1.png)  
