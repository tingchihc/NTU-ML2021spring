# Self-attention  
  
  <img src="https://latex.codecogs.com/svg.image?b^{2}&space;=&space;\sum_{i}^{}\alpha'_{2,i}\nu&space;^{i}" title="b^{2} = \sum_{i}^{}\alpha'_{2,i}\nu ^{i}" />  
  
  * output: {b1, b2, b3, b4} -> parallel  

## Compute with Matrix
## Use training data to learn the parameters(<img src="https://latex.codecogs.com/svg.image?W^{q},W^{v},W^{k}" title="W^{q},W^{v},W^{k}" />)  

  * Matrix I: input(a1,a2,a3,a4)  
  * Matrix Q: query(q1,q2,q3,q4)  
  * Matrix K: key(k1,k2,k3,k4)  
  * Matrix v: V(v1,v2,v3,v4)  
  * Matrix A: Attention Matrix <img src="https://latex.codecogs.com/svg.image?\left&space;(\alpha(1,1),&space;...,&space;&space;\alpha(4,4)&space;&space;\right&space;)" title="\left (\alpha(1,1), ..., \alpha(4,4) \right )" />  
  * Matrix O: output(b1,b2,b3,b4)  
  
  * Step1:  
    * Use a1 to compute (q1,k1,v1), Use a2 to compute (q2,k2,v2)...  
    * <img src="https://latex.codecogs.com/svg.image?q^{i}=w^{q}a^{i}" title="q^{i}=w^{q}a^{i}" />  
    * <img src="https://latex.codecogs.com/svg.image?k^{i}=w^{k}a^{i}" title="k^{i}=w^{k}a^{i}" />  
    * <img src="https://latex.codecogs.com/svg.image?v^{i}=w^{v}a^{i}" title="v^{i}=w^{v}a^{i}" />  
  
  * Step2:  
    * Usa k1 and q1 to compute <img src="https://latex.codecogs.com/svg.image?\alpha(1,1)&space;" title="\alpha(1,1) " />...  
    * <img src="https://latex.codecogs.com/svg.image?\alpha(1,1)&space;=&space;k_{1}^{T}q_{1}" title="\alpha(1,1) = k_{1}^{T}q_{1}" />  
    * <img src="https://latex.codecogs.com/svg.image?\alpha(1,2)&space;=&space;k_{2}^{T}q_{1}" title="\alpha(1,2) = k_{2}^{T}q_{1}" />  
    * <img src="https://latex.codecogs.com/svg.image?\alpha(1,3)&space;=&space;k_{3}^{T}q_{1}" title="\alpha(1,3) = k_{3}^{T}q_{1}" />  
    * <img src="https://latex.codecogs.com/svg.image?\alpha(1,4)&space;=&space;k_{4}^{T}q_{1}" title="\alpha(1,4) = k_{4}^{T}q_{1}" />  
  
  * Step3:  
    * A = Transformation matrix(K) * Q  
    * A -> softmax -> <img src="https://latex.codecogs.com/svg.image?A^{'}" title="A^{'}" />  
    * <img src="https://latex.codecogs.com/svg.image?A^{'}" title="A^{'}" /> * V = O  

## Multi-head self-attention (Different types of relevance)  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sa27.png)
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sa28.png)

## Positional Encoding  
  * No position information in self-attention.  
  * Each position has a unique positional vector <img src="https://latex.codecogs.com/svg.image?e^{i}" title="e^{i}" />  
  * hand-crafted  
  * learned from data  
  * <img src="https://latex.codecogs.com/svg.image?e^{i}&plus;a^{i}&space;\rightarrow&space;q^{i},k^{i},v^{i}" title="e^{i}+a^{i} \rightarrow q^{i},k^{i},v^{i}" />  

## Many applications...  
  * Transformer, ref.: https://arxiv.org/abs/1706.03762  
  * BERT, ref.: https://arxiv.org/abs/1810.04805  
  * Natural Langue Processing(NLP)  

## Self-attention for Speech  
  * Truncated self-attention -> attention in arange  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sa32.png)  
  
## Self-attention for image  
* an image can also be considered as a vector set.  
* example:  
  * self-attention GAN ref.: https://arxiv.org/abs/1805.08318  
  * DEtection transformer(DETR) ref.: https://arxiv.org/abs/2005.12872  

## Self-attention V.S. CNN  
* ref.: https://arxiv.org/abs/1911.03584  
* CNN: self-attention that can only attends in a receptive field.  
* CNN is a simplified self-attention.  
* Self-attention: CNN with learnable receptive field.  
* Self-attention is the complex version of CNN.  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sa36.png)  
