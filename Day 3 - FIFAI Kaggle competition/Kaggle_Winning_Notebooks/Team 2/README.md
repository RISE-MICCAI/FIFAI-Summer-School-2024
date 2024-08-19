# FIFAI 2024 Kaggle Solution
Solution notebook and description provided by Joey.
## Solution

- **Data processing before the model**:  I checked the ratio of labels and I observed the imbalance - more 0s than 1s. I counted each label in each client and balanced each label (equal) by using WeightedRandomSampler from pytorch library. This improved the result since our evaluation metric (the balanced accuracy) is attributed equally by 0s and 1s in the prediction labels.


- **Federated learning process**:  There was a missing and important component in the given code. The number of global rounds. I put the local learning and weight averaging in the loop and control the number of loops - global rounds. In general, I tried to reduce the number of local epochs and increase the number of global rounds to prevent client drift. In my case, 20 rounds, 3 epochs was the optimal for public test set.


- **In-model**: To improve further, I tested other models as well (SimpleMLP, DenseNet). I observed SimpleMLP was almost equally good as SimpleCNN and a powerful model, DenseNet got trained slowly and overfitted to training set. i decided to keep using SimpleCNN and to maxmize test-time adaptation effect (post-model processing), I inserted batchnorm layer additionally. However, Batchnorm made the model to be learned faster, and I observed it was overfitted to training set. Therefore, I used weight_decay in the optimizer to prevent overfitting.  By replacing activation function (ReLU -> LeakyReLU), I got a slight improvement as well.   


- **post-model processing**: I used TENT [1] out of Test-Time adaptation methods. To maximize TENT [1] effect, I increased batch size (32->128) and inserted adaptation steps in test inference time.



## References

[1]  Wang, Dequan et al. “Tent: Fully Test-Time Adaptation by Entropy Minimization.” International Conference on Learning Representations (2021).
