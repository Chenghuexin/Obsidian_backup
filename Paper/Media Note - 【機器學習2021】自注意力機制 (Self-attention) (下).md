---
media: https://www.youtube.com/watch?v=gmsMY5kc-zw
---
承上回 : [[自注意力機制 (Self-attention) (上)]]

# Multi-head Self-attention

透過query找key的相關，但相關有不同的形式和定義，所以應該要有多個不同的query負責不同的種類的相關性

> **以 2 heads作為解釋舉例** : 得到query(aj)之後乘上另外兩個矩陣得到qj1,qj2，以此類推，key和value都要有兩個；接著同一類的一起計算attention score，最後會得到bi1和bi2；接下來將bi1和bi2經過一個transform後得到bi


# Positional Encoding

self-attention沒有位置資訊，如果想要把位置資訊加進去，可以使用positional encoding

原理 : 對每一個位置設定一個專屬向量(人工設置)，叫做positional vector，然後把對應的positional vector加到對應的向量

# Self-attention v.s. CNN

> CNN可以視為一種簡化版的self-attention，self-attention會考慮到整張圖片，但CNN只會考慮receptive field裡的東西；也可以說self-attention是CNN的複雜化

> CNN的彈性比較小，在資料量比較小的時候表現會比self-attention好；而self-attention彈性比較大，在資料量大的時候表現會比CNN好
