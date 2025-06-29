AutoAugment: automatically search for improved data augmentation policies

Search Space: a policy consists of many sub-policies
+ sub-policy: tow operations: image processing and probabilities and magnitudes with which the functions are applied

Search Algorithm: reinforcement learning

Improvements:
+ AutoAugment can be applied directly on the dataset of interest to find the best augmentation policy (AutoAugment-direct)
+ learned policies can be transferred to new datasets (AutoAugment-transfer)

# AutoAugment
###### policy: what image processing operation to use, the probability of using the operation in each batch, and the magnitude of the operation
###### frameword:
![[Pasted image 20250629213028.png]]

##### Search Space
A policy consists of 5 sub-policies with each sub-policy consisting of two image operations to be applied in sequence. Additionally, each operation is also associated with two hyperparameters: 1) the probability of applying the operation, and 2) the magnitude of the operation.

The operations we searched over are ShearX/Y, TranslateX/Y, Rotate, AutoContrast, Invert, Equalize, Solarize, Posterize, Contrast, Color, Brightness, Sharpness, Cutout, Sample Pairing.

##### Search Algorithm
