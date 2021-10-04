## This note can help me finish HW2.  

## The lecture video is from prof. Hung-yi Lee.(DLHLP 2020) Speech Recognition  

  * YT: https://www.youtube.com/watch?v=AIKu43goh-8  
  * Slide: https://speech.ee.ntu.edu.tw/~tlkagk/courses/DLHLP20/ASR%20(v12).pdf  

## note  

  * speech -> speech recognition -> text  
  * input: speech  
  * output: text  
  * speech is a sequence of vector(length T, dimension D)  
  * text is a sequence of token(length N, V different tokens)  
  * Usually T > N  

## Token  

  * phoneme: a unit of sound  
    * ex: w ah n p ah n ch m ae  
    * Lexicon: word to phonemes  
    * ex: cat -> k ae t  
  * Grapheme: smallest unit of a writing system(Lexicon free)  
    * ex: 26 English alphabet + {_}(space) + {punctuation marks}  
    * one_punch_man -> N=13,V=26?  
  * Word: for some languages, V can be too large  
  * Morpheme: the smallest meaningful unit(<word, >grapheme)  
    * unbreakable -> "un" , "break" , "able"  
    * To find Morphemes in a language with linguistic or statistic  
  * Bytes(!): the system can be language independent  
    * ex: UTF-8 (V is always 256)  

# The main speech recognition method is GRAPHEME. #  

## input: acoustic feature(length T, dimension D)  

  * First, extracting a window(25ms), we will call that this featured window is frame.  
    * ex: 39-dim MFCC, 80-dim filter bank output  
  * Second, move the window(1st window:0->25ms , 2nd window:10ms->35ms). In one second, we have 100 frames.  

## Acoustic Feature example. Slide. p12  

  * input: weaveform  
  * weaveform(one window) -> Discrete Fourier Transform(DFM) -> spectrogram  
  * spectrogram -> filter bank -> vector  
  * vector -> log -> Discrete Cosine Transform(DCT) -> MFCC  

## in 2019, filter bank output is the main method.  
## Two points of views  
 
 * seq-to-seq  
 * HMM  

# Models to be introduced #  

## Listen, Attend, and Spell(LAS)  

 * Listen -> Encoder, Spell -> Decoder (It is the typical seq2seq with attention.)  
 
 ## In the Listen part, we will extract content information, remove speaker variance and remove noises.  
 * input -> {x1,x2,x3,...,xn} acoustic features  
 * output -> {h1,h2,h3,...,hn} high-level representations  
 * Listen - Down Sampling: to resample in a multi-rate digital signal processing system.  
 * Down Sampling methods: Time-delay DNN, Truncated Self-attention  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/listen(CNNRNN).png)  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/listen(selfattention).png)  

## In the Attention part  
 * vector: z0(keyword)  
 * encoder output: h(database)  
 * function match: input(z0,h) , output(alpha(^1,_0))  
 * Attention methods: Dot-product attention and Additive attention.  
 * C0: Context vector  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/dot%20attention.png)
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/additive%20attention.png)  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/attention.png)

## In the Spell part
 ![Image of Yaktocat]()
 ![Image of Yaktocat]()
 ![Image of Yaktocat]()
 ![Image of Yaktocat]()
