---
media: https://www.youtube.com/watch?v=BABPWOkSbLE
---
承上回 : [[類神經網路訓練不起來怎麼辦 (四)：損失函數 (Loss) 也可能有影響]]

# Changing Landscape

## error surface過於崎嶇導致訓練效果不好

## 導致error surface崎嶇的原因 : 

- 特徵跟特徵之間的數值範圍差距過大

# 解決方法 ─ Feature Normalization

解決特徵與特徵之間數值範圍差距過大的問題

## standardlization 


- [07:19](https://www.youtube.com/watch?v=BABPWOkSbLE&t=440#t=07:20.00) 公式解釋，做完normalization之後的好處是所有的特徵加總平均為0，變異數(variance)皆為1

# Normalization後經過某個layer之後的值也需要做Normalization 

- [10:00](https://www.youtube.com/watch?v=BABPWOkSbLE&t=600#t=10:00.15) 

## Batch Normalization

只做一個batch裡面的normalization


- [18:33](https://www.youtube.com/watch?v=BABPWOkSbLE&t=1114#t=18:33.55) 避免做完normalization後平均都是0，可能會給network一些限制導致有負面的影響，所以加上參數讓調整分布

# Testing

在做batch normalization時是透過一整個batch算出μ和σ，如果今天在測試時你只有丟一筆資料進去測試的話根本無法得到這兩個參數
