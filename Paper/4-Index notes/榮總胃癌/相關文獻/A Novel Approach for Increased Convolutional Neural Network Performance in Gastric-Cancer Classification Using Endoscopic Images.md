---
tags:
  - Augmentation
  - CADx
  - gastric_cancer
  - segmentation
refernece: https://ieeexplore.ieee.org/document/9389708
---
# SEGMENTATION METHOD: SLIC SUPERPIXEL
+ fast clustering method
+ clustering is performed using only cluster information within a certain area without requiring the entire image’s cluster information.
+ the pixels in the image are clustered into **k superpixels** using the same procedure

> [!NOTE] SuperPixel
> 有意義的像素群
> 優點 : 通常會「順著物體的輪廓」

### 前置處理
+ 改顏色空間：RGB → CIELAB
	+ CIELAB「比較接近人眼感受」的均勻色差
+ 用 1D kernel 算梯度
+ 在每個初始中心周圍 3×3 區域裡，找「梯度最小」的位置(最不像邊界的位置)，把中心移過去
### 定義顏色距離 dc
**dc = pixel i 與 cluster j 在 CIELAB 顏色空間的歐氏距離**  
→ 顏色越相似，dc 越小。

### 定義空間距離 ds
**dc = pixel i 與 cluster j 在 CIELAB 顏色空間的歐氏距離**  
→ 顏色越相似，dc 越小。