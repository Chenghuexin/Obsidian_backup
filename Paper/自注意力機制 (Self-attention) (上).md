---
media: https://www.youtube.com/watch?v=hYdO9CscNes
---
# Self-attention

吃整個Sequence的資訊，輸入幾個向量，就會輸出幾個向量；輸出的向量皆是考慮過整個sequence才得到的(同時計算ㄔㄨ)


## Step 1 :

> **考慮關聯性** : 根據a1向量，考慮其他向量，其中哪個向量與a1是最有關連的，每一個向量與a1的關聯程度以α(attention score)表示

> [!NOTE]
> 如何自動決定向量之間的關聯性 :
> - dot-product(常見作法) : 
> 將比較的兩個向量分別乘上不同的矩陣(Wq、Wk)，得到q、k兩個矩陣，再將q和k做dot-product，所得到的結果就是α
> 
> - additive
> 一樣跟dot-product先得到q、k矩陣後，將這兩個矩陣串接起來，經過activation function，再通過transform

實作 : a1乘上Wq得到query，其他向量乘上Wk得到key；接著query和不同的key做dot-product所得到的結果就是α(attention score)，另外query也會跟自己計算關聯性，也就是a1也會乘上Wk得到key，再做dot-product；完成上述步驟後會執行一次softmax

---
## Step 2 :

> **抽取重要資訊** : 將所有原輸入的向量乘上Wv向量得到V，接著再將對應的α'(經過softmax的α)和相對應的V相乘，再相加起來；如果a1和a2的關聯性較大，最後V相加的結果就會與α12相似