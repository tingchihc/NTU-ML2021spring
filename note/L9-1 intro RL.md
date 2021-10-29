## YT  
  * https://www.youtube.com/watch?v=XWukX-ayIrs  

## slide  
  * https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/drl_v5.pdf  

## Reinforcement Learning  
  * It is challenging to label data in some tasks.  
  * machine can know the results are good or not.  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/rl1.png)  

## RL like ML Steps:  
## 1) function with unknown  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/rl2.png)  
## 2) define loss from training data, Total reward(return) what we want to maximize  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/rl3.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/rl4.png)  
## 3) optimization  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/rl5.png)  

## Optimization -> policy gradient  
## How to control your actor  
  * make it take(or don not take) a specific action given specific observation.  
  * ex:  
  observation(s) -> Actor(<img src="https://latex.codecogs.com/svg.image?\theta&space;" title="\theta " />) -> Action a(left,right,fire) <-> <img src="https://latex.codecogs.com/svg.image?\hat{a}" title="\hat{a}" />  
  e = cross-entropy with <img src="https://latex.codecogs.com/svg.image?\left&space;(&space;a,\hat{a}&space;\right&space;)" title="\left ( a,\hat{a} \right )" />  
  Take action <img src="https://latex.codecogs.com/svg.image?\hat{a},L=e" title="\hat{a},L=e" />  
  Don't take action <img src="https://latex.codecogs.com/svg.image?\hat{a},L=-e" title="\hat{a},L=-e" />  
  <img src="https://latex.codecogs.com/svg.image?\theta&space;^{*}=arg\underset{\theta&space;}{min}L" title="\theta ^{*}=arg\underset{\theta }{min}L" />  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/rl6.png)  
