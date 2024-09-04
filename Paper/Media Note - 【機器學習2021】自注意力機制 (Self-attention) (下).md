---
media: https://www.youtube.com/watch?v=gmsMY5kc-zw
---
承上回 : [[自注意力機制 (Self-attention) (上)]]

# Multi-head Self-attention

透過query找key的相關，但相關有不同的形式和定義，所以應該要有多個不同的query負責不同的種類的相關性

> **以 2 heads作為解釋舉例** : 得到query(aj)之後乘上另外兩個矩陣得到qj1,qj2，以此類推，key和value都要有兩個；接著同一類的一起計算attention score，最後會得到bi1和bi2；接下來將bi1和bi2經過一個transform後得到bi


# Self-attention沒有位置資訊