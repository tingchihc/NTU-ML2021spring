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
