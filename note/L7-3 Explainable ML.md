## YT  
  * https://www.youtube.com/watch?v=WQY85vaQfTI  

## Slide  
  * https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/xai_v4.pdf  

## Explainable Machine Learning  
## Local explanation V.S. Global explanation  
  * local explanation: why do you think this img is a cat?  
  * global explanation: what does a "cat" look like?  

## Local explanation -> which component is critical?  
  * object x -> image, text, etc.  
  * components: {x1,x2,...xn}  
  * Method:  
    * Removing or modifying the components  
    * Large decision change -> important component  

## Saliency map  
  * the light dot in the image can represent which parts are important in the image.  

## Limitation: noisy gradient  
  * SmoothGrad: Randomly add noises to the input image, get saliency maps of the noisy images, and average them.  

## Limitation: gradient saturation  
  * Gradient cannot always reflect importance  
  * Alternative: Integrated gradient(IG)  

## How a network processes the input data?  
  * visualization  
  * proding  
