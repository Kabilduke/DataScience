##### Two layer Neural Net-work:

$$ Z^{(1)} = XW^{(1)} ------- (1) $$
$$ A^1 = Sigmoid(Z^{(1)}) $$

$$ Z^{(2)} = A^1W^{(2)} ------- (2) $$
$$ Y^p = Sigmoid(Z^{(2)}) $$

- $X$ : Input
- $W^1$ :  Weights from  input to hidden layer 
- $W^2$ :  Weights from  hidden to output layer

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

```
