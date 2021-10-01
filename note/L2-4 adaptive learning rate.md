slide: https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/optimizer_v4.pdf

## Training stuck != Small Gradient

  * Training can be difficult even without critical points.  
  * Learning rate cannot be one-size-fits-all.  

## 1. Different parameters needs different learning rate  

  * Used in Adagrad  

<img src="https://latex.codecogs.com/svg.image?\theta&space;_{i}^{t&plus;1}\leftarrow&space;\theta&space;_{i}^{t}-\frac{\eta&space;}{\sigma&space;_{i}^{t}}g_{i}^{t}" title="\theta _{i}^{t+1}\leftarrow \theta _{i}^{t}-\frac{\eta }{\sigma _{i}^{t}}g_{i}^{t}" />  

<img src="https://latex.codecogs.com/svg.image?\sigma&space;_{i}^{t}&space;=&space;\sqrt{\frac{1}{t&plus;1}\sum_{i=0}^{t}\left&space;(g&space;_{i}^{t}&space;\right&space;)^{2}}" title="\sigma _{i}^{t} = \sqrt{\frac{1}{t+1}\sum_{i=0}^{t}\left (g _{i}^{t} \right )^{2}}" />  

 
 Smaller <img src="https://latex.codecogs.com/svg.image?\sigma&space;_{i}^{t}&space;" title="\sigma _{i}^{t} " /> larger step  
 
 Larger <img src="https://latex.codecogs.com/svg.image?\sigma&space;_{i}^{t}&space;" title="\sigma _{i}^{t} " /> smaller step  

## 2. RMSProp  

  * Slide p.9  
  * designer can adjust the parameters to dependent on the importance.  
  * We can dynamically adjust the parameters when the gradient has large influence or less influence.  

## 3. Adam: RMSProp + Momentum

  * ref.: https://arxiv.org/pdf/1412.6980.pdf  

## 4. Learning Rate Scheduling  

  * Learning rate decay  
    * As the training goes, we are closer to the destination, so we reduce the learning rate.  
  * Warm up  
    * increase and then decrease?  
  
  Residual Network (ref. heeps://arxiv.org/abs/1512.03385)  
  Transformer (ref. https://arxiv.org/abs/1706.03762)  
