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

# Prompt-base