slide p.17: https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/small-gradient-v7.pdf

## Review: Optimization with Batch

![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/batch.png)  

## 1. Small Batch & Large Batch

  * Consider 20 examples(N=20)
  
  |Batch size = N(Full batch)|Batch size = 1|
  |--------------------------|--------------|
  |See all examples          |See only one example|
  |Long time for cooldown, but powerful|Short time for cooldown, but noisy|
  
  ```diff
  - Large batch size does not require longer time to compute gradient(unless batch size is too large)

  ```
