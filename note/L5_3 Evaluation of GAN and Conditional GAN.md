# YT  
  * https://www.youtube.com/watch?v=MP0BnVH2yOo  


## Evaluation of Generation  
## Quality of Image  

 * How to evaluate the quality of the generated images automatically?  Ans: image classifier(inception net, VGG)  
 * ex: y(image) -> off-the-shelf image classifier -> p(c|y) [Concentrated distribution means higher visual quality]  

## Problem of evaluation - Diversity - mode collapse  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/mode%20collapse.png)  

## Problem of evaluation - Diversity - mode dropping  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/mode%20dropping.png)


## Frechet Inception Distance(FID)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/FID.png)  

## Conditional Generation  

 * x(condition) + z(distribution) -> Generator -> y(complex distribution)  
 * application: Text-to-image(need label data)  
![Image of Yaktocat]
