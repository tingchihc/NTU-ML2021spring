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
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/simplification1.png)  

## Typical Setting  
  * all channels  
  * kernel size means Width X Height  
  * stride means that the moving step(We do not hope the bigger stride because we need the overlapping receptive field)  
  * padding means that add the value in the none value of receptive field.  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/typical%20setting.png)  

## Observation 2
  * the same patterns appear in different regions.  
  * Does each receptive field need a "beak" detector?  

## Simplification 2 (parameter sharing)  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/simplification2.png) 

## Typical Setting  
  * filter means the parameter.  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/filter.png) 

# Benefit of Convolutional Layer  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/benefitof%20CNN.png) 

# Another story about filter  
  * one Convolution has a lot of filters(each filter detects a small pattern. ex: 3*3*channel) channel 3 = colorful, channel 1 = black and white  
  * !! The values in the filters are unknown parameters. (Use gradient descent to compute)  
  * ex:  
    * image -> Convolution(64 filters) -> Feature Map(image with 64 channels)  
    * Feature Map(image with 64 channels) -> Convolution(3*3*64 filters) -> ....  

# Comparison of TWO stories  
  * Neuron Version:  
    * Each neuron only considers a receptive field.  
    * The neurons with different receptive fields share the parameters.  
  * Filter Version:  
    * There are a set fo filters detectiong small patterns.  
    * Each filter convolves over the input image.  
  ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/comparison.png) 
