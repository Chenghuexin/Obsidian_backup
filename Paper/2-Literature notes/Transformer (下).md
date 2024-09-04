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

Masked Self-attention : 與self-attention不同的點是產生b1的時候只能考慮a1，產生b2時只能考慮a1,a2，以此類推([11:48](https://www.youtube.com/watch?v=N6aRv06iv2g&t=709#t=11:48.59) )；因為decoder的運作方法，所以只能考慮左邊的東西，無法考慮到右邊的東西