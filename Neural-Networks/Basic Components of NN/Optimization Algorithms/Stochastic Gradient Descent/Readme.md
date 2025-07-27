## Working of Stochastic Gradient Descent

In Stochastic Gradient Descent, the gradient is calculated for each training example (or a small subset of training examples) rather than the entire dataset.

## Implementing SGD from scratch


### Challenges of SGD

1. Noisy Convergence: Since the gradient is estimated based on a single data point (or a small batch), the updates can be noisy, causing the cost function to fluctuate rather than steadily decrease. This makes convergence slower and more erratic than in batch gradient descent.

2. Learning Rate Tuning: SGD is highly sensitive to the choice of learning rate. A learning rate that is too large may cause the algorithm to diverge, while one that is too small can slow down convergence. Adaptive methods like Adam and RMSprop address this by adjusting the learning rate dynamically during training.

3. Long Training Times: While each individual update is fast, the convergence might take a longer time overall since the steps are more erratic compared to batch gradient descent.
### Variants of SGD

While traditional SGD is a method, there are several improvements and variants designed to improve convergence and stability:

1. Mini-batch SGD: Instead of using a single data point, mini-batch SGD uses a small batch of data points to calculate the gradient. This strikes a balance between the efficiency of SGD and the stability of batch gradient descent. It reduces the noise in the updates while maintaining the computational efficiency.

2. Momentum: Momentum helps accelerate SGD by adding a fraction of the previous update to the current one. This allows the algorithm to keep moving in the same direction and can help overcome oscillations in the cost function.

3. Adaptive Methods (example: Adam, RMSprop): These methods dynamically adjust the learning rate for each parameter. Adam, for example, uses both the average of the gradients (first moment) and the average of the squared gradients (second m
