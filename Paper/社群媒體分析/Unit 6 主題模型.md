# 從文本中找出主題
# How to dicide topic?
Method 1: 人工決定，藉由字典(lexicon)決定
Method 2: 自動決定，並且每一個文件只會屬於一個主題
Method 3: 自動決定，但每一個文件可能會屬於多個主題

# Method 1 人工決定主題
字典 : 每一個主題會有相對應的相關的字詞

# Method 2 自動決定(單主題)
利用分群演算法將文件分群 :
- 將文件以向量表示(TF-IDF)
- 設置 similarity function (衡量文件的相似度)
- 分在同一群的文件會有較高的相似度，每一群就代表著一個topic

# Method 3 自動決定(多主題)
假設 :
- 每一個文件以 a bag of words 表示(no order)
- 主題數量
- 每一個主題在字詞上是多元分佈的
- 每一個文件在主題上是多元分佈的 (multinormal distribution)
公式
![[Pasted image 20250604112309.png]]
xi: 字詞 i 出現的次數
P(w): 機率分佈

# Topic Model
### Latent Dirichlet吃Allocation (LDA)
![[Pasted image 20250608033534.png]]![[Pasted image 20250608033732.png]]
![[Pasted image 20250608034005.png]]
- N: 文