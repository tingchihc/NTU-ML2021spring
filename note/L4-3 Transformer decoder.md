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
