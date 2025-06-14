
# Abastract
+ survival analysis model for NPC (malignant tumors)
+ nutritional status of cancer patients is closely associated with the clinical progression of the disease.
+ combine TabNet and Cox models
+ Using:
	+ TabNet: sequential attention mechanism
		+ extract interpretable features for identifying disease risk factors
	+ Cox: ?

# Motivation
+ the complexity of neural networks and their incompatibility with medical tabular data can reduce the interpretability of the model

# Introduction
### Malnutrition 
A significant factor in the occurrence and development of tumors, affecting the entire course of cancer and serving as the primary negative factor for the adverse clinical outcomes of tumor patients

Previous studies have shown that approximately 40% of patients with malignant tumors die from malnutrition, not from the disease itself

Most patients with malignant tumors require nutritional intervention. Therefore, timely and accurate detection of malnutrition in patients with nasopharyngeal carcinoma

### Survival analysis model
+ time-to-event model
+ in medical field, it also can identify the risk factors that impact patient survival
	+ for early decision-making
	+ improved treatment strategies
##### Cox Proportional Hazard Model (CPH)
Drawback
+ it posits that the logarithmic survival risk of a patient can be expressed as a linear combination of patient covariates (預設病因是線性關係), which is considered overly simplistic for many practical medical situations due to the frequent presence of complex nonlinear relationships among variables.

### Deep Survival Analysis model
+ Overcome the linear constraints of CPH
	+ combine DNN and CPH
Challenge
+ many neural networks have not shown comparable levels of effectiveness in handling tabular data
	+ In practice, clinical survival data frequently comprises a significant amount of tabular data, which many survival analysis models fail to adequately consider
	+ tabular data:
		+ Tabular Data Characteristics
			+ 特徵異質（heterogeneous features）
			- 樣本數量相對較小
			- 可能會有 curse of dimension
			- 含有極端值與離群值（outliers）
		- 深度學習架構的限制
			- 主要為連續數值資料設計 (影像、語音)
			- 無法有效處理類別型或非線性邏輯複雜的 tabular 資料
+ the interpretability

# Tab-Cox
### Input
input data enters the multi-step decision of the model after proceeding through the **BN layer**

### Decision Step
+ relies on sequential multi-step processing with N-steps decision
+ the input of each decision step is affected by information from the previous step to determine which features to utilize
+ At each decision step, the processed feature representation will be outputted along with the single-step prediction vector
+ Finally, the feature representation is aggregated to calculate the global feature importance.
+ At each decision step, the model adjusts its focus by considering past outcomes and current information.
+ 2 pivotal components:
	1. Attentive Transformer: feature selection
	2. Feature Transformer: feature extraction
### Attentive Transformer
+ generate a feature mask that assesses the importance of each feature
### Feature Transformer
+ “Instance-Wise” feature selection
	+ 不同資料其相同的特徵權重會不一樣