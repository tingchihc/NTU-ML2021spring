Slide: https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/self_v7.pdf  
YT: https://www.youtube.com/watch?v=hYdO9CscNes  
YT: https://www.youtube.com/watch?v=gmsMY5kc-zw  

# Self-attention  

## Issue  

   * input is a vector  
      * vector -> model -> scalar or class  
   * input is a set of vectors  
      * vectors(may change length) -> model -> scalars or classes  
    
## Vector set as Input  

   * Such as: acoustic signal, graph  
   * ex.: this is a cat. Every word is a vector.  
   * How to make a word become a vector? 2 methods  
      * One-hot Encoding  
      * Word Embedding  
   
    
## What is the output?  

  * Each vector has a label.  
  * (1) {X1, X2,X3, X4} -> Model -> {Y1, Y2, Y3, Y4}  
  * Example applications:  
    * POS tagging  
    * acoustic signal  
    * social network  

  * (2) {X1, X2, X3, X4} -> Model -> Y  
  * Example applications:  
    * Sentiment analysis  
    * Recognize speaker  
    * Graph(hydrophilicity)  
  
  * (3) Model decides the nember of labels itself.  
  * Example: seq2seq  

## Sequence Labeling  

  * Issues: the window can not cover the bigger or smaller sequences simultaneously.  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sequencelabeling.png)  

## Self-attention  
## Overview  

* Papaer [Attention is all you need] https://arxiv.org/abs/1706.03762  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/selfattention.png)  
## How does the model operate in the Self-attention  Slide: p.13-p.18

  * Step1: Find the relevant vectors in a sequence  
  * Step2: Use Dot-product, Additive or more methods to compute the relevant vector  
  * Step3: Compute the query, key and attention score  
  * Step4: Use activation function(Soft-max, ReLu ...)  
  * Step5: Extract information based on attention scores  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sa13.png)
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sa14.png)
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sa15.png)
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sa16.png)
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sa17.png)
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/sa18.png)
