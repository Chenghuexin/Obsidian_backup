# Motivation of Text Embedding
- Text embedding: 將一些文字投射至高維的空間(latent space)轉為向量，如果兩個向量相似那就代表這兩個文章在語義上是相似的
- latent: 我們不知道這些每一個維度代表的意義
##### 相似度(語義上的 semantically) :
- word to word matrix: 根據前後文(context)的用字比較相似度
	- 缺點 : 維度過大、字詞的順序
- Singular Value Decomposition (SVD)
	- 分解 word to word matrix
	- 只儲存比較重要的資訊
	- 問題 : 計算耗時、難以整合新的字詞或文件、沒有考量到字詞的順序
# Word Embeddings

### Word2Vec
- 每一個字詞都以low-dimension 向量表示
- 使用神經網路
- 關鍵 : 預測每一個字詞的surrounding words
### Continuous Bag of Word (CBOW)
從前後幾個字詞(a window of word) 去預測字詞
![[Pasted image 20250608042631.png]]
![[Pasted image 20250608043217.png]]
### Skip-gram (SG)
根據一個字詞去預測其周遭的字詞 (surrounding words)
![[Pasted image 20250608042638.png]]

### Word analogies
轉為向量後，根據字詞之間的關係(夾角)去推論出另一個字詞有相關的字詞

### Represent the meaning of sentence/text
- 方法一 : 對 word2vecs 取向量
- 方法二 : doc2vec
# Transformer-based Embeddings
### Problem
- Computation Bottleneck on the length of input sequence
- Attention is short，會遺忘稍早字詞的重點

### Decoder-Only Transformer
最後輸出的向量會經過一些處理，比如說contrastive learning
### Bert
- 使用 encoder

### ChatGPT
- 使用 decoder

![[Pasted image 20250608080929.png]]