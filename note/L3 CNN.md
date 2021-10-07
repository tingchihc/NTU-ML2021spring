Slide: https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/cnn_v4.pdf  
YT: https://www.youtube.com/watch?v=OP5HcXJg2Aw  

# Convolutional Neural Network(CNN)  

## Image Classification  

   * All the images to be classified have the same size. (ex. 100X100)  
   * input: image  
   * image -> model -> y'
   * <img src="https://latex.codecogs.com/svg.image?&space;y'\Leftrightarrow&space;&space;\hat{y}" title=" y'\Leftrightarrow \hat{y}" /> (make the lesser Cross entropy)  
   
## IN the computer, the image like ....

  * the image  is a 3-D tensor(Width, Height, Channels).  
  * one colorful image is represented by RGM(3 channels).  
  * To stretch the image to a vector, the value in the vector represents intensity.  

## Issue  
  * input: 100 X 100 X 3 value  
  * in the fully connected network, if we have 1000 neurons.  
  * We have 30000000 processes.  
  * !!!! Do we really need "fully connected" in image processing? Ans: NO.  

## Observation 1
  * A neuron does not have to see the whole image.  
  * Some patterns are much smaller than the whole image.  
  * ex: layer1(basic detector), layer2(advanced dector)...  
 
## Simplification 1
  * Setting a receptive field's range, we can use this range and neuron to observe specific pattern.  
  * Many neurons can use the same receptive field.  
  * Receptive field can overlapped.  
  * Issues:YES!!  
    * Can different neurons have different sizes of receptive field?  
    * Cover only some channels?  
    * Not square receptive field?  
