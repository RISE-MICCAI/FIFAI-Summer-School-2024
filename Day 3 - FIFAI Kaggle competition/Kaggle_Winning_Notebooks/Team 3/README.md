# FIFAI 2024 Kaggle Solution
Solution notebook and description provided by Prabin Bohara. 
## Solution

- **To handle class imbalance**: I applied several data augmentation techniques. The SMOTE (Synthetic Minority Over-sampling Technique) was used to generate synthetic samples for minority classes, balancing the class distribution. Additionally, I implemented Random and Weighted Samplers to ensure adequate representation of minority classes during the training process. To further address class imbalance, I utilized a weighted cross-entropy loss function, assigning higher penalties to misclassifications of minority classes and thereby improving the model's ability to learn from these classes.

- **Training Process**: Each client node performed local training on its data for different numbers of epochs (50, 100, 200). The final submission was made for 200 epochs. I iterated the training process for 2 and 5 rounds to find the optimal configuration for model performance.


