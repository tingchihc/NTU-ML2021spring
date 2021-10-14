# Slide:  
  * https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/normalization_v4.pdf  

# YT:  
  * https://www.youtube.com/watch?v=BABPWOkSbLE  

## Batch Normalization  
  * If the model has a error service, the batch normalization is a great method to use.  

## Feature Normalization  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/feature%20normalization.png)  
  

## Considering Deep Learning - Training  
 <img src="https://latex.codecogs.com/svg.image?\tilde{X^{1}}&space;\to&space;W^{1}\to&space;z^{1}\to&space;Sigmoid\to&space;a^{1}\to&space;W^{2}&space;..." title="\tilde{X^{1}} \to W^{1}\to z^{1}\to Sigmoid\to a^{1}\to W^{2} ..." />  
 * We need normalization in Z or a (depend on activation function)  
 <img src="https://latex.codecogs.com/svg.image?\gamma&space;" title="\gamma " /> is a all 1 vectore and <img src="https://latex.codecogs.com/svg.image?\beta&space;" title="\beta " /> is a all 0 vector in first step. This two vectors need to learn from model.  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/considering1.png)  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/considering2.png)  
