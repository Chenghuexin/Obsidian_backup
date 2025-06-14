
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