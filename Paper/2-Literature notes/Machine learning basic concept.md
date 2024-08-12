
## 1. Function

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

![[Pasted image 20240812191722.png]]

![[Pasted image 20240812191808.png]]

- learning rate : 移動距離，為hyperparameters(需要自行設置的參數)