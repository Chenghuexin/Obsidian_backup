---
media: https://www.youtube.com/watch?v=HYUXEeh3kwY
---
承上回 : [[類神經網路訓練不起來怎麼辦 (二)： 批次 (batch) 與動量 (momentum)]]

# Learning rate cannot be one-size-fits-all

learning rate應該要客製化，不同的參數需要不同的learning rate


- [11:36](https://www.youtube.com/watch?v=HYUXEeh3kwY&t=696#t=11:36.09) 

## Root Mean Square


- [15:21](https://www.youtube.com/watch?v=HYUXEeh3kwY&t=922#t=15:21.76) 過去所有的gradient的平方和，再平均然後開根號

- [16:01](https://www.youtube.com/watch?v=HYUXEeh3kwY&t=962#t=16:01.98) Adagrad

- [17:33](https://www.youtube.com/watch?v=HYUXEeh3kwY&t=1053#t=17:33.25) 同一個參數在不同的時間可能也會需要不同的learning rate

## RMSProp


- [19:25](https://www.youtube.com/watch?v=HYUXEeh3kwY&t=1165#t=19:25.26) 透過alpha可以自行調整每一個gradient的權重，達到動態調整sigma

- [21:57](https://www.youtube.com/watch?v=HYUXEeh3kwY&t=1318#t=21:57.63) example


# Adam

- RMSProp + Momentum
- most used optimization

# Learning Rate Scheduling

## Learning Rate Decay

learning rate隨著時間越來越小

## Warm Up

learning rate 首先變大再變小