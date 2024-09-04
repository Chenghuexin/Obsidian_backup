---
media: https://www.youtube.com/watch?v=hYdO9CscNes
---
# Self-attention

吃整個Sequence的資訊，輸入幾個向量，就會輸出幾個向量；輸出的向量皆是考慮過整個sequence才得到的


根據a1向量，考慮其他向量，其中哪個向量與a1是最有關連的，每一個向量與a1的關聯程度以α表示

如何自動決定向量之間的關聯性 :
dot-product(常見作法) : 
將比較的兩個向量分別乘上不同的矩陣，得到q、k兩個矩陣，再將q和k做dot-product，所得到的結果就是α

a