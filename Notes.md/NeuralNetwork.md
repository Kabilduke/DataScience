##### Two layer Neural Net-work:

$$ Z^{(1)} = XW^{(1)} ------- (1) $$
$$ A^1 = Sigmoid(Z^{(1)}) $$

$$ Z^{(2)} = A^1W^{(2)} ------- (2) $$
$$ Y^p = Sigmoid(Z^{(2)}) $$

- $X$ : Input
- $W^1$ :  Weights from  input to hidden layer 
- $W^2$ :  Weights from  hidden to output layer

```
import numpy as np
```

```python

class NeuralNetwork:
  def __init__(self):
      self.inputNetwork = 2
      self.outputNetwork = 1
      self.hiddenNetwork = 3

      self.weights_input_hidden = np.random.rand(self.inputNetwork, self.hiddenNetwork)
      self.weights_hidden_output = np.random.rand(self.hiddenNetwork, self.outputNetwork)

  def sigmoid(X):
      return 1 / (1+np.exp(-X))

  def forward(self, inputs):
      inputs = np.array(inputs)

      self.Z1 = np.dot(inputs, self.weights_input_hidden)
      self.A1 = self.sigmoid(self.Z1)

      self.Z2 = np.dot(self.A1, self.weights_hidden_output)
      self.Y_pred = self.sigmoid(self.Z2)

      return self.Y_pred

  def sigmoidprime(X):
     sigma = self.sigmoid
     return sigma * (1 - sigma)

  def cost_function(self, y, y_pred):
     return np.mean((y - y_pred)**2)

  def backward(self, inputs, y, learning_rate = 0.1):
     y_pred = self.forward(inputs)

     delta_output = (y_pred - y) * self.sigmoid(self.Z2)
     delta_hidden = np.dot(delta_output, self.weights_hidden_output.T) * self.sigmoidprime(self.Z1)

    #Gradient update:
     grad_hidden_output = np.dot(self.A1.T, delta_output)
     grad_input_hidden = np.dot(inputs.T, delta_hidden)

    #updating the weights:
     self.weights_hidden_output -= learning_rate * grad_hidden_output 
     self.weights_input_hidden -= learning_rate * grad_input_hidden

     return self.cost_function(y, y_pred) 

```

```python
NN = NeuralNetwork()

inputs = np.asarray([[5, 8],
          [2, 10],
          [6, 8]])
outputs = np.asarray([[0], [1], [0]])

for epoch in range(1000):
    loss = Neural_net.backward(inputs, outputs, learning_rate = 0.1)
    if epoch % 100 == 0:
        print(f"{epoch}: Loss {loss: .4f}")

predictions = Neural_net.forward(inputs)
print("Predictions:",predictions)
```

### Gradient Descent
###### Minimizing the cost function using Gradient Descent to find the gobal minimium
> Formula

$$ w = w - lr.\frac {\partial{L}} {\partial{w}} $$

Note :\
If $\frac {\partial{L}} {\partial{w}}$ is positive(+) the cost functions is going $Up$.

If $\frac {\partial{L}} {\partial{w}}$ is negative(-) the cost functions is going $Down$.
