## YT  
  * https://www.youtube.com/watch?v=xGQKhbjrFRk  
## Slide  
  * https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/attack_v3.pdf  

## Adversarial Attack  
## Motivation -> Are networks robust to the inputs that are built to fool them?  

## Example of attack: 1. Non-targeted: anything other than "cat" 2. Targeted: misclassified as a specific class  

  * Normal: benign img -> Network(image classifier) -> output(cat)  
  * Attack: attacked img(benign img + small noisy) -> Network(image classifier) -> output(not cat)  

## How to attack  
  * x is close with x0 and humans can not perceive the distance.  
  * y is as far as y(head) and as close as y(target).  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/how%20to%20attack.png)  
