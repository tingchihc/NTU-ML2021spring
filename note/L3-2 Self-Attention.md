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
