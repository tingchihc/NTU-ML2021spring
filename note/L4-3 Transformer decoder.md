# Transformer  

## Decoder - Autoregressive(AT)  

  * ex. Speech recognition:  
  * Input is Encoder's output.  
  * Input + BEGIN(special token) -> Decoder -> softmax -> output is a vector(size is vocabulary size)  
  * the output vector is a distribution and we will output the word of the highest value.  
  * 
