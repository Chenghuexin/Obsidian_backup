# 訓練 LLM
- Step 1: mask description, Next Sentense Prediction, 只會文字接龍
- Step 2: supervised fine-tuning, 問答題QA
- Step 3: RLHF (Reinforcement Learning, Human Feedback)
	- humand feedback: 選擇題

# Step 1 - BASE MODEL
輸入的資料會包括網路上的資料 : 程式碼、維基百科、書籍、科學文獻、QA 網站、forums
GPT-2: 根據輸入的內容延續

# Step 2 - Supervised Fine-Tuning

# Step 3 - Humand Feedback
- reward model: 根據 QA 評分
# Step 4 - Reinforcement Learning
- reward 能符合人工對回答所排的順序
![[Pasted image 20250608052019.png]]

# Prompt Enginerring
##### Tips in prompt design
- provide clear context
- shuffle(調整) key words in the input
- tell the LLM what to avoid
- use list as input
- few shot prompting, provide some examples to help LLM better understand your intention
- Chain of Thought (COT) prompting, ask LLM to reason before giving an answer
- self consistency, 多問幾次

# Retrieval Assisted Generation (RAG)
##### LLM lack
- real time data
- data of a specialize domain

![[Pasted image 20250608053735.png]]
