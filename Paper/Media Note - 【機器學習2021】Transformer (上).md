---
media: https://www.youtube.com/watch?v=n9TlOhRjYoc
---
self-attention : [[自注意力機制 (Self-attention) (上)]]、[[自注意力機制 (Self-attention) (下)]]

# Sequence-to-sequence model

Transformer 是一個 Seq2Seq model, 它的輸出長度由機器自行決定

# Seq2seq for Multi-label Classification

## Multi-class v.s. Multi-label

- Multi-class : 機器要從數個class中選出一個class
- Multi-label : 同一個東西，可以屬於多個class

# Seq2seq 架構


- ![[【機器學習2021】Transformer (上)PT22M59.241S.webp|【機器學習2021】Transformer (上) - 22:59|50]] [22:59](https://www.youtube.com/watch?v=n9TlOhRjYoc&t=1379#t=22:59.24) 
## Encoder

工作 : 輸入一排向量，輸出一排向量
架構圖 :  ![[【機器學習2021】Transformer (上)PT24M44.058S.webp|【機器學習2021】Transformer (上) - 24:44|50]] [24:44](https://www.youtube.com/watch?v=n9TlOhRjYoc&t=1484#t=24:44.06) 

流程 : 輸入一排vector進入self-attention(multi-head)，self-attention的輸出還會加上原本相對應的輸入(residual connection)，接著再執行layer normalization，接著連接全連接，並且也有residual connection，再做一次layer normalization，最後輸出結果

> [!NOTE]
> - layer normalization : normalize同一個feature不同維度的資料
> 
> - 可能會加上positional encoding
> 
> - Add & Norm : residual + layer normalization

## Decoder
