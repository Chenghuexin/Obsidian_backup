# 訓練 LLM
- Step 1: mask description, Next Sentense Prediction, 只會文字接龍
- Step 2: supervised fine-tuning, 問答題QA
- Step 3: RLHF (Reinforcement Learning, Human Feedback)
	- humand feedback: 選擇題

# Step 1 - BASE MODEL
輸入的資料會包括網路上的資料 : 程式碼、維基百科、書籍、科學文獻、QA 網站、forums
GPT-2: 根據輸入的內容延續

# Step 2 - Supervised Fine-Tuning
輸入 : 問答題
準備大量的問答題餵入，使得產生這個回答的機率越高越好
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
![[Pasted image 20250608053820.png]]

### NAIVE RAG 痛點
- missing content
- missed the top ranked documents
- key points missing in answer
- structured data QA
- incorrect specificity, 回答太空泛
- wrong output format
- incomplete
- LLM security, 回答內容違反倫理

### Solution
- Pre-retrieval
	- Query Routing: 不同問題使用不同的方法
	- Query Rewriting
	- Query Expansion: decompose into sub questions(Query planning)
- Post-retrieval
	- Rerank
	- Summary

### Agentic flow
![[Pasted image 20250608054738.png]]
- reflection: 反思
- tool use
- planning
- multi-agent collaboration

### RAG 優點
- 外存知識 (fine tuning)
- 提供相當的解釋力
- 降低幻覺 (hallucination)

### Retrieval Augmented Generation Assessment (RAGA)
根據回答與正解比較正確性或相似性
answer_relevancy, faithfulness, context_precision by LLM