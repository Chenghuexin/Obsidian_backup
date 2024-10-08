---
media: https://www.youtube.com/watch?v=N6aRv06iv2g
---
承上回 : [[Transformer (上)]]

# Transformer 架構 - Decoder

## Autoregressive

decoder會把自己的輸出當作接下來的輸入 (e.g.  [01:55](https://www.youtube.com/watch?v=N6aRv06iv2g&t=116#t=01:55.88) )

### 架構圖

 ![[【機器學習2021】Transformer (下)PT9M18.824S.webp|【機器學習2021】Transformer (下) - 09:18|50]] [09:18](https://www.youtube.com/watch?v=N6aRv06iv2g&t=559#t=09:18.82) 

### 流程

輸入begin token，經過masked self-attention, 接著進行residual connection和layer normalization；將輸出結果與encoder的輸出結果進行cross attention；最後進行全連接和Add & Norm

> [!NOTE]
> Masked Self-attention : 與self-attention不同的點是產生b1的時候只能考慮a1，產生b2時只能考慮a1,a2，以此類推([11:48](https://www.youtube.com/watch?v=N6aRv06iv2g&t=709#t=11:48.59) )；因為decoder的運作方法，所以只能考慮左邊的東西，無法考慮到右邊的東西

> [!NOTE]
> cross-attention : masked self-attention的輸出乘上transform得到一個向量query，然後encoder的輸出向量產生key，再計算key和query的attention score並執行一次softmax；接著藉由encoder的輸出向量產生value(這邊產生的方法都跟self-attention一樣)，接著與個別的attention score相乘最後相加
> 

## Non-autoregressive(NAT)

一次把整個句子產生出來，輸入可能會是一整排的begin token讓他一次產生一排的token

> [!NOTE]
> 怎麼決定輸入長度 : 
> 方法一 : 透過一個classifier決定輸入長度
> 方法二 : 輸入很長一排begin token，在輸出出現end token的時候停止

> 優點 : 執行速度比AT快、比較可以控制輸出的長度
> 
> 缺點 : 往往表現都不如AT(原因 : Multi-modality)

# Transformer - training

decoder的輸入會是正確答案(teacher forcing)

## Optimizing Evaluation Metrics

訓練的時候看的是cross-entropy
測試的時候看的是BLEU score

## Exopsure bias

不一致的現象 : 訓練的時候decoder看到的是正確答案，但在測試的時候decoder看到的是自己的預測結果

解決方法 : 在訓練的時候給予decoder錯誤的資料(scheduled sampling)
## Guided Attention

強制學習順序

## Beam Search

