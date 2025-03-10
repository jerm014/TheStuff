# Project 2282: Classification Using Neural Networks
----


![1](2282_1.jpg)

## Background Context

At the end of this project, you should be able to build your own binary image classifier from scratch using`numpy`.

Good luck and have fun!

## Resources

**Read or watch**:

* [Supervised vs. Unsupervised Machine Learning](https://blogs.oracle.com/datascience/supervised-vs-unsupervised-machine-learning)
* [How would you explain neural networks to someone who knows very little about AI or neurology?](https://www.quora.com/How-would-you-explain-neural-networks-to-someone-who-knows-very-little-about-AI-or-neurology/answer/Yohan-John)
* [Using Neural Nets to Recognize Handwritten Digits](http://neuralnetworksanddeeplearning.com/chap1.html)(*until �A simple network to classify handwritten digits� (excluded)*)
* [Forward propagation](https://www.youtube.com/watch?v=wL17g67vU88)
* [Understanding Activation Functions in Neural Networks](https://medium.com/the-theory-of-everything/understanding-activation-functions-in-neural-networks-9491262884e0)
* [Loss function](https://en.wikipedia.org/wiki/Loss_function)
* [Gradient descent](https://en.wikipedia.org/wiki/Gradient_descent)
* [Calculus on Computational Graphs: Backpropagation](http://colah.github.io/posts/2015-08-Backprop/)
* [Backpropagation calculus](https://www.youtube.com/watch?v=tIeHLnjs5U8)
* [What is a Neural Network?](https://www.youtube.com/watch?v=n1l-9lIMW7E&index=2&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [Supervised Learning with a Neural Network](https://www.youtube.com/watch?v=BYGpKPY9pO0&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&t=0s&index=4)
* [Binary Classification](https://www.youtube.com/watch?v=eqEc66RFY0I&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=7)
* [Logistic Regression](https://www.youtube.com/watch?v=hjrYrynGWGA&index=8&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [Logistic Regression Cost Function](https://www.youtube.com/watch?v=SHEPb1JHw5o&index=9&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [Gradient Descent](https://www.youtube.com/watch?v=uJryes5Vk1o&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=10)
* [Computation Graph](https://www.youtube.com/watch?v=hCP1vGoCdYU&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=13)
* [Logistic Regression Gradient Descent](https://www.youtube.com/watch?v=z_xiwjEdAC4&index=15&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [Vectorization](https://www.youtube.com/watch?v=qsIrQi0fzbY&index=17&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [Vectorizing Logistic Regression](https://www.youtube.com/watch?v=okpqeEUdEkY&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=19)
* [Vectorizing Logistic Regression�s Gradient Computation](https://www.youtube.com/watch?v=2BkqApHKwn0&index=20&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [A Note on Python/Numpy Vectors](https://www.youtube.com/watch?v=V2QlTmh6P2Y&index=22&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [Neural Network Representations](https://www.youtube.com/watch?v=CcRkHl75Z-Y&index=26&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [Computing Neural Network Output](https://www.youtube.com/watch?v=rMOdrD61IoU&index=27&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [Vectorizing Across Multiple Examples](https://www.youtube.com/watch?v=xy5MOQpx3aQ&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=28)
* [Gradient Descent For Neural Networks](https://www.youtube.com/watch?v=7bLEWDZng_M&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&index=33)
* [Random Initialization](https://www.youtube.com/watch?v=6by6Xas_Kho&index=35&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [Deep L-Layer Neural Network](https://www.youtube.com/watch?v=2gw5tE2ziqA&index=36&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0)
* [Train/Dev/Test Sets](https://www.youtube.com/watch?v=1waHlpKiNyY&list=PLkDaE6sCZn6Hn0vK8co82zjQtt3T2Nkqc)
* [Random Initialization For Neural Networks : A Thing Of The Past](https://medium.com/towards-data-science/random-initialization-for-neural-networks-a-thing-of-the-past-bfcdd806bf9e)
* [Initialization of deep networks](http://ww1.deepdish.io/?sub1=cda23d8a-d0a3-11ed-96eb-2a7eb3cde2cb)
* [Multiclass classification](https://en.wikipedia.org/wiki/Multiclass_classification)
* [Derivation: Derivatives for Common Neural Network Activation Functions](https://theclevermachine.wordpress.com/2014/09/08/derivation-derivatives-for-common-neural-network-activation-functions/)
* [What is One Hot Encoding? Why And When do you have to use it?](https://hackernoon.com/what-is-one-hot-encoding-why-and-when-do-you-have-to-use-it-e3c6186d008f?gi=a4f47cf027f7)
* [Softmax function](https://en.wikipedia.org/wiki/Softmax_function)
* [What is the intuition behind SoftMax function?](https://www.quora.com/What-is-the-intuition-behind-SoftMax-function)
* [Cross entropy](https://en.wikipedia.org/wiki/Cross_entropy)
* [Loss Functions: Cross-Entropy](https://ml-cheatsheet.readthedocs.io/en/latest/loss_functions.html#cross-entropy)
* [Softmax Regression](https://www.youtube.com/watch?v=LLux1SW--oM&list=PLkDaE6sCZn6Hn0vK8co82zjQtt3T2Nkqc&index=31)(*Note: I suggest watching this video at 1.5x - 2x speed*)
* [Training Softmax Classifier](https://www.youtube.com/watch?v=ueO_Ph0Pyqk&list=PLkDaE6sCZn6Hn0vK8co82zjQtt3T2Nkqc&index=32)(*Note: I suggest watching this video at 1.5x - 2x speed*)
* [numpy.zeros](https://numpy.org/doc/1.18/reference/generated/numpy.zeros.html)
* [numpy.random.randn](https://docs.scipy.org/doc/numpy-1.15.1/reference/generated/numpy.random.randn.html)
* [numpy.exp](https://numpy.org/doc/1.18/reference/generated/numpy.exp.html)
* [numpy.log](https://numpy.org/doc/1.18/reference/generated/numpy.log.html)
* [numpy.sqrt](https://numpy.org/doc/1.18/reference/generated/numpy.sqrt.html)
* [numpy.where](https://numpy.org/doc/1.18/reference/generated/numpy.where.html)
* [numpy.max](https://docs.scipy.org/doc/numpy-1.15.0/reference/generated/numpy.amax.html)
* [numpy.sum](https://docs.scipy.org/doc/numpy-1.15.0/reference/generated/numpy.sum.html)
* [numpy.argmax](https://docs.scipy.org/doc/numpy-1.15.0/reference/generated/numpy.argmax.html)
* [What is Pickle in python?](https://yasoob.me/2013/08/02/what-is-pickle-in-python/)
* [pickle](https://docs.python.org/3/library/pickle.html)
* [pickle.dump](https://docs.python.org/3/library/pickle.html#pickle.dump)
* [pickle.load](https://docs.python.org/3/library/pickle.html#pickle.load)

**Optional**:

* [Predictive analytics](https://en.wikipedia.org/wiki/Predictive_analytics)
* [Maximum Likelihood Estimation](https://medium.com/towards-data-science/maximum-likelihood-estimation-984af2dcfcac)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What is a model?
* What is supervised learning?
* What is a prediction?
* What is a node?
* What is a weight?
* What is a bias?
* What are activation functions?
  * Sigmoid?
  * Tanh?
  * Relu?
  * Softmax?

* What is a layer?
* What is a hidden layer?
* What is Logistic Regression?
* What is a loss function?
* What is a cost function?
* What is forward propagation?
* What is Gradient Descent?
* What is back propagation?
* What is a Computation Graph?
* How to initialize weights/biases
* The importance of vectorization
* How to split up your data
* What is multiclass classification?
* What is a one-hot vector?
* How to encode/decode one-hot vectors
* What is the softmax function and when do you use it?
* What is cross-entropy loss?
* What is pickling in Python?
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`python3`(version 3.9)
* Your files will be executed with`numpy`(version 1.25.2)
* All your files should end with a new line
* The first line of all your files should be exactly`#!/usr/bin/env python3`
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`pycodestyle`style (version 2.11.1)
* All your modules should have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions (inside and outside a class) should have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`and`python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* Unless otherwise noted, you are not allowed to import any module except`import numpy as np`
* Unless otherwise noted, you are not allowed to use any loops (`for`,`while`, etc.)
* All your files must be executable
* The length of your files will be tested using`wc`
## More Info

### Matrix Multiplications

For all matrix multiplications in the following tasks, please use[numpy.matmul](https://numpy.org/doc/1.18/reference/generated/numpy.matmul.html)

### Testing your code

In order to test your code, you�ll need DATA! Please download these datasets ([Binary_Train.npz](https://s3.eu-west-3.amazonaws.com/hbtn.intranet.project.files/holbertonschool-ml/Binary_Train.npz),[Binary_Dev.npz](https://s3.eu-west-3.amazonaws.com/hbtn.intranet.project.files/holbertonschool-ml/Binary_Dev.npz),[MNIST.npz](https://s3.eu-west-3.amazonaws.com/hbtn.intranet.project.files/holbertonschool-ml/MNIST.npz)) to go along with all of the following main files. You**do not**need to upload these files to GitHub. Your code will not necessarily be tested with these datasets. All of the following code assumes that you have stored all of your datasets in a separate`data`directory.

``
```
alexa@ubuntu-xenial:$ cat show_data.py
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']

fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_3D[i])
    plt.title(Y[0, i])
    plt.axis('off')
plt.tight_layout()
plt.show()
alexa@ubuntu-xenial:$ ./show_data.py
```

![1](2282_1.png)

``
```
alexa@ubuntu-xenial:$ cat show_multi_data.py
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np

lib = np.load('../data/MNIST.npz')
print(lib.files)
X_train_3D = lib['X_train']
Y_train = lib['Y_train']

fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_train_3D[i])
    plt.title(str(Y_train[i]))
    plt.axis('off')
plt.tight_layout()
plt.show()
alexa@ubuntu-xenial:$ ./show_multi_data.py
['Y_test', 'X_test', 'X_train', 'Y_train', 'X_valid', 'Y_valid']
```

![2](2282_2.png)


----
## Tasks
---
### 0. Neuron

Write a class <!--plain-NL-->`Neuron`<!--inline-NL--> that defines a single neuron performing binary classification:<!--plain-NL-->

- class constructor: `def __init__(self, nx):`

`nx` is the number of input features to the neuron


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`

All exceptions should be raised in the order listed above
- `nx` is the number of input features to the neuron


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- All exceptions should be raised in the order listed above
- Public instance attributes:


`W`: The weights vector for the neuron. Upon instantiation, it should be initialized using a random normal distribution.
`b`: The bias for the neuron. Upon instantiation, it should be initialized to 0.
`A`: The activated output of the neuron (prediction). Upon instantiation, it should be initialized to 0.
- `W`: The weights vector for the neuron. Upon instantiation, it should be initialized using a random normal distribution.
- `b`: The bias for the neuron. Upon instantiation, it should be initialized to 0.
- `A`: The activated output of the neuron (prediction). Upon instantiation, it should be initialized to 0.

- `nx` is the number of input features to the neuron


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- All exceptions should be raised in the order listed above

- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`

- `W`: The weights vector for the neuron. Upon instantiation, it should be initialized using a random normal distribution.
- `b`: The bias for the neuron. Upon instantiation, it should be initialized to 0.
- `A`: The activated output of the neuron (prediction). Upon instantiation, it should be initialized to 0.

```
alexa@ubuntu-xenial:$ cat 0-main.py
#!/usr/bin/env python3

import numpy as np

Neuron = __import__('0-neuron').Neuron

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
neuron = Neuron(X.shape[0])
print(neuron.W)
print(neuron.W.shape)
print(neuron.b)
print(neuron.A)
neuron.A = 10
print(neuron.A)
alexa@ubuntu-xenial:$ ./0-main.py
[[ 1.76405235e+00  4.00157208e-01  9.78737984e-01  2.24089320e+00
   1.86755799e+00 -9.77277880e-01  9.50088418e-01 -1.51357208e-01

...

  -5.85865511e-02 -3.17543094e-01 -1.63242330e+00 -6.71341546e-02
   1.48935596e+00  5.21303748e-01  6.11927193e-01 -1.34149673e+00]]
(1, 784)
0
0
10
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `0-neuron.py`


---
### 1. Privatize Neuron

Write a class <!--plain-NL-->`Neuron`<!--inline-NL--> that defines a single neuron performing binary classification (Based on <!--plain-NL-->`0-neuron.py`<!--inline-NL-->):<!--plain-NL-->

- class constructor: `def __init__(self, nx):`

`nx` is the number of input features to the neuron


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be a integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be positive`

All exceptions should be raised in the order listed above
- `nx` is the number of input features to the neuron


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be a integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be positive`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be a integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be positive`
- All exceptions should be raised in the order listed above
- **Private** instance attributes:


`__W`: The weights vector for the neuron. Upon instantiation, it should be initialized using a random normal distribution.
`__b`: The bias for the neuron. Upon instantiation, it should be initialized to 0.
`__A`: The activated output of the neuron (prediction). Upon instantiation, it should be initialized to 0.
Each private attribute should have a corresponding getter function (no setter function).
- `__W`: The weights vector for the neuron. Upon instantiation, it should be initialized using a random normal distribution.
- `__b`: The bias for the neuron. Upon instantiation, it should be initialized to 0.
- `__A`: The activated output of the neuron (prediction). Upon instantiation, it should be initialized to 0.
- Each private attribute should have a corresponding getter function (no setter function).

- `nx` is the number of input features to the neuron


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be a integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be positive`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be a integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be positive`
- All exceptions should be raised in the order listed above

- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be a integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be positive`

- `__W`: The weights vector for the neuron. Upon instantiation, it should be initialized using a random normal distribution.
- `__b`: The bias for the neuron. Upon instantiation, it should be initialized to 0.
- `__A`: The activated output of the neuron (prediction). Upon instantiation, it should be initialized to 0.
- Each private attribute should have a corresponding getter function (no setter function).

```
alexa@ubuntu-xenial:$ cat 1-main.py
#!/usr/bin/env python3

import numpy as np

Neuron = __import__('1-neuron').Neuron

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
neuron = Neuron(X.shape[0])
print(neuron.W)
print(neuron.b)
print(neuron.A)
neuron.A = 10
print(neuron.A)
alexa@ubuntu-xenial:$ ./1-main.py
[[ 1.76405235e+00  4.00157208e-01  9.78737984e-01  2.24089320e+00
   1.86755799e+00 -9.77277880e-01  9.50088418e-01 -1.51357208e-01

...

  -5.85865511e-02 -3.17543094e-01 -1.63242330e+00 -6.71341546e-02
   1.48935596e+00  5.21303748e-01  6.11927193e-01 -1.34149673e+00]]
0
0
Traceback (most recent call last):
  File "./1-main.py", line 16, in <module>
    neuron.A = 10
AttributeError: can't set attribute
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `1-neuron.py`


---
### 2. Neuron Forward Propagation

Write a class <!--plain-NL-->`Neuron`<!--inline-NL--> that defines a single neuron performing binary classification (Based on <!--plain-NL-->`1-neuron.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def forward_prop(self, X):`

Calculates the forward propagation of the neuron
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

Updates the private attribute `__A`
The neuron should use a sigmoid activation function
Returns the private attribute `__A`
- Calculates the forward propagation of the neuron
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- Updates the private attribute `__A`
- The neuron should use a sigmoid activation function
- Returns the private attribute `__A`

- Calculates the forward propagation of the neuron
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- Updates the private attribute `__A`
- The neuron should use a sigmoid activation function
- Returns the private attribute `__A`

- `nx` is the number of input features to the neuron
- `m` is the number of examples

```
alexa@ubuntu-xenial:$ cat 2-main.py
#!/usr/bin/env python3

import numpy as np

Neuron = __import__('2-neuron').Neuron

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
neuron = Neuron(X.shape[0])
neuron._Neuron__b = 1
A = neuron.forward_prop(X)
if (A is neuron.A):
        print(A)
alexa@ubuntu-xenial:$ ./2-main.py
[[5.34775247e-10 7.24627778e-04 4.52416436e-07 ... 8.75691930e-05
  1.13141966e-06 6.55799932e-01]]
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `2-neuron.py`


---
### 3. Neuron Cost

Write a class <!--plain-NL-->`Neuron`<!--inline-NL--> that defines a single neuron performing binary classification (Based on <!--plain-NL-->`2-neuron.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def cost(self, Y, A):`

Calculates the cost of the model using logistic regression
`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
To avoid division by zero errors, please use `1.0000001 - A` instead of `1 - A`
Returns the cost
- Calculates the cost of the model using logistic regression
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
- To avoid division by zero errors, please use `1.0000001 - A` instead of `1 - A`
- Returns the cost

- Calculates the cost of the model using logistic regression
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
- To avoid division by zero errors, please use `1.0000001 - A` instead of `1 - A`
- Returns the cost

```
alexa@ubuntu-xenial:$ cat 3-main.py
#!/usr/bin/env python3

import numpy as np

Neuron = __import__('3-neuron').Neuron

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
neuron = Neuron(X.shape[0])
A = neuron.forward_prop(X)
cost = neuron.cost(Y, A)
print(cost)
alexa@ubuntu-xenial:$ ./3-main.py
4.365104944262272
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `3-neuron.py`


---
### 4. Evaluate Neuron

Write a class <!--plain-NL-->`Neuron`<!--inline-NL--> that defines a single neuron performing binary classification (Based on <!--plain-NL-->`3-neuron.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def evaluate(self, X, Y):`

Evaluates the neuron�s predictions
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
Returns the neuron�s prediction and the cost of the network, respectively


The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise
- Evaluates the neuron�s predictions
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- Returns the neuron�s prediction and the cost of the network, respectively


The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise
- The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
- The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise

- Evaluates the neuron�s predictions
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- Returns the neuron�s prediction and the cost of the network, respectively


The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise
- The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
- The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise

- `nx` is the number of input features to the neuron
- `m` is the number of examples

- The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
- The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise

```
alexa@ubuntu-xenial:$ cat 4-main.py
#!/usr/bin/env python3

import numpy as np

Neuron = __import__('4-neuron').Neuron

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
neuron = Neuron(X.shape[0])
A, cost = neuron.evaluate(X, Y)
print(A)
print(cost)
alexa@ubuntu-xenial:$ ./4-main.py
[[0 0 0 ... 0 0 0]]
4.365104944262272
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `4-neuron.py`


---
### 5. Neuron Gradient Descent

Write a class <!--plain-NL-->`Neuron`<!--inline-NL--> that defines a single neuron performing binary classification (Based on <!--plain-NL-->`4-neuron.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def gradient_descent(self, X, Y, A, alpha=0.05):`

Calculates one pass of gradient descent on the neuron
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
`alpha` is the learning rate
Updates the private attributes `__W` and `__b`
- Calculates one pass of gradient descent on the neuron
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
- `alpha` is the learning rate
- Updates the private attributes `__W` and `__b`

- Calculates one pass of gradient descent on the neuron
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
- `alpha` is the learning rate
- Updates the private attributes `__W` and `__b`

- `nx` is the number of input features to the neuron
- `m` is the number of examples

```
alexa@ubuntu-xenial:$ cat 5-main.py
#!/usr/bin/env python3

import numpy as np

Neuron = __import__('5-neuron').Neuron

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
neuron = Neuron(X.shape[0])
A = neuron.forward_prop(X)
neuron.gradient_descent(X, Y, A, 0.5)
print(neuron.W)
print(neuron.b)
alexa@ubuntu-xenial:$ ./5-main.py
[[ 1.76405235e+00  4.00157208e-01  9.78737984e-01  2.24089320e+00
   1.86755799e+00 -9.77277880e-01  9.50088418e-01 -1.51357208e-01

...

  -5.85865511e-02 -3.17543094e-01 -1.63242330e+00 -6.71341546e-02
   1.48935596e+00  5.21303748e-01  6.11927193e-01 -1.34149673e+00]]
0.2579495783615682
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `5-neuron.py`


---
### 6. Train Neuron

Write a class <!--plain-NL-->`Neuron`<!--inline-NL--> that defines a single neuron performing binary classification (Based on <!--plain-NL-->`5-neuron.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def train(self, X, Y, iterations=5000, alpha=0.05):`

Trains the neuron
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

`alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`

All exceptions should be raised in the order listed above
Updates the private attributes `__W`, `__b`, and `__A`
You are allowed to use one loop
Returns the evaluation of the training data after `iterations` of training have occurred
- Trains the neuron
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- All exceptions should be raised in the order listed above
- Updates the private attributes `__W`, `__b`, and `__A`
- You are allowed to use one loop
- Returns the evaluation of the training data after `iterations` of training have occurred

- Trains the neuron
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- All exceptions should be raised in the order listed above
- Updates the private attributes `__W`, `__b`, and `__A`
- You are allowed to use one loop
- Returns the evaluation of the training data after `iterations` of training have occurred

- `nx` is the number of input features to the neuron
- `m` is the number of examples

- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`

```
alexa@ubuntu-xenial:$ cat 6-main.py
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np

Neuron = __import__('6-neuron').Neuron

lib_train = np.load('../data/Binary_Train.npz')
X_train_3D, Y_train = lib_train['X'], lib_train['Y']
X_train = X_train_3D.reshape((X_train_3D.shape[0], -1)).T
lib_dev = np.load('../data/Binary_Dev.npz')
X_dev_3D, Y_dev = lib_dev['X'], lib_dev['Y']
X_dev = X_dev_3D.reshape((X_dev_3D.shape[0], -1)).T

np.random.seed(0)
neuron = Neuron(X_train.shape[0])
A, cost = neuron.train(X_train, Y_train, iterations=10)
accuracy = np.sum(A == Y_train) / Y_train.shape[1] * 100
print("Train cost:", np.round(cost, decimals=10))
print("Train accuracy: {}%".format(np.round(accuracy, decimals=10)))
print("Train data:", np.round(A, decimals=10))
print("Train Neuron A:", np.round(neuron.A, decimals=10))

A, cost = neuron.evaluate(X_dev, Y_dev)
accuracy = np.sum(A == Y_dev) / Y_dev.shape[1] * 100
print("Dev cost:", np.round(cost, decimals=10))
print("Dev accuracy: {}%".format(np.round(accuracy, decimals=10)))
print("Dev data:", np.round(A, decimals=10))
print("Dev Neuron A:", np.round(neuron.A, decimals=10))

fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_dev_3D[i])
    plt.title(A[0, i])
    plt.axis('off')
plt.tight_layout()
plt.show()

alexa@ubuntu-xenial:$ ./6-main.py
Train cost: 1.3805076999
Train accuracy: 64.737465456%
Train data: [[0 0 0 ... 0 0 1]]
Train Neuron A: [[2.70000000e-08 2.18229559e-01 1.63492900e-04 ... 4.66530830e-03
  6.06518000e-05 9.73817942e-01]]
Dev cost: 1.4096194345
Dev accuracy: 64.4917257683%
Dev data: [[1 0 0 ... 0 0 1]]
Dev Neuron A: [[0.85021134 0.         0.3526692  ... 0.10140937 0.         0.99555018]]

```



![3](2282_3.png)

*Not that great� Let�s get more data!*<!--italics-NL-->

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `6-neuron.py`


---
### 7. Upgrade Train Neuron

Write a class <!--plain-NL-->`Neuron`<!--inline-NL--> that defines a single neuron performing binary classification (Based on <!--plain-NL-->`6-neuron.py`<!--inline-NL-->):<!--plain-NL-->

- Update the public method `train` to `def train(self, X, Y, iterations=5000, alpha=0.05, verbose=True, graph=True, step=100):`

Trains the neuron by updating the private attributes `__W`, `__b`, and `__A`
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

`alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`

`verbose` is a boolean that defines whether or not to print information about the training. If `True`, print `Cost after {iteration} iterations: {cost}` every `step` iterations:


 Include data from the 0th and last iteration

 `graph` is a boolean that defines whether or not to graph information about the training once the training has completed. If `True`:


 Plot the training data every `step` iterations as a blue line
 Label the x-axis as `iteration`
 Label the y-axis as `cost`
 Title the plot `Training Cost`
 Include data from the 0th and last iteration

 Only if either `verbose` or `graph` are `True`:


if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
if `step` is not positive or is greater than `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`

All exceptions should be raised in the order listed above
 The 0th iteration should represent the state of the neuron before any training has occurred
 You are allowed to use one loop
 You can use `import matplotlib.pyplot as plt`
Returns: the evaluation of the training data after `iterations` of training have occurred
- Trains the neuron by updating the private attributes `__W`, `__b`, and `__A`
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- `verbose` is a boolean that defines whether or not to print information about the training. If `True`, print `Cost after {iteration} iterations: {cost}` every `step` iterations:


 Include data from the 0th and last iteration
- Include data from the 0th and last iteration
- `graph` is a boolean that defines whether or not to graph information about the training once the training has completed. If `True`:


 Plot the training data every `step` iterations as a blue line
 Label the x-axis as `iteration`
 Label the y-axis as `cost`
 Title the plot `Training Cost`
 Include data from the 0th and last iteration
- Plot the training data every `step` iterations as a blue line
- Label the x-axis as `iteration`
- Label the y-axis as `cost`
- Title the plot `Training Cost`
- Include data from the 0th and last iteration
- Only if either `verbose` or `graph` are `True`:


if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
if `step` is not positive or is greater than `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
- if `step` is not positive or is greater than `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- All exceptions should be raised in the order listed above
- The 0th iteration should represent the state of the neuron before any training has occurred
- You are allowed to use one loop
- You can use `import matplotlib.pyplot as plt`
- Returns: the evaluation of the training data after `iterations` of training have occurred

- Trains the neuron by updating the private attributes `__W`, `__b`, and `__A`
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- `verbose` is a boolean that defines whether or not to print information about the training. If `True`, print `Cost after {iteration} iterations: {cost}` every `step` iterations:


 Include data from the 0th and last iteration
- Include data from the 0th and last iteration
- `graph` is a boolean that defines whether or not to graph information about the training once the training has completed. If `True`:


 Plot the training data every `step` iterations as a blue line
 Label the x-axis as `iteration`
 Label the y-axis as `cost`
 Title the plot `Training Cost`
 Include data from the 0th and last iteration
- Plot the training data every `step` iterations as a blue line
- Label the x-axis as `iteration`
- Label the y-axis as `cost`
- Title the plot `Training Cost`
- Include data from the 0th and last iteration
- Only if either `verbose` or `graph` are `True`:


if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
if `step` is not positive or is greater than `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
- if `step` is not positive or is greater than `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- All exceptions should be raised in the order listed above
- The 0th iteration should represent the state of the neuron before any training has occurred
- You are allowed to use one loop
- You can use `import matplotlib.pyplot as plt`
- Returns: the evaluation of the training data after `iterations` of training have occurred

- `nx` is the number of input features to the neuron
- `m` is the number of examples

- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`

- Include data from the 0th and last iteration

- Plot the training data every `step` iterations as a blue line
- Label the x-axis as `iteration`
- Label the y-axis as `cost`
- Title the plot `Training Cost`
- Include data from the 0th and last iteration

- if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
- if `step` is not positive or is greater than `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`

```
alexa@ubuntu-xenial:$ cat 7-main.py
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np

Neuron = __import__('7-neuron').Neuron

lib_train = np.load('../data/Binary_Train.npz')
X_train_3D, Y_train = lib_train['X'], lib_train['Y']
X_train = X_train_3D.reshape((X_train_3D.shape[0], -1)).T
lib_dev = np.load('../data/Binary_Dev.npz')
X_dev_3D, Y_dev = lib_dev['X'], lib_dev['Y']
X_dev = X_dev_3D.reshape((X_dev_3D.shape[0], -1)).T

np.random.seed(0)
neuron = Neuron(X_train.shape[0])
A, cost = neuron.train(X_train, Y_train, iterations=3000)
accuracy = np.sum(A == Y_train) / Y_train.shape[1] * 100
print("Train cost:", cost)
print("Train accuracy: {}%".format(accuracy))
A, cost = neuron.evaluate(X_dev, Y_dev)
accuracy = np.sum(A == Y_dev) / Y_dev.shape[1] * 100
print("Dev cost:", cost)
print("Dev accuracy: {}%".format(accuracy))
fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_dev_3D[i])
    plt.title(A[0, i])
    plt.axis('off')
plt.tight_layout()
plt.show()
alexa@ubuntu-xenial:$ ./7-main.py
Cost after 0 iterations: 4.365104944262272
Cost after 100 iterations: 0.11955134491351888

...

Cost after 3000 iterations: 0.013386353289868338

```



![4](2282_4.png)

```
Train cost: 0.013386353289868338
Train accuracy: 99.66837741808132%
Dev cost: 0.010803484515167197
Dev accuracy: 99.81087470449172%

```



![5](2282_5.png)

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `7-neuron.py`


---
### 8. NeuralNetwork

Write a class <!--plain-NL-->`NeuralNetwork`<!--inline-NL--> that defines a neural network with one hidden layer performing binary classification:<!--plain-NL-->

- class constructor: `def __init__(self, nx, nodes):`

`nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`

`nodes` is the number of nodes found in the hidden layer


If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`

All exceptions should be raised in the order listed above
- `nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- `nodes` is the number of nodes found in the hidden layer


If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`
- If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
- If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`
- All exceptions should be raised in the order listed above
- Public instance attributes:


`W1`: The weights vector for the hidden layer. Upon instantiation, it should be initialized using a random normal distribution.
`b1`: The bias for the hidden layer. Upon instantiation, it should be initialized with 0�s.
`A1`: The activated output for the hidden layer. Upon instantiation, it should be initialized to 0.
`W2`: The weights vector for the output neuron. Upon instantiation, it should be initialized using a random normal distribution.
`b2`: The bias for the output neuron. Upon instantiation, it should be initialized to 0.
`A2`: The activated output for the output neuron (prediction). Upon instantiation, it should be initialized to 0.
- `W1`: The weights vector for the hidden layer. Upon instantiation, it should be initialized using a random normal distribution.
- `b1`: The bias for the hidden layer. Upon instantiation, it should be initialized with 0�s.
- `A1`: The activated output for the hidden layer. Upon instantiation, it should be initialized to 0.
- `W2`: The weights vector for the output neuron. Upon instantiation, it should be initialized using a random normal distribution.
- `b2`: The bias for the output neuron. Upon instantiation, it should be initialized to 0.
- `A2`: The activated output for the output neuron (prediction). Upon instantiation, it should be initialized to 0.

- `nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- `nodes` is the number of nodes found in the hidden layer


If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`
- If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
- If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`
- All exceptions should be raised in the order listed above

- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`

- If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
- If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`

- `W1`: The weights vector for the hidden layer. Upon instantiation, it should be initialized using a random normal distribution.
- `b1`: The bias for the hidden layer. Upon instantiation, it should be initialized with 0�s.
- `A1`: The activated output for the hidden layer. Upon instantiation, it should be initialized to 0.
- `W2`: The weights vector for the output neuron. Upon instantiation, it should be initialized using a random normal distribution.
- `b2`: The bias for the output neuron. Upon instantiation, it should be initialized to 0.
- `A2`: The activated output for the output neuron (prediction). Upon instantiation, it should be initialized to 0.

```
alexa@ubuntu-xenial:$ cat 8-main.py
#!/usr/bin/env python3

import numpy as np

NN = __import__('8-neural_network').NeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
nn = NN(X.shape[0], 3)
print(nn.W1)
print(nn.W1.shape)
print(nn.b1)
print(nn.W2)
print(nn.W2.shape)
print(nn.b2)
print(nn.A1)
print(nn.A2)
nn.A1 = 10
print(nn.A1)
alexa@ubuntu-xenial:$ ./8-main.py
[[ 1.76405235  0.40015721  0.97873798 ...  0.52130375  0.61192719
  -1.34149673]
 [ 0.47689837  0.14844958  0.52904524 ...  0.0960042  -0.0451133
   0.07912172]
 [ 0.85053068 -0.83912419 -1.01177408 ... -0.07223876  0.31112445
  -1.07836109]]
(3, 784)
[[0.]
 [0.]
 [0.]]
[[ 1.06160017 -1.18488744 -1.80525169]]
(1, 3)
0
0
0
10
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `8-neural_network.py`


---
### 9. Privatize NeuralNetwork

Write a class <!--plain-NL-->`NeuralNetwork`<!--inline-NL--> that defines a neural network with one hidden layer performing binary classification (based on <!--plain-NL-->`8-neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- class constructor: `def __init__(self, nx, nodes):`

`nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`

`nodes` is the number of nodes found in the hidden layer


If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`

All exceptions should be raised in the order listed above
- `nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- `nodes` is the number of nodes found in the hidden layer


If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`
- If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
- If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`
- All exceptions should be raised in the order listed above
- **Private** instance attributes:


`W1`: The weights vector for the hidden layer. Upon instantiation, it should be initialized using a random normal distribution.
`b1`: The bias for the hidden layer. Upon instantiation, it should be initialized with 0�s.
`A1`: The activated output for the hidden layer. Upon instantiation, it should be initialized to 0.
`W2`: The weights vector for the output neuron. Upon instantiation, it should be initialized using a random normal distribution.
`b2`: The bias for the output neuron. Upon instantiation, it should be initialized to 0.
`A2`: The activated output for the output neuron (prediction). Upon instantiation, it should be initialized to 0.
Each private attribute should have a corresponding getter function (no setter function).
- `W1`: The weights vector for the hidden layer. Upon instantiation, it should be initialized using a random normal distribution.
- `b1`: The bias for the hidden layer. Upon instantiation, it should be initialized with 0�s.
- `A1`: The activated output for the hidden layer. Upon instantiation, it should be initialized to 0.
- `W2`: The weights vector for the output neuron. Upon instantiation, it should be initialized using a random normal distribution.
- `b2`: The bias for the output neuron. Upon instantiation, it should be initialized to 0.
- `A2`: The activated output for the output neuron (prediction). Upon instantiation, it should be initialized to 0.
- Each private attribute should have a corresponding getter function (no setter function).

- `nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- `nodes` is the number of nodes found in the hidden layer


If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`
- If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
- If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`
- All exceptions should be raised in the order listed above

- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`

- If `nodes` is not an integer, raise a `TypeError` with the exception: `nodes must be an integer`
- If `nodes` is less than 1, raise a `ValueError` with the exception: `nodes must be a positive integer`

- `W1`: The weights vector for the hidden layer. Upon instantiation, it should be initialized using a random normal distribution.
- `b1`: The bias for the hidden layer. Upon instantiation, it should be initialized with 0�s.
- `A1`: The activated output for the hidden layer. Upon instantiation, it should be initialized to 0.
- `W2`: The weights vector for the output neuron. Upon instantiation, it should be initialized using a random normal distribution.
- `b2`: The bias for the output neuron. Upon instantiation, it should be initialized to 0.
- `A2`: The activated output for the output neuron (prediction). Upon instantiation, it should be initialized to 0.
- Each private attribute should have a corresponding getter function (no setter function).

```
alexa@ubuntu-xenial:$ cat 9-main.py
#!/usr/bin/env python3

import numpy as np

NN = __import__('9-neural_network').NeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
nn = NN(X.shape[0], 3)
print(nn.W1)
print(nn.b1)
print(nn.W2)
print(nn.b2)
print(nn.A1)
print(nn.A2)
nn.A1 = 10
print(nn.A1)
alexa@ubuntu-xenial:$ ./9-main.py
[[ 1.76405235  0.40015721  0.97873798 ...  0.52130375  0.61192719
  -1.34149673]
 [ 0.47689837  0.14844958  0.52904524 ...  0.0960042  -0.0451133
   0.07912172]
 [ 0.85053068 -0.83912419 -1.01177408 ... -0.07223876  0.31112445
  -1.07836109]]
[[0.]
 [0.]
 [0.]]
[[ 1.06160017 -1.18488744 -1.80525169]]
0
0
0
Traceback (most recent call last):
  File "./9-main.py", line 19, in <module>
    nn.A1 = 10
AttributeError: can't set attribute
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `9-neural_network.py`


---
### 10. NeuralNetwork Forward Propagation

Write a class <!--plain-NL-->`NeuralNetwork`<!--inline-NL--> that defines a neural network with one hidden layer performing binary classification (based on <!--plain-NL-->`9-neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def forward_prop(self, X):`

Calculates the forward propagation of the neural network
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

Updates the private attributes `__A1` and `__A2`
The neurons should use a sigmoid activation function
Returns the private attributes `__A1` and `__A2`, respectively
- Calculates the forward propagation of the neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- Updates the private attributes `__A1` and `__A2`
- The neurons should use a sigmoid activation function
- Returns the private attributes `__A1` and `__A2`, respectively

- Calculates the forward propagation of the neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- Updates the private attributes `__A1` and `__A2`
- The neurons should use a sigmoid activation function
- Returns the private attributes `__A1` and `__A2`, respectively

- `nx` is the number of input features to the neuron
- `m` is the number of examples

```
alexa@ubuntu-xenial:$ cat 10-main.py
#!/usr/bin/env python3

import numpy as np

NN = __import__('10-neural_network').NeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
nn = NN(X.shape[0], 3)
nn._NeuralNetwork__b1 = np.ones((3, 1))
nn._NeuralNetwork__b2 = 1
A1, A2 = nn.forward_prop(X)
if A1 is nn.A1:
        print(A1)
if A2 is nn.A2:
        print(A2)
alexa@ubuntu-xenial:$ ./10-main.py
[[5.34775247e-10 7.24627778e-04 4.52416436e-07 ... 8.75691930e-05
  1.13141966e-06 6.55799932e-01]
 [9.99652394e-01 9.99999995e-01 6.77919152e-01 ... 1.00000000e+00
  9.99662771e-01 9.99990554e-01]
 [5.57969669e-01 2.51645047e-02 4.04250047e-04 ... 1.57024117e-01
  9.97325173e-01 7.41310459e-02]]
[[0.23294587 0.44286405 0.54884691 ... 0.38502756 0.12079644 0.593269  ]]
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `10-neural_network.py`


---
### 11. NeuralNetwork Cost

Write a class <!--plain-NL-->`NeuralNetwork`<!--inline-NL--> that defines a neural network with one hidden layer performing binary classification (based on <!--plain-NL-->`10-neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def cost(self, Y, A):`

Calculates the cost of the model using logistic regression
`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
To avoid division by zero errors, please use `1.0000001 - A` instead of `1 - A`
Returns the cost
- Calculates the cost of the model using logistic regression
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
- To avoid division by zero errors, please use `1.0000001 - A` instead of `1 - A`
- Returns the cost

- Calculates the cost of the model using logistic regression
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
- To avoid division by zero errors, please use `1.0000001 - A` instead of `1 - A`
- Returns the cost

```
alexa@ubuntu-xenial:$ cat 11-main.py
#!/usr/bin/env python3

import numpy as np

NN = __import__('11-neural_network').NeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
nn = NN(X.shape[0], 3)
_, A = nn.forward_prop(X)
cost = nn.cost(Y, A)
print(cost)
alexa@ubuntu-xenial:$ ./11-main.py
0.7917984405648547
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `11-neural_network.py`


---
### 12. Evaluate NeuralNetwork

Write a class <!--plain-NL-->`NeuralNetwork`<!--inline-NL--> that defines a neural network with one hidden layer performing binary classification (based on <!--plain-NL-->`11-neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def evaluate(self, X, Y):`

Evaluates the neural network�s predictions
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
Returns the neuron�s prediction and the cost of the network, respectively


The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise
- Evaluates the neural network�s predictions
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- Returns the neuron�s prediction and the cost of the network, respectively


The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise
- The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
- The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise

- Evaluates the neural network�s predictions
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- Returns the neuron�s prediction and the cost of the network, respectively


The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise
- The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
- The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise

- `nx` is the number of input features to the neuron
- `m` is the number of examples

- The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
- The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise

```
alexa@ubuntu-xenial:$ cat 12-main.py
#!/usr/bin/env python3

import numpy as np

NN = __import__('12-neural_network').NeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
nn = NN(X.shape[0], 3)
A, cost = nn.evaluate(X, Y)
print(A)
print(cost)
alexa@ubuntu-xenial:$ ./12-main.py
[[0 0 0 ... 0 0 0]]
0.7917984405648547
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `12-neural_network.py`


---
### 13. NeuralNetwork Gradient Descent

Write a class <!--plain-NL-->`NeuralNetwork`<!--inline-NL--> that defines a neural network with one hidden layer performing binary classification (based on <!--plain-NL-->`12-neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def gradient_descent(self, X, Y, A1, A2, alpha=0.05):`

Calculates one pass of gradient descent on the neural network
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`A1` is the output of the hidden layer
`A2` is the predicted output
`alpha` is the learning rate
Updates the private attributes `__W1`, `__b1`, `__W2`, and `__b2`
- Calculates one pass of gradient descent on the neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `A1` is the output of the hidden layer
- `A2` is the predicted output
- `alpha` is the learning rate
- Updates the private attributes `__W1`, `__b1`, `__W2`, and `__b2`

- Calculates one pass of gradient descent on the neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `A1` is the output of the hidden layer
- `A2` is the predicted output
- `alpha` is the learning rate
- Updates the private attributes `__W1`, `__b1`, `__W2`, and `__b2`

- `nx` is the number of input features to the neuron
- `m` is the number of examples

```
alexa@ubuntu-xenial:$ cat 13-main.py
#!/usr/bin/env python3

import numpy as np

NN = __import__('13-neural_network').NeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
nn = NN(X.shape[0], 3)
A1, A2 = nn.forward_prop(X)
nn.gradient_descent(X, Y, A1, A2, 0.5)
print(nn.W1)
print(nn.b1)
print(nn.W2)
print(nn.b2)
alexa@ubuntu-xenial:$ ./13-main.py
[[ 1.76405235  0.40015721  0.97873798 ...  0.52130375  0.61192719
  -1.34149673]
 [ 0.47689837  0.14844958  0.52904524 ...  0.0960042  -0.0451133
   0.07912172]
 [ 0.85053068 -0.83912419 -1.01177408 ... -0.07223876  0.31112445
  -1.07836109]]
[[ 0.003193  ]
 [-0.01080922]
 [-0.01045412]]
[[ 1.06583858 -1.06149724 -1.79864091]]
[[0.15552509]]
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `13-neural_network.py`


---
### 14. Train NeuralNetwork

Write a class <!--plain-NL-->`NeuralNetwork`<!--inline-NL--> that defines a neural network with one hidden layer performing binary classification (based on <!--plain-NL-->`13-neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def train(self, X, Y, iterations=5000, alpha=0.05):`

Trains the neural network
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

`alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`

All exceptions should be raised in the order listed above
Updates the private attributes `__W1`, `__b1`,  `__A1`, `__W2`, `__b2`, and `__A2`
You are allowed to use one loop
Returns the evaluation of the training data after `iterations` of training have occurred
- Trains the neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- All exceptions should be raised in the order listed above
- Updates the private attributes `__W1`, `__b1`,  `__A1`, `__W2`, `__b2`, and `__A2`
- You are allowed to use one loop
- Returns the evaluation of the training data after `iterations` of training have occurred

- Trains the neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- All exceptions should be raised in the order listed above
- Updates the private attributes `__W1`, `__b1`,  `__A1`, `__W2`, `__b2`, and `__A2`
- You are allowed to use one loop
- Returns the evaluation of the training data after `iterations` of training have occurred

- `nx` is the number of input features to the neuron
- `m` is the number of examples

- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`

```
alexa@ubuntu-xenial:$ cat 14-main.py
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np

NN = __import__('14-neural_network').NeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_train_3D, Y_train = lib_train['X'], lib_train['Y']
X_train = X_train_3D.reshape((X_train_3D.shape[0], -1)).T
lib_dev = np.load('../data/Binary_Dev.npz')
X_dev_3D, Y_dev = lib_dev['X'], lib_dev['Y']
X_dev = X_dev_3D.reshape((X_dev_3D.shape[0], -1)).T

np.random.seed(0)
nn = NN(X_train.shape[0], 3)
A, cost = nn.train(X_train, Y_train, iterations=100)
accuracy = np.sum(A == Y_train) / Y_train.shape[1] * 100
print("Train cost:", cost)
print("Train accuracy: {}%".format(accuracy))
A, cost = nn.evaluate(X_dev, Y_dev)
accuracy = np.sum(A == Y_dev) / Y_dev.shape[1] * 100
print("Dev cost:", cost)
print("Dev accuracy: {}%".format(accuracy))
fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_dev_3D[i])
    plt.title(A[0, i])
    plt.axis('off')
plt.tight_layout()
plt.show()
alexa@ubuntu-xenial:$ ./14-main.py
Train cost: 0.4680930945144984
Train accuracy: 84.69009080142123%
Dev cost: 0.45985938789496067
Dev accuracy: 86.52482269503547%
alexa@ubuntu-xenial:$

```



![6](2282_6.png)

*Pretty good� but there are still some incorrect labels. We need more data to see why�*<!--italics-NL-->

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `14-neural_network.py`


---
### 15. Upgrade Train NeuralNetwork

Write a class <!--plain-NL-->`NeuralNetwork`<!--inline-NL--> that defines a neural network with one hidden layer performing binary classification (based on <!--plain-NL-->`14-neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Update the public method `train` to `def train(self, X, Y, iterations=5000, alpha=0.05, verbose=True, graph=True, step=100):`

Trains the neural network
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

`alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`

Updates the private attributes `__W1`, `__b1`, `__A1`, `__W2`, `__b2`, and `__A2`
`verbose` is a boolean that defines whether or not to print information about the training. If `True`, print `Cost after {iteration} iterations: {cost}` every `step` iterations:


 Include data from the 0th and last iteration

 `graph` is a boolean that defines whether or not to graph information about the training once the training has completed. If `True`:


 Plot the training data every `step` iterations as a blue line
 Label the x-axis as `iteration`
 Label the y-axis as `cost`
 Title the plot `Training Cost`
 Include data from the 0th and last iteration

 Only if either `verbose` or `graph` are `True`:


if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`

All exceptions should be raised in the order listed above
 The 0th iteration should represent the state of the neuron before any training has occurred
 You are allowed to use one loop
Returns the evaluation of the training data after `iterations` of training have occurred
- Trains the neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- Updates the private attributes `__W1`, `__b1`, `__A1`, `__W2`, `__b2`, and `__A2`
- `verbose` is a boolean that defines whether or not to print information about the training. If `True`, print `Cost after {iteration} iterations: {cost}` every `step` iterations:


 Include data from the 0th and last iteration
- Include data from the 0th and last iteration
- `graph` is a boolean that defines whether or not to graph information about the training once the training has completed. If `True`:


 Plot the training data every `step` iterations as a blue line
 Label the x-axis as `iteration`
 Label the y-axis as `cost`
 Title the plot `Training Cost`
 Include data from the 0th and last iteration
- Plot the training data every `step` iterations as a blue line
- Label the x-axis as `iteration`
- Label the y-axis as `cost`
- Title the plot `Training Cost`
- Include data from the 0th and last iteration
- Only if either `verbose` or `graph` are `True`:


if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
- if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- All exceptions should be raised in the order listed above
- The 0th iteration should represent the state of the neuron before any training has occurred
- You are allowed to use one loop
- Returns the evaluation of the training data after `iterations` of training have occurred

- Trains the neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- Updates the private attributes `__W1`, `__b1`, `__A1`, `__W2`, `__b2`, and `__A2`
- `verbose` is a boolean that defines whether or not to print information about the training. If `True`, print `Cost after {iteration} iterations: {cost}` every `step` iterations:


 Include data from the 0th and last iteration
- Include data from the 0th and last iteration
- `graph` is a boolean that defines whether or not to graph information about the training once the training has completed. If `True`:


 Plot the training data every `step` iterations as a blue line
 Label the x-axis as `iteration`
 Label the y-axis as `cost`
 Title the plot `Training Cost`
 Include data from the 0th and last iteration
- Plot the training data every `step` iterations as a blue line
- Label the x-axis as `iteration`
- Label the y-axis as `cost`
- Title the plot `Training Cost`
- Include data from the 0th and last iteration
- Only if either `verbose` or `graph` are `True`:


if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
- if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- All exceptions should be raised in the order listed above
- The 0th iteration should represent the state of the neuron before any training has occurred
- You are allowed to use one loop
- Returns the evaluation of the training data after `iterations` of training have occurred

- `nx` is the number of input features to the neuron
- `m` is the number of examples

- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`

- Include data from the 0th and last iteration

- Plot the training data every `step` iterations as a blue line
- Label the x-axis as `iteration`
- Label the y-axis as `cost`
- Title the plot `Training Cost`
- Include data from the 0th and last iteration

- if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
- if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`

```
alexa@ubuntu-xenial:$ cat 15-main.py
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np

NN = __import__('15-neural_network').NeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_train_3D, Y_train = lib_train['X'], lib_train['Y']
X_train = X_train_3D.reshape((X_train_3D.shape[0], -1)).T
lib_dev = np.load('../data/Binary_Dev.npz')
X_dev_3D, Y_dev = lib_dev['X'], lib_dev['Y']
X_dev = X_dev_3D.reshape((X_dev_3D.shape[0], -1)).T

np.random.seed(0)
nn = NN(X_train.shape[0], 3)
A, cost = nn.train(X_train, Y_train)
accuracy = np.sum(A == Y_train) / Y_train.shape[1] * 100
print("Train cost:", cost)
print("Train accuracy: {}%".format(accuracy))
A, cost = nn.evaluate(X_dev, Y_dev)
accuracy = np.sum(A == Y_dev) / Y_dev.shape[1] * 100
print("Dev cost:", cost)
print("Dev accuracy: {}%".format(accuracy))
fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_dev_3D[i])
    plt.title(A[0, i])
    plt.axis('off')
plt.tight_layout()
plt.show()
alexa@ubuntu-xenial:$ ./15-main.py
Cost after 0 iterations: 0.7917984405648547
Cost after 100 iterations: 0.4680930945144984

...

Cost after 5000 iterations: 0.024369225667283875

```



![7](2282_7.png)

```
Train cost: 0.024369225667283875
Train accuracy: 99.3999210422424%
Dev cost: 0.020330639788072768
Dev accuracy: 99.57446808510639%

```



![8](2282_8.png)

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `15-neural_network.py`


---
### 16. DeepNeuralNetwork

Write a class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> that defines a deep neural network performing binary classification:<!--plain-NL-->

- class constructor: `def __init__(self, nx, layers):`

`nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`

`layers` is a list representing the number of nodes in each layer of the network


If `layers` is not a list or an empty list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
The first value in `layers` represents the number of nodes in the first layer, �
If the elements in `layers` are not all positive integers, raise a `TypeError` with the exception `layers must be a list of positive integers`

All exceptions should be raised in the order listed above
Sets the public instance attributes:


`L`: The number of layers in the neural network.
`cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
`weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to 0�s and saved in the `weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to


You are allowed to use one loop
- `nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- `layers` is a list representing the number of nodes in each layer of the network


If `layers` is not a list or an empty list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
The first value in `layers` represents the number of nodes in the first layer, �
If the elements in `layers` are not all positive integers, raise a `TypeError` with the exception `layers must be a list of positive integers`
- If `layers` is not a list or an empty list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
- The first value in `layers` represents the number of nodes in the first layer, �
- If the elements in `layers` are not all positive integers, raise a `TypeError` with the exception `layers must be a list of positive integers`
- All exceptions should be raised in the order listed above
- Sets the public instance attributes:


`L`: The number of layers in the neural network.
`cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
`weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to 0�s and saved in the `weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- `L`: The number of layers in the neural network.
- `cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
- `weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to 0�s and saved in the `weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- The weights of the network should be initialized using the `He et al.` method and saved in the `weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
- The biases of the network should be initialized to 0�s and saved in the `weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- You are allowed to use one loop

- `nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- `layers` is a list representing the number of nodes in each layer of the network


If `layers` is not a list or an empty list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
The first value in `layers` represents the number of nodes in the first layer, �
If the elements in `layers` are not all positive integers, raise a `TypeError` with the exception `layers must be a list of positive integers`
- If `layers` is not a list or an empty list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
- The first value in `layers` represents the number of nodes in the first layer, �
- If the elements in `layers` are not all positive integers, raise a `TypeError` with the exception `layers must be a list of positive integers`
- All exceptions should be raised in the order listed above
- Sets the public instance attributes:


`L`: The number of layers in the neural network.
`cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
`weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to 0�s and saved in the `weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- `L`: The number of layers in the neural network.
- `cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
- `weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to 0�s and saved in the `weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- The weights of the network should be initialized using the `He et al.` method and saved in the `weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
- The biases of the network should be initialized to 0�s and saved in the `weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- You are allowed to use one loop

- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`

- If `layers` is not a list or an empty list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
- The first value in `layers` represents the number of nodes in the first layer, �
- If the elements in `layers` are not all positive integers, raise a `TypeError` with the exception `layers must be a list of positive integers`

- `L`: The number of layers in the neural network.
- `cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
- `weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to 0�s and saved in the `weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- The weights of the network should be initialized using the `He et al.` method and saved in the `weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
- The biases of the network should be initialized to 0�s and saved in the `weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to

- The weights of the network should be initialized using the `He et al.` method and saved in the `weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
- The biases of the network should be initialized to 0�s and saved in the `weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to

```
alexa@ubuntu-xenial:$ cat 16-main.py
#!/usr/bin/env python3

import numpy as np

Deep = __import__('16-deep_neural_network').DeepNeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
deep = Deep(X.shape[0], [5, 3, 1])
print(deep.cache)
print(deep.weights)
print(deep.L)
deep.L = 10
print(deep.L)
alexa@ubuntu-xenial:$ ./16-main.py
{}
{'W1': array([[ 0.0890981 ,  0.02021099,  0.04943373, ...,  0.02632982,
         0.03090699, -0.06775582],
       [ 0.02408701,  0.00749784,  0.02672082, ...,  0.00484894,       
        -0.00227857,  0.00399625],
       [ 0.04295829, -0.04238217, -0.05110231, ..., -0.00364861,       
         0.01571416, -0.05446546],
       [ 0.05361891, -0.05984585, -0.09117898, ..., -0.03094292,
        -0.01925805, -0.06308145],
       [-0.01667953, -0.04216413,  0.06239623, ..., -0.02024521,
        -0.05159656, -0.02373981]]), 'b1': array([[0.],
       [0.],
       [0.],
       [0.],
       [0.]]), 'W2': array([[ 0.4609219 ,  0.56004008, -1.2250799 , -0.09454199,  0.57799141],        
       [-0.16310703,  0.06882082, -0.94578088, -0.30359994,  1.15661914],
       [-0.49841799, -0.9111359 ,  0.09453424,  0.49877298,  0.75503205]]), 'b2': array([[0.],        
       [0.],
       [0.]]), 'W3': array([[-0.42271877,  0.18165055,  0.4444639 ]]), 'b3': array([[0.]])}
3
10
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `16-deep_neural_network.py`


---
### 17. Privatize DeepNeuralNetwork

Write a class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> that defines a deep neural network performing binary classification (based on <!--plain-NL-->`16-deep_neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- class constructor: `def __init__(self, nx, layers):`

`nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`

`layers` is a list representing the number of nodes in each layer of the network


If `layers` is not a list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
The first value in `layers` represents the number of nodes in the first layer, �
If the elements in `layers` are not all positive integers, raise a TypeError with the exception `layers must be a list of positive integers`

All exceptions should be raised in the order listed above
Sets the **private** instance attributes:


`__L`: The number of layers in the neural network.
`__cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
`__weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `__weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to `0`�s and saved in the `__weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to

Each private attribute should have a corresponding getter function (no setter function).

You are allowed to use one loop
- `nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- `layers` is a list representing the number of nodes in each layer of the network


If `layers` is not a list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
The first value in `layers` represents the number of nodes in the first layer, �
If the elements in `layers` are not all positive integers, raise a TypeError with the exception `layers must be a list of positive integers`
- If `layers` is not a list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
- The first value in `layers` represents the number of nodes in the first layer, �
- If the elements in `layers` are not all positive integers, raise a TypeError with the exception `layers must be a list of positive integers`
- All exceptions should be raised in the order listed above
- Sets the **private** instance attributes:


`__L`: The number of layers in the neural network.
`__cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
`__weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `__weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to `0`�s and saved in the `__weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to

Each private attribute should have a corresponding getter function (no setter function).
- `__L`: The number of layers in the neural network.
- `__cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
- `__weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `__weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to `0`�s and saved in the `__weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- The weights of the network should be initialized using the `He et al.` method and saved in the `__weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
- The biases of the network should be initialized to `0`�s and saved in the `__weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- Each private attribute should have a corresponding getter function (no setter function).
- You are allowed to use one loop

- `nx` is the number of input features


If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`
- `layers` is a list representing the number of nodes in each layer of the network


If `layers` is not a list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
The first value in `layers` represents the number of nodes in the first layer, �
If the elements in `layers` are not all positive integers, raise a TypeError with the exception `layers must be a list of positive integers`
- If `layers` is not a list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
- The first value in `layers` represents the number of nodes in the first layer, �
- If the elements in `layers` are not all positive integers, raise a TypeError with the exception `layers must be a list of positive integers`
- All exceptions should be raised in the order listed above
- Sets the **private** instance attributes:


`__L`: The number of layers in the neural network.
`__cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
`__weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `__weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to `0`�s and saved in the `__weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to

Each private attribute should have a corresponding getter function (no setter function).
- `__L`: The number of layers in the neural network.
- `__cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
- `__weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `__weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to `0`�s and saved in the `__weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- The weights of the network should be initialized using the `He et al.` method and saved in the `__weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
- The biases of the network should be initialized to `0`�s and saved in the `__weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- Each private attribute should have a corresponding getter function (no setter function).
- You are allowed to use one loop

- If `nx` is not an integer, raise a `TypeError` with the exception: `nx must be an integer`
- If `nx` is less than 1, raise a `ValueError` with the exception: `nx must be a positive integer`

- If `layers` is not a list, raise a `TypeError` with the exception: `layers must be a list of positive integers`
- The first value in `layers` represents the number of nodes in the first layer, �
- If the elements in `layers` are not all positive integers, raise a TypeError with the exception `layers must be a list of positive integers`

- `__L`: The number of layers in the neural network.
- `__cache`: A dictionary to hold all intermediary values of the network. Upon instantiation, it should be set to an empty dictionary.
- `__weights`: A dictionary to hold all weights and biased of the network. Upon instantiation:


The weights of the network should be initialized using the `He et al.` method and saved in the `__weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
The biases of the network should be initialized to `0`�s and saved in the `__weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- The weights of the network should be initialized using the `He et al.` method and saved in the `__weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
- The biases of the network should be initialized to `0`�s and saved in the `__weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to
- Each private attribute should have a corresponding getter function (no setter function).

- The weights of the network should be initialized using the `He et al.` method and saved in the `__weights` dictionary using the key `W{l}` where `{l}` is the hidden layer the weight belongs to
- The biases of the network should be initialized to `0`�s and saved in the `__weights` dictionary using the key `b{l}` where `{l}` is the hidden layer the bias belongs to

```
alexa@ubuntu-xenial:$ cat 17-main.py
#!/usr/bin/env python3

import numpy as np

Deep = __import__('17-deep_neural_network').DeepNeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
deep = Deep(X.shape[0], [5, 3, 1])
print(deep.cache)
print(deep.weights)
print(deep.L)
deep.L = 10
print(deep.L)
alexa@ubuntu-xenial:$ ./17-main.py
{}
{'W1': array([[ 0.0890981 ,  0.02021099,  0.04943373, ...,  0.02632982,
         0.03090699, -0.06775582],
       [ 0.02408701,  0.00749784,  0.02672082, ...,  0.00484894,
        -0.00227857,  0.00399625],
       [ 0.04295829, -0.04238217, -0.05110231, ..., -0.00364861,
         0.01571416, -0.05446546],
       [ 0.05361891, -0.05984585, -0.09117898, ..., -0.03094292,
        -0.01925805, -0.06308145],
       [-0.01667953, -0.04216413,  0.06239623, ..., -0.02024521,
        -0.05159656, -0.02373981]]), 'b1': array([[0.],
       [0.],
       [0.],
       [0.],
       [0.]]), 'W2': array([[ 0.4609219 ,  0.56004008, -1.2250799 , -0.09454199,  0.57799141],        
       [-0.16310703,  0.06882082, -0.94578088, -0.30359994,  1.15661914],
       [-0.49841799, -0.9111359 ,  0.09453424,  0.49877298,  0.75503205]]), 'b2': array([[0.],        
       [0.],
       [0.]]), 'W3': array([[-0.42271877,  0.18165055,  0.4444639 ]]), 'b3': array([[0.]])}
3
Traceback (most recent call last):
  File "./17-main.py", line 16, in <module>
    deep.L = 10
AttributeError: can't set attribute
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `17-deep_neural_network.py`


---
### 18. DeepNeuralNetwork Forward Propagation

Write a class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> that defines a deep neural network performing binary classification (based on <!--plain-NL-->`17-deep_neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def forward_prop(self, X):`

Calculates the forward propagation of the neural network
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

Updates the private attribute `__cache`:


The activated outputs of each layer should be saved in the `__cache` dictionary using the key `A{l}` where `{l}` is the hidden layer the activated output belongs to
`X` should be saved to the `cache` dictionary using the key `A0`

All neurons should use a sigmoid activation function
You are allowed to use one loop
Returns the output of the neural network and the cache, respectively
- Calculates the forward propagation of the neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- Updates the private attribute `__cache`:


The activated outputs of each layer should be saved in the `__cache` dictionary using the key `A{l}` where `{l}` is the hidden layer the activated output belongs to
`X` should be saved to the `cache` dictionary using the key `A0`
- The activated outputs of each layer should be saved in the `__cache` dictionary using the key `A{l}` where `{l}` is the hidden layer the activated output belongs to
- `X` should be saved to the `cache` dictionary using the key `A0`
- All neurons should use a sigmoid activation function
- You are allowed to use one loop
- Returns the output of the neural network and the cache, respectively

- Calculates the forward propagation of the neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- Updates the private attribute `__cache`:


The activated outputs of each layer should be saved in the `__cache` dictionary using the key `A{l}` where `{l}` is the hidden layer the activated output belongs to
`X` should be saved to the `cache` dictionary using the key `A0`
- The activated outputs of each layer should be saved in the `__cache` dictionary using the key `A{l}` where `{l}` is the hidden layer the activated output belongs to
- `X` should be saved to the `cache` dictionary using the key `A0`
- All neurons should use a sigmoid activation function
- You are allowed to use one loop
- Returns the output of the neural network and the cache, respectively

- `nx` is the number of input features to the neuron
- `m` is the number of examples

- The activated outputs of each layer should be saved in the `__cache` dictionary using the key `A{l}` where `{l}` is the hidden layer the activated output belongs to
- `X` should be saved to the `cache` dictionary using the key `A0`

```
alexa@ubuntu-xenial:$ cat 18-main.py
#!/usr/bin/env python3

import numpy as np

Deep = __import__('18-deep_neural_network').DeepNeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
deep = Deep(X.shape[0], [5, 3, 1])
deep._DeepNeuralNetwork__weights['b1'] = np.ones((5, 1))
deep._DeepNeuralNetwork__weights['b2'] = np.ones((3, 1))
deep._DeepNeuralNetwork__weights['b3'] = np.ones((1, 1))
A, cache = deep.forward_prop(X)
print(A)
print(cache)
print(cache is deep.cache)
print(A is cache['A3'])
alexa@ubuntu-xenial:$ ./18-main.py
[[0.75603476 0.7516025  0.75526716 ... 0.75228888 0.75522853 0.75217069]]
{'A0': array([[0., 0., 0., ..., 0., 0., 0.],
       [0., 0., 0., ..., 0., 0., 0.],
       [0., 0., 0., ..., 0., 0., 0.],
       ...,
       [0., 0., 0., ..., 0., 0., 0.],
       [0., 0., 0., ..., 0., 0., 0.],
       [0., 0., 0., ..., 0., 0., 0.]], dtype=float32), 'A1': array([[0.4678435 , 0.64207147, 0.55271425, ..., 0.61718097, 0.56412986,
        0.72751504],
       [0.79441392, 0.87140579, 0.72851107, ..., 0.8898201 , 0.79466389,
        0.82257068],
       [0.72337339, 0.68239373, 0.63526533, ..., 0.7036234 , 0.7770501 ,
        0.69465346],
       [0.65305735, 0.69829955, 0.58646313, ..., 0.73949722, 0.52054315,
        0.73151973],
       [0.67408798, 0.69624537, 0.73084352, ..., 0.70663173, 0.76204175,
        0.72705428]]), 'A2': array([[0.75067742, 0.78319533, 0.77755571, ..., 0.77891002, 0.75847839, 
        0.78517215],
       [0.70591081, 0.71159364, 0.7362214 , ..., 0.70845465, 0.72133875,
        0.71090691],
       [0.72032379, 0.69519095, 0.72414599, ..., 0.70067751, 0.71161433,
        0.70420437]]), 'A3': array([[0.75603476, 0.7516025 , 0.75526716, ..., 0.75228888, 0.75522853, 
        0.75217069]])}
True
True
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `18-deep_neural_network.py`


---
### 19. DeepNeuralNetwork Cost

Write a class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> that defines a deep neural network performing binary classification (based on <!--plain-NL-->`18-deep_neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def cost(self, Y, A):`

Calculates the cost of the model using logistic regression
`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
To avoid division by zero errors, please use `1.0000001 - A` instead of `1 - A`
Returns the cost
- Calculates the cost of the model using logistic regression
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
- To avoid division by zero errors, please use `1.0000001 - A` instead of `1 - A`
- Returns the cost

- Calculates the cost of the model using logistic regression
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `A` is a `numpy.ndarray` with shape (1, `m`) containing the activated output of the neuron for each example
- To avoid division by zero errors, please use `1.0000001 - A` instead of `1 - A`
- Returns the cost

```
alexa@ubuntu-xenial:$ cat 19-main.py
#!/usr/bin/env python3

import numpy as np

Deep = __import__('19-deep_neural_network').DeepNeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
deep = Deep(X.shape[0], [5, 3, 1])
A, _ = deep.forward_prop(X)
cost = deep.cost(Y, A)
print(cost)
alexa@ubuntu-xenial:$ ./19-main.py
0.6958649419170609
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `19-deep_neural_network.py`


---
### 20. Evaluate DeepNeuralNetwork

Write a class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> that defines a deep neural network performing binary classification (based on <!--plain-NL-->`19-deep_neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def evaluate(self, X, Y):`

Evaluates the neural network�s predictions
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
Returns the neuron�s prediction and the cost of the network, respectively


The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise
- Evaluates the neural network�s predictions
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- Returns the neuron�s prediction and the cost of the network, respectively


The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise
- The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
- The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise

- Evaluates the neural network�s predictions
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- Returns the neuron�s prediction and the cost of the network, respectively


The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise
- The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
- The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise

- `nx` is the number of input features to the neuron
- `m` is the number of examples

- The prediction should be a `numpy.ndarray` with shape (1, `m`) containing the predicted labels for each example
- The label values should be 1 if the output of the network is &gt;= 0.5 and 0 otherwise

```
alexa@ubuntu-xenial:$ cat 20-main.py
#!/usr/bin/env python3

import numpy as np

Deep = __import__('20-deep_neural_network').DeepNeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
deep = Deep(X.shape[0], [5, 3, 1])
A, cost = deep.evaluate(X, Y)
print(A)
print(cost)
alexa@ubuntu-xenial:$ ./20-main.py
[[1 1 1 ... 1 1 1]]
0.6958649419170609
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `20-deep_neural_network.py`


---
### 21. DeepNeuralNetwork Gradient Descent

Write a class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> that defines a deep neural network performing binary classification (based on <!--plain-NL-->`20-deep_neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def gradient_descent(self, Y, cache, alpha=0.05):`

Calculates one pass of gradient descent on the neural network
`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`cache` is a dictionary containing all the intermediary values of the network
`alpha` is the learning rate
Updates the private attribute `__weights`
You are allowed to use one loop
- Calculates one pass of gradient descent on the neural network
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `cache` is a dictionary containing all the intermediary values of the network
- `alpha` is the learning rate
- Updates the private attribute `__weights`
- You are allowed to use one loop

- Calculates one pass of gradient descent on the neural network
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `cache` is a dictionary containing all the intermediary values of the network
- `alpha` is the learning rate
- Updates the private attribute `__weights`
- You are allowed to use one loop

```
alexa@ubuntu-xenial:$ cat 21-main.py
#!/usr/bin/env python3

import numpy as np

Deep = __import__('21-deep_neural_network').DeepNeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_3D, Y = lib_train['X'], lib_train['Y']
X = X_3D.reshape((X_3D.shape[0], -1)).T

np.random.seed(0)
deep = Deep(X.shape[0], [5, 3, 1])
A, cache = deep.forward_prop(X)
deep.gradient_descent(Y, cache, 0.5)
print(deep.weights)
alexa@ubuntu-xenial:$ ./21-main.py
{'W1': array([[ 0.0890981 ,  0.02021099,  0.04943373, ...,  0.02632982,
         0.03090699, -0.06775582],
       [ 0.02408701,  0.00749784,  0.02672082, ...,  0.00484894,
        -0.00227857,  0.00399625],
       [ 0.04295829, -0.04238217, -0.05110231, ..., -0.00364861,
         0.01571416, -0.05446546],
       [ 0.05361891, -0.05984585, -0.09117898, ..., -0.03094292,
        -0.01925805, -0.06308145],
       [-0.01667953, -0.04216413,  0.06239623, ..., -0.02024521,
        -0.05159656, -0.02373981]]), 'b1': array([[-1.01835520e-03],
       [-1.22929756e-04],
       [ 9.25521878e-05],
       [ 1.07730873e-04],
       [ 2.29014796e-04]]), 'W2': array([[ 0.4586347 ,  0.55968571, -1.22435332, -0.09516874,  0.57668454],
       [-0.16209305,  0.06902405, -0.9460547 , -0.30329296,  1.15722071],
       [-0.49595566, -0.91068385,  0.09382566,  0.49948968,  0.75647764]]), 'b2': array([[-0.00055419],
       [ 0.00032369],
       [ 0.0007201 ]]), 'W3': array([[-0.41262664,  0.18889024,  0.44717929]]), 'b3': array([[0.00659936]])}
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `21-deep_neural_network.py`


---
### 22. Train DeepNeuralNetwork

Write a class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> that defines a deep neural network performing binary classification (based on <!--plain-NL-->`21-deep_neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Add the public method `def train(self, X, Y, iterations=5000, alpha=0.05):`

Trains the deep neural network
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

`alpha` is the learning rate


if `alpha` is not a float, raise a TypeError with the exception `alpha must be a float`
if `alpha` is not positive, raise a ValueError with the exception `alpha must be positive`

All exceptions should be raised in the order listed above
Updates the private attributes `__weights` and `__cache`
You are allowed to use one loop
Returns the evaluation of the training data after `iterations` of training have occurred
- Trains the deep neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a TypeError with the exception `alpha must be a float`
if `alpha` is not positive, raise a ValueError with the exception `alpha must be positive`
- if `alpha` is not a float, raise a TypeError with the exception `alpha must be a float`
- if `alpha` is not positive, raise a ValueError with the exception `alpha must be positive`
- All exceptions should be raised in the order listed above
- Updates the private attributes `__weights` and `__cache`
- You are allowed to use one loop
- Returns the evaluation of the training data after `iterations` of training have occurred

- Trains the deep neural network
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a TypeError with the exception `alpha must be a float`
if `alpha` is not positive, raise a ValueError with the exception `alpha must be positive`
- if `alpha` is not a float, raise a TypeError with the exception `alpha must be a float`
- if `alpha` is not positive, raise a ValueError with the exception `alpha must be positive`
- All exceptions should be raised in the order listed above
- Updates the private attributes `__weights` and `__cache`
- You are allowed to use one loop
- Returns the evaluation of the training data after `iterations` of training have occurred

- `nx` is the number of input features to the neuron
- `m` is the number of examples

- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

- if `alpha` is not a float, raise a TypeError with the exception `alpha must be a float`
- if `alpha` is not positive, raise a ValueError with the exception `alpha must be positive`

```
alexa@ubuntu-xenial:$ cat 22-main.py
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np

Deep = __import__('22-deep_neural_network').DeepNeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_train_3D, Y_train = lib_train['X'], lib_train['Y']
X_train = X_train_3D.reshape((X_train_3D.shape[0], -1)).T
lib_dev = np.load('../data/Binary_Dev.npz')
X_dev_3D, Y_dev = lib_dev['X'], lib_dev['Y']
X_dev = X_dev_3D.reshape((X_dev_3D.shape[0], -1)).T

np.random.seed(0)
deep = Deep(X_train.shape[0], [5, 3, 1])
A, cost = deep.train(X_train, Y_train, iterations=100)
accuracy = np.sum(A == Y_train) / Y_train.shape[1] * 100
print("Train cost:", cost)
print("Train accuracy: {}%".format(accuracy))
A, cost = deep.evaluate(X_dev, Y_dev)
accuracy = np.sum(A == Y_dev) / Y_dev.shape[1] * 100
print("Dev cost:", cost)
print("Dev accuracy: {}%".format(accuracy))
fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_dev_3D[i])
    plt.title(A[0, i])
    plt.axis('off')
plt.tight_layout()
plt.show()
alexa@ubuntu-xenial:$ ./22-main.py
Train cost: 0.6444304786060048
Train accuracy: 56.241610738255034%
Dev cost: 0.6428913158565179
Dev accuracy: 57.730496453900706%

```



![9](2282_9.png)

*Hmm� doesn�t seem like this worked very well. Could it be because of our architecture or that it wasn�t trained properly? We need to see more information�*<!--italics-NL-->

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `22-deep_neural_network.py`


---
### 23. Upgrade Train DeepNeuralNetwork

Write a class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> that defines a deep neural network performing binary classification (based on <!--plain-NL-->`22-deep_neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Update the public method `train` to `def train(self, X, Y, iterations=5000, alpha=0.05, verbose=True, graph=True, step=100):`

Trains the deep neural network by updating the private attributes `__weights` and `__cache`
`X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples

`Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
`iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

`alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`

`verbose` is a boolean that defines whether or not to print information about the training. If `True`, print `Cost after {iteration} iterations: {cost}` every `step` iterations:


 Include data from the 0th and last iteration

 `graph` is a boolean that defines whether or not to graph information about the training once the training has completed. If `True`:


 Plot the training data every `step` iterations as a blue line
 Label the x-axis as `iteration`
 Label the y-axis as `cost`
 Title the plot `Training Cost`
 Include data from the 0th and last iteration

 Only if either `verbose` or `graph` are `True`:


if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`

All exceptions should be raised in the order listed above
 The 0th iteration should represent the state of the neuron before any training has occurred
 You are allowed to use one loop
Returns the evaluation of the training data after `iterations` of training have occurred
- Trains the deep neural network by updating the private attributes `__weights` and `__cache`
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- `verbose` is a boolean that defines whether or not to print information about the training. If `True`, print `Cost after {iteration} iterations: {cost}` every `step` iterations:


 Include data from the 0th and last iteration
- Include data from the 0th and last iteration
- `graph` is a boolean that defines whether or not to graph information about the training once the training has completed. If `True`:


 Plot the training data every `step` iterations as a blue line
 Label the x-axis as `iteration`
 Label the y-axis as `cost`
 Title the plot `Training Cost`
 Include data from the 0th and last iteration
- Plot the training data every `step` iterations as a blue line
- Label the x-axis as `iteration`
- Label the y-axis as `cost`
- Title the plot `Training Cost`
- Include data from the 0th and last iteration
- Only if either `verbose` or `graph` are `True`:


if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
- if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- All exceptions should be raised in the order listed above
- The 0th iteration should represent the state of the neuron before any training has occurred
- You are allowed to use one loop
- Returns the evaluation of the training data after `iterations` of training have occurred

- Trains the deep neural network by updating the private attributes `__weights` and `__cache`
- `X` is a `numpy.ndarray` with shape (`nx`, `m`) that contains the input data


`nx` is the number of input features to the neuron
`m` is the number of examples
- `nx` is the number of input features to the neuron
- `m` is the number of examples
- `Y` is a `numpy.ndarray` with shape (1, `m`) that contains the correct labels for the input data
- `iterations` is the number of iterations to train over


if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`
- `alpha` is the learning rate


if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`
- `verbose` is a boolean that defines whether or not to print information about the training. If `True`, print `Cost after {iteration} iterations: {cost}` every `step` iterations:


 Include data from the 0th and last iteration
- Include data from the 0th and last iteration
- `graph` is a boolean that defines whether or not to graph information about the training once the training has completed. If `True`:


 Plot the training data every `step` iterations as a blue line
 Label the x-axis as `iteration`
 Label the y-axis as `cost`
 Title the plot `Training Cost`
 Include data from the 0th and last iteration
- Plot the training data every `step` iterations as a blue line
- Label the x-axis as `iteration`
- Label the y-axis as `cost`
- Title the plot `Training Cost`
- Include data from the 0th and last iteration
- Only if either `verbose` or `graph` are `True`:


if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
- if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`
- All exceptions should be raised in the order listed above
- The 0th iteration should represent the state of the neuron before any training has occurred
- You are allowed to use one loop
- Returns the evaluation of the training data after `iterations` of training have occurred

- `nx` is the number of input features to the neuron
- `m` is the number of examples

- if `iterations` is not an integer, raise a `TypeError` with the exception `iterations must be an integer`
- if `iterations` is not positive, raise a `ValueError` with the exception `iterations must be a positive integer`

- if `alpha` is not a float, raise a `TypeError` with the exception `alpha must be a float`
- if `alpha` is not positive, raise a `ValueError` with the exception `alpha must be positive`

- Include data from the 0th and last iteration

- Plot the training data every `step` iterations as a blue line
- Label the x-axis as `iteration`
- Label the y-axis as `cost`
- Title the plot `Training Cost`
- Include data from the 0th and last iteration

- if `step` is not an integer, raise a `TypeError` with the exception `step must be an integer`
- if `step` is not positive and less than or equal to `iterations`, raise a `ValueError` with the exception `step must be positive and &lt;= iterations`

```
alexa@ubuntu-xenial:$ cat 23-main.py
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np

Deep = __import__('23-deep_neural_network').DeepNeuralNetwork

lib_train = np.load('../data/Binary_Train.npz')
X_train_3D, Y_train = lib_train['X'], lib_train['Y']
X_train = X_train_3D.reshape((X_train_3D.shape[0], -1)).T
lib_dev = np.load('../data/Binary_Dev.npz')
X_dev_3D, Y_dev = lib_dev['X'], lib_dev['Y']
X_dev = X_dev_3D.reshape((X_dev_3D.shape[0], -1)).T

np.random.seed(0)
deep = Deep(X_train.shape[0], [5, 3, 1])
A, cost = deep.train(X_train, Y_train)
accuracy = np.sum(A == Y_train) / Y_train.shape[1] * 100
print("Train cost:", cost)
print("Train accuracy: {}%".format(accuracy))
A, cost = deep.evaluate(X_dev, Y_dev)
accuracy = np.sum(A == Y_dev) / Y_dev.shape[1] * 100
print("Dev cost:", cost)
print("Dev accuracy: {}%".format(accuracy))
fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_dev_3D[i])
    plt.title(A[0, i])
    plt.axis('off')
plt.tight_layout()
plt.show()
alexa@ubuntu-xenial:$ ./23-main.py
Cost after 0 iterations: 0.6958649419170609
Cost after 100 iterations: 0.6444304786060048

...
Cost after 4800 iterations: 0.012130338888226167
Cost after 4900 iterations: 0.011896856912322803
Cost after 5000 iterations: 0.011671820326008163

```



![10](2282_10.png)

```
Train cost: 0.011671820326008163
Train accuracy: 99.88945913936044%
Dev cost: 0.009249552132279246
Dev accuracy: 99.95271867612293%

```



![11](2282_11.png)

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `23-deep_neural_network.py`


---
### 24. One-Hot Encode

Write a function <!--plain-NL-->`def one_hot_encode(Y, classes):`<!--inline-NL--> that converts a numeric label vector into a one-hot matrix:<!--plain-NL-->

- `Y` is a `numpy.ndarray` with shape (`m`,) containing numeric class labels


`m` is the number of examples
- `m` is the number of examples
- `classes` is the maximum number of classes found in `Y`
- Returns: a one-hot encoding of `Y` with shape (`classes`, `m`), or `None` on failure

- `m` is the number of examples

```
alexa@ubuntu-xenial:$ cat 24-main.py
#!/usr/bin/env python3

import numpy as np

oh_encode = __import__('24-one_hot_encode').one_hot_encode

lib = np.load('../data/MNIST.npz')
Y = lib['Y_train'][:10]

print(Y)
Y_one_hot = oh_encode(Y, 10)
print(Y_one_hot)
alexa@ubuntu-xenial:$ ./24-main.py
[5 0 4 1 9 2 1 3 1 4]
[[0. 1. 0. 0. 0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 1. 0. 0. 1. 0. 1. 0.]
 [0. 0. 0. 0. 0. 1. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0. 0. 0. 1. 0. 0.]
 [0. 0. 1. 0. 0. 0. 0. 0. 0. 1.]
 [1. 0. 0. 0. 0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 1. 0. 0. 0. 0. 0.]]
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `24-one_hot_encode.py`


---
### 25. One-Hot Decode

Write a function <!--plain-NL-->`def one_hot_decode(one_hot):`<!--inline-NL--> that converts a one-hot matrix into a vector of labels:<!--plain-NL-->

- `one_hot` is a one-hot encoded `numpy.ndarray` with shape (`classes`, `m`)


`classes` is the maximum number of classes
`m` is the number of examples
- `classes` is the maximum number of classes
- `m` is the number of examples
- Returns: a `numpy.ndarray` with shape (`m`, ) containing the numeric labels for each example, or `None` on failure

- `classes` is the maximum number of classes
- `m` is the number of examples

```
alexa@ubuntu-xenial:$ cat 25-main.py
#!/usr/bin/env python3

import numpy as np

oh_encode = __import__('24-one_hot_encode').one_hot_encode
oh_decode = __import__('25-one_hot_decode').one_hot_decode

lib = np.load('../data/MNIST.npz')
Y = lib['Y_train'][:10]

print(Y)
Y_one_hot = oh_encode(Y, 10)
Y_decoded = oh_decode(Y_one_hot)
print(Y_decoded)
alexa@ubuntu-xenial:$ ./25-main.py
[5 0 4 1 9 2 1 3 1 4]
[5 0 4 1 9 2 1 3 1 4]
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `25-one_hot_decode.py`


---
### 26. Persistence is Key

Update the class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> (based on <!--plain-NL-->`23-deep_neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Create the instance method `def save(self, filename):`

Saves the instance object to a file in `pickle` format
`filename` is the file to which the object should be saved
If `filename` does not have the extension `.pkl`, add it
- Saves the instance object to a file in `pickle` format
- `filename` is the file to which the object should be saved
- If `filename` does not have the extension `.pkl`, add it
- Create the static method `def load(filename):`

Loads a pickled `DeepNeuralNetwork` object
`filename` is the file from which the object should be loaded
Returns: the loaded object, or `None` if `filename` doesn�t exist
- Loads a pickled `DeepNeuralNetwork` object
- `filename` is the file from which the object should be loaded
- Returns: the loaded object, or `None` if `filename` doesn�t exist

Create the instance method <!--plain-NL-->`def save(self, filename):`<!--inline-NL-->

- Saves the instance object to a file in `pickle` format
- `filename` is the file to which the object should be saved
- If `filename` does not have the extension `.pkl`, add it

Create the static method <!--plain-NL-->`def load(filename):`<!--inline-NL-->

- Loads a pickled `DeepNeuralNetwork` object
- `filename` is the file from which the object should be loaded
- Returns: the loaded object, or `None` if `filename` doesn�t exist

```
alexa@ubuntu-xenial:$ cat 26-main.py
#!/usr/bin/env python3

import numpy as np

Deep = __import__('26-deep_neural_network').DeepNeuralNetwork
one_hot_encode = __import__('24-one_hot_encode').one_hot_encode
one_hot_decode = __import__('25-one_hot_decode').one_hot_decode

lib_train = np.load('../data/Binary_Train.npz')
X_train_3D, Y_train = lib_train['X'], lib_train['Y']
X_train = X_train_3D.reshape((X_train_3D.shape[0], -1)).T

np.random.seed(0)
deep = Deep(X_train.shape[0], [3, 1])
A, cost = deep.train(X_train, Y_train, iterations=400, graph=False)
deep.save('26-output')
del deep

saved = Deep.load('26-output.pkl')
A_saved, cost_saved = saved.evaluate(X_train, Y_train)

print(np.array_equal(A, A_saved) and cost == cost_saved)
alexa@ubuntu-xenial:$ ls 26-output*
ls: cannot access '26-output*': No such file or directory
alexa@ubuntu-xenial:$ ./26-main.py
Cost after 0 iterations: 0.7773240521521816
Cost after 100 iterations: 0.18751378071323063
Cost after 200 iterations: 0.12117095705345622
Cost after 300 iterations: 0.09031067302785326
Cost after 400 iterations: 0.07222364349190777
True
alexa@ubuntu-xenial:$ ls 26-output*
26-output.pkl
alexa@ubuntu-xenial:$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `26-deep_neural_network.py`


---
### 27. Update DeepNeuralNetwork

Update the class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> to perform multiclass classification (based on <!--plain-NL-->`26-deep_neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- You will need to update the instance methods `forward_prop`, `cost`, and `evaluate`
- `Y` is now a one-hot `numpy.ndarray` of shape `(classes, m)`

*Ideally, you should not have to change the __init__, gradient_descent, or train instance methods*<!--italics-NL-->

Because the training process takes such a long time, I have pretrained a model for you to load and finish training (<!--plain-->[27-saved.pkl](https://s3.eu-west-3.amazonaws.com/hbtn.intranet.project.files/holbertonschool-ml/27-saved.pkl) <!--link-->). This model has already been trained for 2000 iterations.<!--plain-->

*The training process may take up to 5 minutes*<!--italics-NL-->

```
alexa@ubuntu-xenial:$ cat 27-main.py
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np

Deep = __import__('27-deep_neural_network').DeepNeuralNetwork
one_hot_encode = __import__('24-one_hot_encode').one_hot_encode
one_hot_decode = __import__('25-one_hot_decode').one_hot_decode

lib= np.load('../data/MNIST.npz')
X_train_3D = lib['X_train']
Y_train = lib['Y_train']
X_valid_3D = lib['X_valid']
Y_valid = lib['Y_valid']
X_train = X_train_3D.reshape((X_train_3D.shape[0], -1)).T
X_valid = X_valid_3D.reshape((X_valid_3D.shape[0], -1)).T
Y_train_one_hot = one_hot_encode(Y_train, 10)
Y_valid_one_hot = one_hot_encode(Y_valid, 10)

deep = Deep.load('27-saved.pkl')
A_one_hot, cost = deep.train(X_train, Y_train_one_hot, iterations=100,
                             step=10, graph=False)
A = one_hot_decode(A_one_hot)
accuracy = np.sum(Y_train == A) / Y_train.shape[0] * 100
print("Train cost:", cost)
print("Train accuracy: {}%".format(accuracy))

A_one_hot, cost = deep.evaluate(X_valid, Y_valid_one_hot)
A = one_hot_decode(A_one_hot)
accuracy = np.sum(Y_valid == A) / Y_valid.shape[0] * 100
print("Validation cost:", cost)
print("Validation accuracy: {}%".format(accuracy))

deep.save('27-output')

fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_valid_3D[i])
    plt.title(A[i])
    plt.axis('off')
plt.tight_layout()
plt.show()
ubuntu@alexa-ml:~$ ./27-main.py
Cost after 0 iterations: 0.4388904112857043
Cost after 10 iterations: 0.43778288041633584
Cost after 20 iterations: 0.43668839872612714
Cost after 30 iterations: 0.4356067473605946
Cost after 40 iterations: 0.4345377117680657
Cost after 50 iterations: 0.43348108159932525
Cost after 60 iterations: 0.43243665061046194
Cost after 70 iterations: 0.43140421656876826
Cost after 80 iterations: 0.43038358116155134
Cost after 90 iterations: 0.4293745499077263
Cost after 99 iterations: 0.4293745499077263
Train cost: 0.42837693207206456
Train accuracy: 88.442%
Validation cost: 0.39517557351173044
Validation accuracy: 89.64%

```



![12](2282_12.png)

*As you can see, our training has become very slow and is beginning to plateau. Let�s alter the model a little and see if we get a better result*<!--italics-NL-->

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `27-deep_neural_network.py`


---
### 28. All the Activations

Update the class <!--plain-NL-->`DeepNeuralNetwork`<!--inline-NL--> to allow different activation functions (based on <!--plain-NL-->`27-deep_neural_network.py`<!--inline-NL-->):<!--plain-NL-->

- Update the `__init__` method to `def __init__(self, nx, layers, activation='sig'):`

`activation` represents the type of activation function used in the hidden layers


`sig` represents a sigmoid activation
`tanh` represents a tanh activation
if `activation` is not `sig` or `tanh`, raise a `ValueError` with the exception: `activation must be 'sig' or 'tanh'`

Create the private attribute `__activation` and set it to the value of `activation`
Create a getter for the private attribute `__activation`
- `activation` represents the type of activation function used in the hidden layers


`sig` represents a sigmoid activation
`tanh` represents a tanh activation
if `activation` is not `sig` or `tanh`, raise a `ValueError` with the exception: `activation must be 'sig' or 'tanh'`
- `sig` represents a sigmoid activation
- `tanh` represents a tanh activation
- if `activation` is not `sig` or `tanh`, raise a `ValueError` with the exception: `activation must be 'sig' or 'tanh'`
- Create the private attribute `__activation` and set it to the value of `activation`
- Create a getter for the private attribute `__activation`
- Update the `forward_prop` and `gradient_descent` instance methods to use the `__activation` function in the hidden layers

- `activation` represents the type of activation function used in the hidden layers


`sig` represents a sigmoid activation
`tanh` represents a tanh activation
if `activation` is not `sig` or `tanh`, raise a `ValueError` with the exception: `activation must be 'sig' or 'tanh'`
- `sig` represents a sigmoid activation
- `tanh` represents a tanh activation
- if `activation` is not `sig` or `tanh`, raise a `ValueError` with the exception: `activation must be 'sig' or 'tanh'`
- Create the private attribute `__activation` and set it to the value of `activation`
- Create a getter for the private attribute `__activation`

- `sig` represents a sigmoid activation
- `tanh` represents a tanh activation
- if `activation` is not `sig` or `tanh`, raise a `ValueError` with the exception: `activation must be 'sig' or 'tanh'`

Because the training process takes such a long time, I have pre-trained a model for you to load and finish training (<!--plain-->[28-saved.pkl](https://s3.eu-west-3.amazonaws.com/hbtn.intranet.project.files/holbertonschool-ml/28-saved.pkl) <!--link-->). This model has already been trained for 2000 iterations.<!--plain-->

*The training process may take up to 5 minutes*<!--italics-NL-->

```
alexa@ubuntu-xenial:$ cat 28-main.py
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np

Deep27 = __import__('27-deep_neural_network').DeepNeuralNetwork
Deep28 = __import__('28-deep_neural_network').DeepNeuralNetwork
one_hot_encode = __import__('24-one_hot_encode').one_hot_encode
one_hot_decode = __import__('25-one_hot_decode').one_hot_decode

lib= np.load('../data/MNIST.npz')
X_train_3D = lib['X_train']
Y_train = lib['Y_train']
X_valid_3D = lib['X_valid']
Y_valid = lib['Y_valid']
X_test_3D = lib['X_test']
Y_test = lib['Y_test']
X_train = X_train_3D.reshape((X_train_3D.shape[0], -1)).T
X_valid = X_valid_3D.reshape((X_valid_3D.shape[0], -1)).T
X_test = X_test_3D.reshape((X_test_3D.shape[0], -1)).T
Y_train_one_hot = one_hot_encode(Y_train, 10)
Y_valid_one_hot = one_hot_encode(Y_valid, 10)
Y_test_one_hot = one_hot_encode(Y_test, 10)

print('Sigmoid activation:')
deep27 = Deep27.load('27-output.pkl')
A_one_hot27, cost27 = deep27.evaluate(X_train, Y_train_one_hot)
A27 = one_hot_decode(A_one_hot27)
accuracy27 = np.sum(Y_train == A27) / Y_train.shape[0] * 100
print("Train cost:", cost27)
print("Train accuracy: {}%".format(accuracy27))
A_one_hot27, cost27 = deep27.evaluate(X_valid, Y_valid_one_hot)
A27 = one_hot_decode(A_one_hot27)
accuracy27 = np.sum(Y_valid == A27) / Y_valid.shape[0] * 100
print("Validation cost:", cost27)
print("Validation accuracy: {}%".format(accuracy27))
A_one_hot27, cost27 = deep27.evaluate(X_test, Y_test_one_hot)
A27 = one_hot_decode(A_one_hot27)
accuracy27 = np.sum(Y_test == A27) / Y_test.shape[0] * 100
print("Test cost:", cost27)
print("Test accuracy: {}%".format(accuracy27))

fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_test_3D[i])
    plt.title(A27[i])
    plt.axis('off')
plt.tight_layout()
plt.show()

print('\nTanh activaiton:')

deep28 = Deep28.load('28-saved.pkl')
A_one_hot28, cost28 = deep28.train(X_train, Y_train_one_hot, iterations=100,
                                step=10, graph=False)
A28 = one_hot_decode(A_one_hot28)
accuracy28 = np.sum(Y_train == A28) / Y_train.shape[0] * 100
print("Train cost:", cost28)
print("Train accuracy: {}%".format(accuracy28))
A_one_hot28, cost28 = deep28.evaluate(X_valid, Y_valid_one_hot)
A28 = one_hot_decode(A_one_hot28)
accuracy28 = np.sum(Y_valid == A28) / Y_valid.shape[0] * 100
print("Validation cost:", cost28)
print("Validation accuracy: {}%".format(accuracy28))
A_one_hot28, cost28 = deep28.evaluate(X_test, Y_test_one_hot)
A28 = one_hot_decode(A_one_hot28)
accuracy28 = np.sum(Y_test == A28) / Y_test.shape[0] * 100
print("Test cost:", cost28)
print("Test accuracy: {}%".format(accuracy28))
deep28.save('28-output')

fig = plt.figure(figsize=(10, 10))
for i in range(100):
    fig.add_subplot(10, 10, i + 1)
    plt.imshow(X_test_3D[i])
    plt.title(A28[i])
    plt.axis('off')
plt.tight_layout()
plt.show()

alexa@ubuntu-xenial:$ ./28-main.py
Sigmoid activation:
Train cost: 0.42837693207206456
Train accuracy: 88.442%
Validation cost: 0.39517557351173044
Validation accuracy: 89.64%
Test cost: 0.4074169894615401
Test accuracy: 89.0%

```



![13](2282_13.png)

```
Tanh activaiton:
Cost after 0 iterations: 0.1806181562229199
Cost after 10 iterations: 0.18012009542718574
Cost after 20 iterations: 0.17962428978349268
Cost after 30 iterations: 0.17913072860418566
Cost after 40 iterations: 0.1786394012066576
Cost after 50 iterations: 0.17815029691267448
Cost after 60 iterations: 0.17766340504784378
Cost after 70 iterations: 0.1771787149412177
Cost after 80 iterations: 0.1766962159250237
Cost after 90 iterations: 0.17621589733451382
Train cost: 0.17573774850792664
Train accuracy: 95.006%
Validation cost: 0.1768930960039794
Validation accuracy: 95.13000000000001%
Test cost: 0.1809489808838737
Test accuracy: 94.77%

```



![14](2282_14.png)

*The training of this model is also getting slow and plateauing after about 2000 iterations. However, just by changing the activation function, we have nearly halved the model�s cost and increased its accuracy by about 6%*<!--italics-NL-->

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/classification`
- File: `28-deep_neural_network.py`


---
### 29. Blogpost

Write a blog post that explains the purpose of activation functions and compares and contrasts (at the minimum) the following functions:<!--plain-NL-->

- Binary
- Linear
- Sigmoid
- Tanh
- ReLU
- Softmax

Your posts should have examples and at least one picture, at the top. Publish your blog post on Medium or LinkedIn, and share it at least on LinkedIn.<!--plain-NL-->

When done, please add all URLs below (blog post, LinkedIn post, etc.)<!--plain-NL-->

Please, remember that these blogs must be written in English to further your technical ability in a variety of settings.<!--plain-NL-->