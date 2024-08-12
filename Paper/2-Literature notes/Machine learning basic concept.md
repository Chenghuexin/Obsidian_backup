
# 訓練過程
## 1. Function

###### 以Linear model為例
![[Pasted image 20240812185440.png]]

- w : weight
- b : bias
- y : Model(with unknown parameters)

## 2. Loss function
![[Pasted image 20240812185714.png|500]] 

![[Pasted image 20240812190619.png|500]]

- 輸出的值所代表的意思 :  設置的b和w表現是否好，數值越大代表與實際情況相差越大，越小代表越相似
- en有很多種方法 e.g. MAE、MSE、cross entropy
- **error Surface** : 嘗試不同的參數，算出其loss值，將其繪製成等高線圖

## 3. Optimization

![[Pasted image 20240812191302.png|500]]

- 找出能讓loss function最小的w和b
### Gradient Descent

###### 以一個參數為舉例
![[Pasted image 20240812191722.png]]

![[Pasted image 20240812191808.png]]

![[Pasted image 20240812192229.png]]

- learning rate : 移動距離，為**hyperparameters**(需要自行設置的參數)
- 斜率為負代表左邊高(loss 高)右邊低(loss 低)，所以應該往右，以此類推
- 缺點 : 因為初始位置導致最後選出來的(local minima)可能不是真正的最佳解(global minima)

###### w、b
![[Pasted image 20240812193913.png]]

