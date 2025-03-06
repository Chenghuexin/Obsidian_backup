# 目的
從**適當的文本**中找出**重要的字詞**

# 方式
### 1.  抓取資料
- 訂定資料來源
- 訂定關鍵字找出相關文章
- 過濾:
	- 過短評論
	- 造假評價
		- 如何判斷?
			- 根據以往作者的評論
			- 根據評論內容、大致使用者的評分
			- 根據發文時間
			- 爬蟲
### 2.  清理資料
目的 : 轉成正規的文句(Keep only processable data)
- 格式統一
- 去除或取代符號
- 更正標點符號的使用
### 3.  斷句/斷詞

### 4.  詞性標記(POS)

### 5.  保留特色的字詞

# 字詞呈現方式
- 設定範圍
- 提取方式
- 圖形化呈現
	- 字詞共現圖
	- 文字雲
	- 字詞分類呈現

# Tidy Data

結構化資料，使之便於分析

### Two types of variables : 
- Dimension variables : 
	- 關於實體的基本屬性
	- independent
- Measure variables : 
	- 衡量的值
### Messy Dataset
- 把Dimension variable values 當作 header names
- 一個欄位裡面有多個變數
- 把Measure variable當作值
![[Pasted image 20250306202818.png]]