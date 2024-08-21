---
media: https://www.youtube.com/watch?v=Dr-WRlEFefw
---

# 3 Steps
## Step 1 : define a set of function
## Step 2 : goodness of function

## Step 3 : pick the best function

# Fully Connect Feedforward Networ

- ![[ML Lecture 6_ Brief Introduction of Deep LearningPT13M18.517S.webp|ML Lecture 6: Brief Introduction of Deep Learning - 13:18|50]] [13:18](https://www.youtube.com/watch?v=Dr-WRlEFefw&t=799#t=13:18.52) 每一個neural都有一組weight和一組bias(weight和bias是透過訓練找出來的)
- ![[ML Lecture 6_ Brief Introduction of Deep LearningPT14M53.878S.webp|ML Lecture 6: Brief Introduction of Deep Learning - 14:53|50]] [14:53](https://www.youtube.com/watch?v=Dr-WRlEFefw&t=894#t=14:53.88) 一個neural network可以視為一個function
- ![[ML Lecture 6_ Brief Introduction of Deep LearningPT17M21.058S.webp|ML Lecture 6: Brief Introduction of Deep Learning - 17:21|50]] [17:21](https://www.youtube.com/watch?v=Dr-WRlEFefw&t=1041#t=17:21.06) 兩個layer之間的neuron是互相連接的，所以稱為**Fully Connect**，又因為傳遞方向為由後往前(layer 1 -> layer2 -> layer3)，所以稱為**Feedforward**
- ![[ML Lecture 6_ Brief Introduction of Deep LearningPT18M49.002S.webp|ML Lecture 6: Brief Introduction of Deep Learning - 18:49|50]] [18:49](https://www.youtube.com/watch?v=Dr-WRlEFefw&t=1129#t=18:49.00) layer 名稱
- ![[ML Lecture 6_ Brief Introduction of Deep LearningPT25M45.343S.webp|ML Lecture 6: Brief Introduction of Deep Learning - 25:45|50]] [25:45](https://www.youtube.com/watch?v=Dr-WRlEFefw&t=1545#t=25:45.34) 一個neural network做的事情實際上就是一連串的vector乘上matrix，再加上vector，將之寫成矩陣運算的好處是可以使用GPU加速
- ![[ML Lecture 6_ Brief Introduction of Deep LearningPT26M56.05S.webp|ML Lecture 6: Brief Introduction of Deep Learning - 26:56|50]] [26:56](https://www.youtube.com/watch?v=Dr-WRlEFefw&t=1616#t=26:56.05) output layers之前的部分將之視為Feature extractor，而output layer做的事情為Multi-calss Classifier，它會經過一個Softmx
- [29:27](https://www.youtube.com/watch?v=Dr-WRlEFefw&t=1767#t=29:27.25) example

# Gradient Descent

隨機選擇一個初始值，接著計算每一個參數(weight 和 bias)，接著計算每個參數的偏微分，所有偏微分的集稱為gradient，接著可以透過參數 - learning rate乘上參數所對應的gradient得到新的參數值

# 