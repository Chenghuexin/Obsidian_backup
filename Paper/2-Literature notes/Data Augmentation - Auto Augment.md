AutoAugment: automatically search for improved data augmentation policies

Search Space: a policy consists of many sub-policies
+ sub-policy: tow operations: image processing and probabilities and magnitudes with which the functions are applied

Search Algorithm: reinforcement learning

Improvements:
+ AutoAugment can be applied directly on the dataset of interest to find the best augmentation policy (AutoAugment-direct)
+ learned policies can be transferred to new datasets (AutoAugment-transfer)

# AutoAugment
###### policy: what image processing operation to use, the probability of using the operation in each batch, and the magnitude of the operation
#####