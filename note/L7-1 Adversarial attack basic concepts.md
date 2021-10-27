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

## Non-perceivable  

  * The smaller L-infinity is hard to notice; the larger L-infinity is easy.  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/non-perceivable.png)  

## Attack approach  
<img src="https://latex.codecogs.com/svg.image?x^{*}&space;=&space;arg&space;\underset{d(x^{0},x)\leq&space;\varepsilon&space;}{min}&space;L(x)" title="x^{*} = arg \underset{d(x^{0},x)\leq \varepsilon }{min} L(x)" />  

## Method 1: Gradient Descent and L-infinity  
  * Start from original image x  
  * For t = 1 to T  
  * <img src="https://latex.codecogs.com/svg.image?x^{t}&space;\leftarrow&space;x^{t-1}-\eta&space;g" title="x^{t} \leftarrow x^{t-1}-\eta g" />  
  * if <img src="https://latex.codecogs.com/svg.image?d(x^{0},x^{t})&space;>&space;\varepsilon&space;,&space;x^{t}&space;\leftarrow&space;fix(x^{t})" title="d(x^{0},x^{t}) > \varepsilon , x^{t} \leftarrow fix(x^{t})" />  
