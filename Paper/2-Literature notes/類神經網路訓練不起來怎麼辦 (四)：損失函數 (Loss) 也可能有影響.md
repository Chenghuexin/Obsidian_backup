---
media: https://www.youtube.com/watch?v=O2VkP8dJ5FE
---
承上回 : [[類神經網路訓練不起來怎麼辦 (三)：自動調整學習速率 (Learning Rate)]]

# 分類的小問題

當 1 = class 1, 2 = class 2, 3 = class 3；這樣的表示方法會導致class 1 和 class 2 比較相似，class 1 和 class 3 比較不一樣，在某些情況下會有問題。

# Class as one-hot vector

這種方法可以避免class之間有相似性的問題


- [05:17](https://www.youtube.com/watch?v=O2VkP8dJ5FE&t=317#t=05:17.14) 輸出

# Softmax


- [06:15](https://www.youtube.com/watch?v=O2VkP8dJ5FE&t=376#t=06:15.95) 原本的輸出(logit)會再經過一個softmax才會是最後的結果

- [08:47](https://www.youtube.com/watch?v=O2VkP8dJ5FE&t=527#t=08:47.20) 公式

# Loss of Classification

## Mean Square Error(MSE)


- [11:21](https://www.youtube.com/watch?v=O2VkP8dJ5FE&t=681#t=11:21.28) 


## Cross-entropy


- [12:09](https://www.youtube.com/watch?v=O2VkP8dJ5FE&t=730#t=12:09.53) 

- [13:08](https://www.youtube.com/watch?v=O2VkP8dJ5FE&t=788#t=13:08.09) Minimizing cross-entropy is equivalent to maximizing likelihood