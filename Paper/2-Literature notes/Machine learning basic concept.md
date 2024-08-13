---
tags:
  - ML
  - DL
---

# 訓練過程
## Step 1 : Function

###### 以Linear model為例
![[Pasted image 20240812185440.png]]

|  w  |            weight             |
| :-: | :---------------------------: |
|  b  |             bias              |
|  y  | Model(with unknow parameters) |

## Step 2 : Loss function
![[Pasted image 20240812185714.png|500]] 

![[Pasted image 20240812190619.png|500]]

- 輸出的值所代表的意思 :  設置的b和w表現是否好，數值越大代表與實際情況相差越大，越小代表越相似
- en有很多種方法 e.g. MAE、MSE、cross entropy
- **error Surface** : 嘗試不同的參數，算出其loss值，將其繪製成等高線圖

## Step 3 : Optimization

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

紅色曲線可以分成三段，我們可以透過**常數和藍色曲線**(如上圖)產生紅色曲線。
第一個轉折點前可藉由 0 + 1藍色曲線組成、第二個轉折點前可藉由0+1+2藍色曲線組成、最後由0+1+2+3藍色曲線組成。
- **Piecewise Linear Curves** : 由很多個鋸齒狀線段組成的

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


## 6. 改寫 (linear -> sigmoid)

![[Pasted image 20240813222849.png]]

![[Pasted image 20240813222950.png]]
![[Pasted image 20240813223040.png]]
![[Pasted image 20240813223138.png]]
![[Pasted image 20240813223214.png]]

![[Pasted image 20240813222416.png]]![[Pasted image 20240813223244.png]]
- θ : 所有未知參數放在一起

# after adjustment
## Step 1 : function with unknown function

origin : [[#Step 1 Function]]
![[Pasted image 20240813223815.png]]

## Step 2 : Loss function L(θ)
![[Pasted image 20240813224634.png]]

## Step 3 : Optimization
![[Pasted image 20240813225651.png]]

![[Pasted image 20240813230010.png]]
實際上我們在訓練的過程會將所有的未知參數分成好幾個**batch**，透過每一個batch去更新參數值，等到所有的batch都跑過一遍之後，代表完成了1次**epoch**
- batch size : hyperparameter
- epoch : hyperparameter

##  Relu
![[Pasted image 20240813230742.png]]

