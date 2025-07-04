# Chapter 3-1 ~ 3-2

# Introduction
- 介紹 prompt-based learning，在 LLM 是一個核心技術
+ 跟 fully supervised learning 和 fine-tuning pre-trained models 比較
+ 介紹 pormpt-based inference 步驟

### Prompt
語言模型的任務就是要去根據輸入去預測
### Prompt 的起源 - DMN
+ 前身 : Dynamic Memory Network (DMN)
+ 神經網路架構

# Fully Supervised Learning in NLP
+ 使用帶有標記的資料（labeled data）進行訓練
+ 這些資料包含輸入與對應的輸出範例，作為模型要學習的任務依據
+ 缺點
	+ 稀缺、昂貴、或需大量時間製作
		+ 舉例 : 情緒分類
	+ 專家設計「特徵工程」
	+ 泛化能力不足
# Pre-train and Fine-tune Learning in NLP
![[Pasted image 20250609134114.png]]
+ 優點 : 
	+ 減少對標記資料的依賴
		+ 因為預訓練已學得語言知識，微調時只需少量資料就能不錯的表現。
	+ 大量知識轉移
		+ 預訓練能讓模型學到通用語言知識，有助於改善多種 NLP 任務表現。
+ 缺點 : 
	+ 訓練成本高
	+ 模型可解釋性低
	+ **訓練目標不一致**  
		+ 預訓練是學「語意關係」，微調則是為了特定任務標註，兩者目標不同，可能造成效能下降。

# Prompt-based Learning
+ prompt-based inference
+ 一種創新的方法，可利用語言模型的強大能力，**在不需再進行微調的情況下**，直接生成特定任務的輸出。
	+ 使用方法
	+ ![[Pasted image 20250609141308.png]]
+ 優點
	+ 廣泛適用性
	+ 跨任務使用
	+ 降低標記資料需求
+ 缺點
	+ 高度依賴 prompt 設計
	+ 不易理解模型內部邏輯
	+ 可能輸出不穩定或矛盾

### Prompt-based Learning Process
以感情分類作為舉例
![[Pasted image 20250609151104.png]]
##### Step 1: Prompt Addition
將輸入資料 x 套入一個預先設計好的模板 template，產生出語言模型要預測的提示句

##### Step 2: Answer Search
[z] 這個位置有很多可能的詞（例如 "great" 或 "terrible"），我們要讓模型幫我們判斷哪一個詞最適合填入這個空格，根據語境做出最佳預測。
+ 把候選答案 z 一個個代入 prompt 中的 `[z]`
+ 模型計算每個填入後的句子機率 P
##### Step 3: Answer Mapping
雖然我們在步驟2找到了答案，但這個答案可能不是我們最後想要的結果。
所以要對答案做映射轉換

### Prompt-based Learning Across NLP Tasks