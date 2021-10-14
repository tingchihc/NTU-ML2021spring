# Slide:  
  * https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/seq2seq_v9.pdf  
# YT:  
  * https://www.youtube.com/watch?v=n9TlOhRjYoc  
  * https://www.youtube.com/watch?v=N6aRv06iv2g  
 
 ## Transformer  
 
  * Transformer is a Sequence-to-sequence(seq2seq) model.  
  * input: a sequence. output: a sequence.  
  * The output length is determined by model.  
  * Applications: Speech Recognition, Machine Translation and Speech Translation(Language without text).  

## Seq2seq2 for Chatbot  

 * input -> seq2seq2 -> response  

## Most Natural Language Processing applications...

 * most applications is Question Answering(QA)  
 * QA can be done by seq2seq2.  
 * ex. question, context -> seq2seq2 -> answer  
 * ref.: https://arxiv.org/abs/1806.08730 , https://arxiv.org/abs/1909.03329  
 * Applications:  
   * Sentiment analysis  
   * Write the abstract  
   * Language translation  
   * ...  
   
## seq2seq for Syntactic Parsing  
 * ref. Grammar as a Foreign Language  
 * ex.  
 * model input: deep learning is  very powerful.  
 * model output: (S (NP deep learning) (VP is (ADJV very powerful) ) )  

## seq2seq for multi-label classification  
 * an object can belong to multiple classes.  

## seq2seq for object detection  
 * ref. https://arxiv.org/abs/2005.12872  

## seq2seq overview  
 * input(sequence) -> Encoder -> Decoder -> output(sequence)  
 
