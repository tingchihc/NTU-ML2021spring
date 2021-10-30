# Transformer  

## Decoder - Autoregressive(AT)  

  * ex. Speech recognition:  
  * Input is Encoder's output.  
  * Input + BEGIN(special token) -> Decoder -> softmax -> output is a vector(size is vocabulary size)  
  * the output vector is a distribution and we will output the word of the highest value.  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/decoder.png)  
  
## Self-attention -> Masked Self-attention  
 * In the self-attention, the output vector(b1,b2,b3,b4) depend on the whole input vector(a1,a2,a3,a4).  
 * However, in the Masked self-attention, we only use the previous and present input to outrpur the vector.  
   * ex. (a1 -> b1) , (a1,a2 -> b2) , (a1,a2,a3 -> b3) , (a1,a2,a3,a4 -> b4).  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/maskedself-attention.png)  
 * We do not know the correct output length.  

## Tweet Solitaire  
 * How to stop the output vector? Ans: adding "Stop Token"  
 * "The Stop Token" is the one of the output in the distribution.  

## Decoder - Non-autoregressive(NAT)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/NAT.png)  

## Encoder-Decoder (two blue input is from encoder, one green input is from decoder)  
## The blue elements are k and v; the green element is q.  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/2b1g.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/crossattention.png)  

## Transformer - Training  

 * input: the acoustic signal with label.  
 * We need that Decoder output has the minimal loss(cross entropy) with ground truth.  

## Teacher Forcing: using the ground truth as input  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/groundtruth.png)  

## Here has a mismatch. In the training, we use the groud truth; however, in the testing(inference), we do not use the ground truth.  
## The mismatch is exposure bias  
  * Solution: scheduled sampling  

## The tips for training the transformer  
## Copy Mechanism  
  * in the Machine Translation, we will copy some words in the input.  
  * ex. Summarization: input(document) -> Model -> output(summary)  

## Guided Attention - Monotonic attention, Location-aware attention  
  * In some tasks, input and output are monotonically aligned.  
  * ex.: speech recognition, TTS, etc.  

## Beam Search  
  * Randomness is needed for decoder when generating sequence in some tasks.  
  * Accept that nothing is perfect. True beauty lies in the cracks of imperfection.  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/beamsearch02.png)  

## Optimizing Evaluation Metrics?  
  * In the training, we focus on the minimal loss(method is cross entropy).  
  * In the testing(inference), we use the output and ground truth to caculate BLEU score.  
  * The minimal cross entropy loss model does not have the great BLEU score in the testing.  

## So how to do the optimization? Ans: When you do not know how to optimize, just use RL!  

