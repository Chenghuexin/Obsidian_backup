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