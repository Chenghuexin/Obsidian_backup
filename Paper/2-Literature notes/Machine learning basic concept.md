
# 訓練過程
## 1. Function

###### 以Linear model為例
![[Pasted image 20240812185440.png]]

|  w  |            weight             |
| :-: | :---------------------------: |
|  b  |             bias              |
|  y  | Model(with unknow parameters) |

## 2. Loss function
![[Pasted image 20240812185714.png|500]] 

![[Pasted image 20240812190619.png|500]]

- 輸出的值所代表的意思 :  設置的b和w表現是否好，數值越大代表與實際情況相差越大，越小代表越相似
- en有很多種方法 e.g. MAE、MSE、cross entropy
- **error Surface** : 嘗試不同的參數，算出其loss值，將其繪製成等高線圖

## 3. Optimization

![[Pasted image 20240812191302.png|500]]

- 找出能讓loss function最小的w和b
### 方法 一 : Gradient Descent

###### 以一個參數為舉例

*下圖為error surface*
![[Pasted image 20240813214122.png]]

![[Pasted image 20240812191722.png]]

![[Pasted image 20240812191808.png]]

![[Pasted image 20240812192229.png]]

- **learning rate** : 移動距離，為**hyperparameters**(需要自行設置的參數)
- 斜率為負代表左邊高(loss 高)右邊低(loss 低)，所以應該往右，以此類推
- 缺點 : 因為初始位置導致最後選出來的(local minima)可能不是真正的最佳解(global minima)

###### w、b
![[Pasted image 20240812193913.png]]

## 4. Linear model的缺點

![[Pasted image 20240812201427.png]]

不管參數怎麼調整，linear model始終是一條線的形式，但現實的狀況不一定只是一條線，我們永遠無法透過linear model成功模擬跟現實相符的形式，原因來自於model的限制(**Model's bias**)


## 5. 解決Linear model's bias

![[Pasted image 20240812201400.png]]

紅色曲線總共分成三段，我們可以透過**常數和藍色曲線**產生紅色曲線。
第一段藉由 0 + 1藍色曲線組成、第二段藉由0+1+2藍色曲線組成、第三段藉由0+1+2+3藍色曲線組成。
這種可以透過常數和藍色曲縣組成的曲線稱為 **All Piecewise Linear Curves**

- 如果今天是不是Piecewise Linear?
	e.g.
	![[Pasted image 20240812202005.png]]
	
	依然可以透過Piecewise linear curve去非常逼近
	![[Pasted image 20240812202047.png]]


### Sigmoid function
![[Pasted image 20240812202404.png]]

##### 透過更改b、w、c產生不同形狀的Sigmoid function
![[Pasted image 20240812202729.png]]

##### Hard Sigmoid
![[Pasted image 20240812202457.png]]
