## Tensor Flow tutorial

### Hello World

* Loss Function
  * After an epoch pass, calculate how well the model predict the answer (basically the cost function)
  * One of them is the Mean Squared Error
* Optimizer
  * Based on the result of the loss function, predict the best next set of weights/bias to use to be closer
  * One of them is the SGD or stochastic gradient descent
* Convergence
  * The idea of getting to an accuracy of 100%
  
### Activation Function

Executed for each layer of the network.
- Relu: Means if X > 0, return X else return 0
- Softmax: Take all the output, and return the biggest one
