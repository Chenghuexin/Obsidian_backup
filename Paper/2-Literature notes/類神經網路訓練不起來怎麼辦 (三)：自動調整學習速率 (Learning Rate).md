---
media: https://www.youtube.com/watch?v=HYUXEeh3kwY
---
承上回 : [[類神經網路訓練不起來怎麼辦 (三)：自動調整學習速率 (Learning Rate)]]

# Learning rate cannot be one-size-fits-all

learning rate應該要客製化，不同的參數需要不同的learning rate


- [11:36](https://www.youtube.com/watch?v=HYUXEeh3kwY&t=696#t=11:36.09) 

## Root Mean Square


- [15:21](https://www.youtube.com/watch?v=HYUXEeh3kwY&t=922#t=15:21.76) 過去所有的gradient的平方和，再平均然後開根號

- [16:01](https://www.youtube.com/watch?v=HYUXEeh3kwY&t=962#t=16:01.98) Adagrad


- [17:33](https://www.youtube.com/watch?v=HYUXEeh3kwY&t=1053#t=17:33.25) 同一個參數在不同的時間可能也會需要不同的learning rate

## RMSProp

