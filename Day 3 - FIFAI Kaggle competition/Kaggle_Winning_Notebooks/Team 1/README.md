
# FIFAI 2024 Kaggle Solution
Solution notebook and description provided by Rahmat Izwan Heroza.
## Method Components

- **Model Architecture**: CNN with two convolutional layers {28, 64} and two dense layers {128, 2}
- **Loss Function**: Weighted Cross Entropy. 
- We add a proximal term to the local objective function, which regularizes the updates made by individual clients to be closer to the global model.
- The best submission is trained for 100 round with 1 local epoch and mu of 0.01 .

## Solution
- **Solution to Imbalance Problem**: We use the **weighted cross entropy loss** with inverse frequency to make the model give more attention to the minority class.

-  **Solution to Non-IID Problem**: FedProx** [1] is used as the federated learning framework, where we tried different mu value = {0.1, 0.01, 0.001} 
- We train the framework for more round and/or epoch. We tried round = {50, 100, 200}, and local epoch = {1, 5, 20} 

## References

[1] Li, T., Sahu, A. K., Zaheer, M., Sanjabi, M., Talwalkar, A., & Smith, V. (2018). Federated Optimization in Heterogeneous Networks. ArXiv. [Link to paper](https://arxiv.org/abs/1812.06127)
