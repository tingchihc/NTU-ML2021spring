## YT  
  * https://www.youtube.com/watch?v=xoastiYx9JU  
  * https://www.youtube.com/watch?v=Q68Eh-wm1Ts  

## slide  
  * https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/meta_v3.pdf  

## Meta Learning  
## Can machine automatically determine the hyperparameters?  
  * What is learnable in a learning algorithm?  
  * Component: Net Architecture, Initial Parameters, Learning Rate  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/meta1.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/meta2.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/meta3.png)  
## How can we know a classifier is good or bad? Evaluate the classifier on testing set  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/meta4.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/meta5.png)  
## In meta, you compute the loss based on testing examples of training tasks  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/meta6.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/meta7.png)  
## Goal -> ≈ find a function F that finds a function f  
## Support set -> the training data in training tasks, Query set -> the testing data in training tasks  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/meta8.png)  
