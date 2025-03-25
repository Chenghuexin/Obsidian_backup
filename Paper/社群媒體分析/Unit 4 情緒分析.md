# Sentiment
- 定義 : 對某東西的評價
	- 表達方式 : 
		- 類別式 : Positive、Negative、Neutral
		- 數字型 : -5 ~ +5
		- 連續行 : [0, 1]
- valence : 喜歡程度
- arousal : 強度

# Sentiment Analysis - 1
用來判斷一篇文章./句子/一個目標的情緒取向(sentiment polarity)

##### Different Level
1. Document Level
2. Sentence Level
3. Aspect Level

##### Method - 字典法
- LIWC 情緒字典

# Sentiment Analysis - 2

## 標詞性 (POS)
- 詞性實體型態
	- Method 1: ML Sequence Model

## 進階情緒處理
- 進階字典法
	- 新增否定和加強字集
	- e.g. not good
	- not : -0.5, good: 0.7 -0.5 x 0.7 = -0.35
	- 所以是稍微帶有負面情緒
- 文件分類法
	- 需要正面和負面的文件集
	- 整理整個文件或句子的情緒
- 遞迴深度模型法
	- 需要情緒文具結構樹