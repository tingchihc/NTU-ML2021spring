slide: https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/overfit-v6.pdf

# Framework ML

* Training data: <img src="https://latex.codecogs.com/svg.image?\left\{(x_{1},\hat{y_{1}}),&space;(x_{n},\hat{y_{n}})\right\}" title="\left\{(x_{1},\hat{y_{1}}), (x_{n},\hat{y_{n}})\right\}" />  
* Testing data: <img src="https://latex.codecogs.com/svg.image?\left\{x_{n&plus;1},x_{n&plus;m}\right\}" title="\left\{x_{n+1},x_{n+m}\right\}" />  
  
*  Speech recognition, Image recognition, Speaker recognition, Machine translation  

* Step1. function with unknown  
  * <img src="https://latex.codecogs.com/svg.image?y&space;=&space;f_{\theta&space;}^{}(x)" title="y = f_{\theta }^{}(x)" />  
  * theta means all unknown parameters  

* Step2. define loss function  
  * <img src="https://latex.codecogs.com/svg.image?L(\theta&space;)" title="L(\theta )" />  

* Step3. optimization  
  * <img src="https://latex.codecogs.com/svg.image?\theta&space;_{}^{*}&space;=&space;arg&space;\underset{\theta&space;}{min}L" title="\theta _{}^{*} = arg \underset{\theta }{min}L" />  
  *  find the min theta to optimize   

* Use theta star to label the testing data

# How to check and optimize ML?  

## 1. General guide
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/general%20guide.png)  
  
  
## 2. Model bias
  * The model is too simple. None of one function can reduce loss function.  
  * Solution: redesign your model model to make it more flexible.  
  * Deep Learning (more neurons, layers, features)
  
## 3. Optimization Issue
  * Large loss not always imply model bias. for example: gradient descent local minimum problem

## 4. How can I know that model has model bias problem or optimization problem?  
  * ref. http://arxiv.org/abs/1512.03385  
  * If deeper networks do not obtain smaller loss on training data, then there is optimization issue.  
  * Solution: more powerful optimization technology  

## 5. Overfitting
  * loss in training data is small but in testing data is large  
  * Solution:  
    * 1. more training data  
    * 2. data augmentation  
    * 3. constrained model  

 | methods | example |
| ------- | ------- |
|  1. less parameters, sharing parameters |ex: fully-connected, CNN |
| 2. less features | |
| 3. early stopping ||
|4. regularization  |  |
| 5. dropout  |  |
    
  * If contrain too much, back to model bias  

## 6. Cross Validation
  * To split the training set into two groups: training set and validation set  
  * Using the results of public testing data to select your model  
  * method: N-fold Cross Validation:  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/n-fold%20cross%20validation.png)  

## 7. Mismatch  
  * your training and testing data have different distributions.  
  * *Be aware* of how data is generated.  
