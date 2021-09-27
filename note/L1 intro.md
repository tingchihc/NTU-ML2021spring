# Different types of functions:  

* Regression: the function outputs a scalar.  
the example about to predict PM2.5:  
  input: PM2.5, temperature and concentration of o3  
  output: PM2.5 of tomorrow  
  
* Classification: given options(classes), the function outputs the correct one.  
the example about to spam filtering:  
  input: email  
  output: yes/no  

* and more(structured learning...)  

# How to find a function?  

## 1. function with unknown parameters
  * y = f(x) = b + w*x1 (based on domain knowledge)
  * w and b are unknown parameters(learning from data)  
  * Model = y
  * feature = x1
  * weight = w
  * bias = b
  
## 2. Define Loss from Training Data
  * Loss: how good a set of values is.
  * Loss is a function of parameters. for example: L(b,w)  
  * L(0.5k,1): y = b + w*x1 -> y = 0.5k + 1*x1
  * notation: y = the predicted value, label: <img src="https://latex.codecogs.com/svg.image?\hat{y}" title="\hat{y}" /> = the true value, 
  * <img src="https://latex.codecogs.com/svg.image?^{e_{1}}" title="^{e_{1}}" /> = <img src="https://latex.codecogs.com/svg.image?\hat{y}" title="\hat{y}" /> - y
  * functions to get e: mean absolute error, mean square error, and cross-entropy
  * Loss function: 1/N * Sigma(<img src="https://latex.codecogs.com/svg.image?^{e_{n}}" title="^{e_{n}}" />)

## 3. Optimization
  * find w, b to minimize loss function  
  * function:  
    * Gradient Descent: <img src="https://latex.codecogs.com/svg.image?w^{1}&space;{\leftarrow}&space;w^{0}&space;-&space;\eta&space;\frac{\partial&space;L&space;}{\partial&space;W}&space;\mid&space;w&space;=&space;w^{0}" title="w^{1} {\leftarrow} w^{0} - \eta \frac{\partial L }{\partial W} \mid w = w^{0}" />
    * <img src="https://latex.codecogs.com/svg.image?\eta" title="\eta" /> = learning rate  
    
## Training = step1 + step2 + step3
  * Linear models: y = b + Sigma(W*X)  
  * Linear models have severe limitation. -> **Model Bias**
