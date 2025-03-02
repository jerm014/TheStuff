# Project 2300: Tensorflow 2 & Keras
----


![1](2300_1.png)

## Resources

**Read or watch**:

* [TensorFlow 1 vs TensorFlow 2: Is the new TF better?](https://www.youtube.com/watch?v=t48a_KOh0fQ&ab_channel=365DataScience)
* [Differences Between Tensorflow 1.x and Tensorflow 2.0](https://www.youtube.com/watch?v=4NLlNx6wVaw&ab_channel=LazyProgrammer)
* [Keras Explained](https://www.youtube.com/watch?v=j_pJmXJwMLA&feature=youtu.be&t=228)(*starting at 3:48*)
* [Keras](https://www.tensorflow.org/guide/keras/sequential_model)
* [Keras vs. tf.keras: What’s the difference in TensorFlow 2.0?](https://pyimagesearch.com/2019/10/21/keras-vs-tf-keras-whats-the-difference-in-tensorflow-2-0/)
* [Hierarchical Data Format](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

**References**:

* [tf.keras](https://www.tensorflow.org/api_docs/python/tf/keras)
  * [tf.keras.models](https://www.tensorflow.org/api_docs/python/tf/keras/models)
  * [tf.keras.activations](https://www.tensorflow.org/api_docs/python/tf/keras/activations)
  * [tf.keras.callbacks](https://www.tensorflow.org/api_docs/python/tf/keras/callbacks)
  * [tf.keras.initializers](https://www.tensorflow.org/api_docs/python/tf/keras/initializers)
  * [tf.keras.layers](https://www.tensorflow.org/api_docs/python/tf/keras/layers)
  * [tf.keras.losses](https://www.tensorflow.org/api_docs/python/tf/keras/losses)
  * [tf.keras.metrics](https://www.tensorflow.org/api_docs/python/tf/keras/metrics)
  * [tf.keras.optimizers](https://www.tensorflow.org/api_docs/python/tf/keras/optimizers)
  * [tf.keras.regularizers](https://www.tensorflow.org/api_docs/python/tf/keras/regularizers)
  * [tf.keras.utils](https://www.tensorflow.org/api_docs/python/tf/keras/utils)
  * [serialization and saving](https://www.tensorflow.org/guide/keras/serialization_and_saving)

## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What is Keras?
* What is a model?
* How to instantiate a model (2 ways)
* How to build a layer
* How to add regularization to a layer
* How to add dropout to a layer
* How to add batch normalization
* How to compile a model
* How to optimize a model
* How to fit a model
* How to use validation data
* How to perform early stopping
* How to measure accuracy
* How to evaluate a model
* How to make a prediction with a model
* How to access the weights/outputs of a model
* What is HDF5?
* How to save and load a model’s weights, a model’s configuration, and the entire model
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`python3`(version 3.9)
* Your files will be executed with`numpy`(version 1.25.2) and`tensorflow`(version 2.15)
* All your files should end with a new line
* The first line of all your files should be exactly`#!/usr/bin/env python3`
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`pycodestyle`style (version 2.11.1)
* All your modules should have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions (inside and outside a class) should have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`and`python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* Unless otherwise noted, you are not allowed to import any module except`import tensorflow.keras as K`
* All your files must be executable
* The length of your files will be tested using`wc`

----
## Tasks
---
### 0. Sequential

Write a function <!--plain-NL-->`def build_model(nx, layers, activations, lambtha, keep_prob):`<!--inline-NL--> that builds a neural network with the Keras library:<!--plain-NL-->

- `nx` is the number of input features to the network
- `layers` is a list containing the number of nodes in each layer of the network
- `activations` is a list containing the activation functions used for each layer of the network
- `lambtha` is the L2 regularization parameter
- `keep_prob` is the probability that a node will be kept for dropout
- You are not allowed to use the `Input` class
- Returns: the keras model

```
ubuntu@alexa-ml:~/keras$ cat 0-main.py 
#!/usr/bin/env python3

# Force Seed - fix for Keras
SEED = 8

import os
os.environ['PYTHONHASHSEED'] = str(SEED)
os.environ['TF_ENABLE_ONEDNN_OPTS']= '0'
import random
random.seed(SEED)
import numpy as np
np.random.seed(SEED)
import tensorflow as tf
tf.random.set_seed(SEED)

build_model = __import__('0-sequential').build_model

if __name__ == '__main__':
    network = build_model(784, [256, 256, 10], ['tanh', 'tanh', 'softmax'], 0.001, 0.95)
    network.summary()
    print(network.losses)

ubuntu@alexa-ml:~/keras$ ./0-main.py 
Model: "sequential"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 dense (Dense)               (None, 256)               200960

 dropout (Dropout)           (None, 256)               0

 dense_1 (Dense)             (None, 256)               65792

 dropout_1 (Dropout)         (None, 256)               0

 dense_2 (Dense)             (None, 10)                2570

=================================================================
Total params: 269322 (1.03 MB)
Trainable params: 269322 (1.03 MB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________
[<tf.Tensor: shape=(), dtype=float32, numpy=0.3851098>, <tf.Tensor: shape=(), dtype=float32, numpy=0.25577578>, <tf.Tensor: shape=(), dtype=float32, numpy=0.019714147>]
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `0-sequential.py`


---
### 1. Input

Write a function <!--plain-NL-->`def build_model(nx, layers, activations, lambtha, keep_prob):`<!--inline-NL--> that builds a neural network with the Keras library:<!--plain-NL-->

- `nx` is the number of input features to the network
- `layers` is a list containing the number of nodes in each layer of the network
- `activations` is a list containing the activation functions used for each layer of the network
- `lambtha` is the L2 regularization parameter
- `keep_prob` is the probability that a node will be kept for dropout
- You are not allowed to use the `Sequential` class
- Returns: the keras model

```
ubuntu@alexa-ml:~/keras$ cat 1-main.py 
#!/usr/bin/env python3

# Force Seed - fix for Keras
SEED = 8

import os
os.environ['PYTHONHASHSEED'] = str(SEED)
os.environ['TF_ENABLE_ONEDNN_OPTS']= '0'
import random
random.seed(SEED)
import numpy as np
np.random.seed(SEED)
import tensorflow as tf
tf.random.set_seed(SEED)

build_model = __import__('1-input').build_model

if __name__ == '__main__':
    network = build_model(784, [256, 256, 10], ['tanh', 'tanh', 'softmax'], 0.001, 0.95)
    network.summary()
    print(network.losses)

ubuntu@alexa-ml:~/keras$ ./1-main.py 
Model: "model"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 input_1 (InputLayer)        [(None, 784)]             0

 dense (Dense)               (None, 256)               200960

 dropout (Dropout)           (None, 256)               0

 dense_1 (Dense)             (None, 256)               65792

 dropout_1 (Dropout)         (None, 256)               0

 dense_2 (Dense)             (None, 10)                2570

=================================================================
Total params: 269322 (1.03 MB)
Trainable params: 269322 (1.03 MB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________
[<tf.Tensor: shape=(), dtype=float32, numpy=0.3851098>, <tf.Tensor: shape=(), dtype=float32, numpy=0.25577578>, <tf.Tensor: shape=(), dtype=float32, numpy=0.019714147>]
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `1-input.py`


---
### 2. Optimize

Write a function <!--plain-NL-->`def optimize_model(network, alpha, beta1, beta2):`<!--inline-NL--> that sets up Adam optimization for a keras model with categorical crossentropy loss and accuracy metrics:<!--plain-NL-->

- `network` is the model to optimize
- `alpha` is the learning rate
- `beta1` is the first Adam optimization parameter
- `beta2` is the second Adam optimization parameter
- Returns: `None`

```
ubuntu@alexa-ml:~/keras$ cat 2-main.py 
#!/usr/bin/env python3

import tensorflow as tf

build_model = __import__('1-input').build_model
optimize_model = __import__('2-optimize').optimize_model

if __name__ == '__main__':
    model = build_model(784, [256, 256, 10], ['tanh', 'tanh', 'softmax'], 0.001, 0.95)
    optimize_model(model, 0.01, 0.99, 0.9)
    print(model.loss)
    opt = model.optimizer
    print(opt.__class__)
    print((opt.lr.numpy(), opt.beta_1, opt.beta_2))

ubuntu@alexa-ml:~/keras$ ./2-main.py 
categorical_crossentropy
<class 'keras.src.optimizers.adam.Adam'>
(0.01, 0.99, 0.9)
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `2-optimize.py`


---
### 3. One Hot

Write a function <!--plain-NL-->`def one_hot(labels, classes=None):`<!--inline-NL--> that converts a label vector into a one-hot matrix:<!--plain-NL-->

- The last dimension of the one-hot matrix must be the number of classes
- Returns: the one-hot matrix

```
ubuntu@alexa-ml:~/keras$ cat 3-main.py 
#!/usr/bin/env python3

import numpy as np
one_hot = __import__('3-one_hot').one_hot

if __name__ == '__main__':
    labels = np.load('MNIST.npz')['Y_train'][:10]
    print(labels)
    print(one_hot(labels))   

ubuntu@alexa-ml:~/keras$ ./3-main.py 
[5 0 4 1 9 2 1 3 1 4]
[[0. 0. 0. 0. 0. 1. 0. 0. 0. 0.]
 [1. 0. 0. 0. 0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 1. 0. 0. 0. 0. 0.]
 [0. 1. 0. 0. 0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0. 0. 0. 0. 0. 1.]
 [0. 0. 1. 0. 0. 0. 0. 0. 0. 0.]
 [0. 1. 0. 0. 0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 1. 0. 0. 0. 0. 0. 0.]
 [0. 1. 0. 0. 0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 1. 0. 0. 0. 0. 0.]]
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `3-one_hot.py`


---
### 4. Train

Write a function <!--plain-NL-->`def train_model(network, data, labels, batch_size, epochs, verbose=True, shuffle=False):`<!--inline-NL--> that trains a model using mini-batch gradient descent:<!--plain-NL-->

- `network` is the model to train
- `data` is a `numpy.ndarray` of shape `(m, nx)` containing the input data
- `labels` is a one-hot `numpy.ndarray` of shape `(m, classes)` containing the labels of `data`
- `batch_size` is the size of the batch used for mini-batch gradient descent
- `epochs` is the number of passes through `data` for mini-batch gradient descent
- `verbose` is a boolean that determines if output should be printed during training
- `shuffle` is a boolean that determines whether to shuffle the batches every epoch. Normally, it is a good idea to shuffle, but for reproducibility, we have chosen to set the default to `False`.
- Returns: the `History` object generated after training the model

```
ubuntu@alexa-ml:~/keras$ cat 4-main.py
#!/usr/bin/env python3
"""
Main file
"""

# Force Seed - fix for Keras
SEED = 8

import os
os.environ['PYTHONHASHSEED'] = str(SEED)
os.environ['TF_ENABLE_ONEDNN_OPTS']= '0'
import random
random.seed(SEED)
import numpy as np
np.random.seed(SEED)
import tensorflow as tf
tf.random.set_seed(SEED)


# Imports
build_model = __import__('1-input').build_model
optimize_model = __import__('2-optimize').optimize_model
one_hot = __import__('3-one_hot').one_hot
train_model = __import__('4-train').train_model


if __name__ == '__main__':
    datasets = np.load('MNIST.npz')
    X_train = datasets['X_train']
    X_train = X_train.reshape(X_train.shape[0], -1)
    Y_train = datasets['Y_train']
    Y_train_oh = one_hot(Y_train)

    lambtha = 0.0001
    keep_prob = 0.95
    network = build_model(784, [256, 256, 10], ['relu', 'relu', 'softmax'], lambtha, keep_prob)
    alpha = 0.001
    beta1 = 0.9
    beta2 = 0.999
    optimize_model(network, alpha, beta1, beta2)
    batch_size = 64
    epochs = 5   
    train_model(network, X_train, Y_train_oh, batch_size, epochs)

ubuntu@alexa-ml:~/keras$ ./4-main.py
Epoch 1/5
782/782 [==============================] - 6s 7ms/step - loss: 0.3262 - accuracy: 0.9205
Epoch 2/5
782/782 [==============================] - 4s 6ms/step - loss: 0.1745 - accuracy: 0.9653
Epoch 3/5
782/782 [==============================] - 4s 5ms/step - loss: 0.1411 - accuracy: 0.9758
Epoch 4/5
782/782 [==============================] - 6s 8ms/step - loss: 0.1245 - accuracy: 0.9804
Epoch 5/5
782/782 [==============================] - 5s 6ms/step - loss: 0.1155 - accuracy: 0.9832
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `4-train.py`


---
### 5. Validate

Based on <!--plain-NL-->`4-train.py`<!--inline-NL-->, update the function <!--plain-NL-->`def train_model(network, data, labels, batch_size, epochs, validation_data=None, verbose=True, shuffle=False):`<!--inline-NL--> to also analyze validaiton data:<!--plain-NL-->

- `validation_data` is the data to validate the model with, if not `None`

```
ubuntu@alexa-ml:~/keras$ cat 5-main.py 
#!/usr/bin/env python3
"""
Main file
"""

# Force Seed - fix for Keras
SEED = 8

import os
os.environ['PYTHONHASHSEED'] = str(SEED)
os.environ['TF_ENABLE_ONEDNN_OPTS']= '0'
import random
random.seed(SEED)
import numpy as np
np.random.seed(SEED)
import tensorflow as tf
tf.random.set_seed(SEED)


# Imports
build_model = __import__('1-input').build_model
optimize_model = __import__('2-optimize').optimize_model
one_hot = __import__('3-one_hot').one_hot
train_model = __import__('5-train').train_model

if __name__ == '__main__':
    datasets = np.load('MNIST.npz')
    X_train = datasets['X_train']
    X_train = X_train.reshape(X_train.shape[0], -1)
    Y_train = datasets['Y_train']
    Y_train_oh = one_hot(Y_train)
    X_valid = datasets['X_valid']
    X_valid = X_valid.reshape(X_valid.shape[0], -1)
    Y_valid = datasets['Y_valid']
    Y_valid_oh = one_hot(Y_valid)

    lambtha = 0.0001
    keep_prob = 0.95
    network = build_model(784, [256, 256, 10], ['relu', 'relu', 'softmax'], lambtha, keep_prob)
    alpha = 0.001
    beta1 = 0.9
    beta2 = 0.999
    optimize_model(network, alpha, beta1, beta2)
    batch_size = 64
    epochs = 5
    train_model(network, X_train, Y_train_oh, batch_size, epochs, validation_data=(X_valid, Y_valid_oh))

ubuntu@alexa-ml:~/keras$ ./5-main.py 
Epoch 1/5
782/782 [==============================] - 4s 5ms/step - loss: 0.3262 - accuracy: 0.9205 - val_loss: 0.1918 - val_accuracy: 0.9600
Epoch 2/5
782/782 [==============================] - 4s 6ms/step - loss: 0.1745 - accuracy: 0.9653 - val_loss: 0.1562 - val_accuracy: 0.9714
Epoch 3/5
782/782 [==============================] - 4s 5ms/step - loss: 0.1411 - accuracy: 0.9758 - val_loss: 0.1506 - val_accuracy: 0.9736
Epoch 4/5
782/782 [==============================] - 5s 6ms/step - loss: 0.1245 - accuracy: 0.9804 - val_loss: 0.1400 - val_accuracy: 0.9767
Epoch 5/5
782/782 [==============================] - 6s 8ms/step - loss: 0.1155 - accuracy: 0.9832 - val_loss: 0.1548 - val_accuracy: 0.9712
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `5-train.py`


---
### 6. Early Stopping

Based on <!--plain-NL-->`5-train.py`<!--inline-NL-->, update the function <!--plain-NL-->`def train_model(network, data, labels, batch_size, epochs, validation_data=None, early_stopping=False, patience=0, verbose=True, shuffle=False):`<!--inline-NL--> to also train the model using early stopping:<!--plain-NL-->

- `early_stopping` is a boolean that indicates whether early stopping should be used


early stopping should only be performed if `validation_data` exists
early stopping should be based on validation loss
- early stopping should only be performed if `validation_data` exists
- early stopping should be based on validation loss
- `patience` is the patience used for early stopping

- early stopping should only be performed if `validation_data` exists
- early stopping should be based on validation loss

```
ubuntu@alexa-ml:~/keras$ cat 6-main.py 
#!/usr/bin/env python3
"""
Main file
"""

# Force Seed - fix for Keras
SEED = 8

import os
os.environ['PYTHONHASHSEED'] = str(SEED)
os.environ['TF_ENABLE_ONEDNN_OPTS']= '0'
import random
random.seed(SEED)
import numpy as np
np.random.seed(SEED)
import tensorflow as tf
tf.random.set_seed(SEED)


# Imports
build_model = __import__('1-input').build_model
optimize_model = __import__('2-optimize').optimize_model
one_hot = __import__('3-one_hot').one_hot
train_model = __import__('6-train').train_model


if __name__ == '__main__':
    datasets = np.load('MNIST.npz')
    X_train = datasets['X_train']
    X_train = X_train.reshape(X_train.shape[0], -1)
    Y_train = datasets['Y_train']
    Y_train_oh = one_hot(Y_train)
    X_valid = datasets['X_valid']
    X_valid = X_valid.reshape(X_valid.shape[0], -1)
    Y_valid = datasets['Y_valid']
    Y_valid_oh = one_hot(Y_valid)

    lambtha = 0.0001
    keep_prob = 0.95
    network = build_model(784, [256, 256, 10], ['relu', 'relu', 'softmax'], lambtha, keep_prob)
    alpha = 0.001
    beta1 = 0.9
    beta2 = 0.999
    optimize_model(network, alpha, beta1, beta2)
    batch_size = 64
    epochs = 30
    train_model(network, X_train, Y_train_oh, batch_size, epochs,
                validation_data=(X_valid, Y_valid_oh), early_stopping=True,
                patience=3)

ubuntu@alexa-ml:~/keras$ ./6-main.py 
Epoch 1/30
782/782 [==============================] - 7s 8ms/step - loss: 0.3262 - accuracy: 0.9205 - val_loss: 0.1918 - val_accuracy: 0.9600
Epoch 2/30
782/782 [==============================] - 5s 6ms/step - loss: 0.1745 - accuracy: 0.9653 - val_loss: 0.1562 - val_accuracy: 0.9714
Epoch 3/30
782/782 [==============================] - 6s 7ms/step - loss: 0.1411 - accuracy: 0.9758 - val_loss: 0.1506 - val_accuracy: 0.9736
Epoch 4/30
782/782 [==============================] - 6s 7ms/step - loss: 0.1245 - accuracy: 0.9804 - val_loss: 0.1400 - val_accuracy: 0.9767
Epoch 5/30
782/782 [==============================] - 5s 6ms/step - loss: 0.1155 - accuracy: 0.9832 - val_loss: 0.1548 - val_accuracy: 0.9712
Epoch 6/30
782/782 [==============================] - 5s 6ms/step - loss: 0.1098 - accuracy: 0.9851 - val_loss: 0.1466 - val_accuracy: 0.9755
Epoch 7/30
782/782 [==============================] - 4s 6ms/step - loss: 0.1046 - accuracy: 0.9865 - val_loss: 0.1576 - val_accuracy: 0.9719
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `6-train.py`


---
### 7. Learning Rate Decay

Based on <!--plain-NL-->`6-train.py`<!--inline-NL-->, update the function <!--plain-NL-->`def train_model(network, data, labels, batch_size, epochs, validation_data=None, early_stopping=False, patience=0, learning_rate_decay=False, alpha=0.1, decay_rate=1, verbose=True, shuffle=False):`<!--inline-NL--> to also train the model with learning rate decay:<!--plain-NL-->

- `learning_rate_decay` is a boolean that indicates whether learning rate decay should be used


learning rate decay should only be performed if `validation_data` exists
the decay should be performed using inverse time decay
the learning rate should decay in a stepwise fashion after each epoch
each time the learning rate updates, `Keras` should print a message
- learning rate decay should only be performed if `validation_data` exists
- the decay should be performed using inverse time decay
- the learning rate should decay in a stepwise fashion after each epoch
- each time the learning rate updates, `Keras` should print a message
- `alpha` is the initial learning rate
- `decay_rate` is the decay rate

- learning rate decay should only be performed if `validation_data` exists
- the decay should be performed using inverse time decay
- the learning rate should decay in a stepwise fashion after each epoch
- each time the learning rate updates, `Keras` should print a message

```
ubuntu@alexa-ml:~/keras$ cat 7-main.py 
#!/usr/bin/env python3
"""
Main file
"""

# Force Seed - fix for Keras
SEED = 8

import os
os.environ['PYTHONHASHSEED'] = str(SEED)
os.environ['TF_ENABLE_ONEDNN_OPTS']= '0'
import random
random.seed(SEED)
import numpy as np
np.random.seed(SEED)
import tensorflow as tf
tf.random.set_seed(SEED)


# Imports
build_model = __import__('1-input').build_model
optimize_model = __import__('2-optimize').optimize_model
one_hot = __import__('3-one_hot').one_hot
train_model = __import__('7-train').train_model 

if __name__ == '__main__':
    datasets = np.load('MNIST.npz')
    X_train = datasets['X_train']
    X_train = X_train.reshape(X_train.shape[0], -1)
    Y_train = datasets['Y_train']
    Y_train_oh = one_hot(Y_train)
    X_valid = datasets['X_valid']
    X_valid = X_valid.reshape(X_valid.shape[0], -1)
    Y_valid = datasets['Y_valid']
    Y_valid_oh = one_hot(Y_valid)

    lambtha = 0.0001
    keep_prob = 0.95
    network = build_model(784, [256, 256, 10], ['relu', 'relu', 'softmax'], lambtha, keep_prob)
    alpha = 0.001
    beta1 = 0.9
    beta2 = 0.999
    optimize_model(network, alpha, beta1, beta2)
    batch_size = 64
    epochs = 1000
    train_model(network, X_train, Y_train_oh, batch_size, epochs,
                validation_data=(X_valid, Y_valid_oh), early_stopping=True,
                patience=3, learning_rate_decay=True, alpha=alpha)

ubuntu@alexa-ml:~/keras$ ./7-main.py

Epoch 1: LearningRateScheduler setting learning rate to 0.001.
Epoch 1/1000
782/782 [==============================] - 13s 15ms/step - loss: 0.3262 - accuracy: 0.9205 - val_loss: 0.1918 - val_accuracy: 0.9600 - lr: 0.0010

Epoch 2: LearningRateScheduler setting learning rate to 0.0005.
Epoch 2/1000
782/782 [==============================] - 7s 9ms/step - loss: 0.1589 - accuracy: 0.9695 - val_loss: 0.1455 - val_accuracy: 0.9752 - lr: 5.0000e-04

Epoch 3: LearningRateScheduler setting learning rate to 0.0003333333333333333.
Epoch 3/1000
782/782 [==============================] - 7s 9ms/step - loss: 0.1255 - accuracy: 0.9798 - val_loss: 0.1348 - val_accuracy: 0.9768 - lr: 3.3333e-04

Epoch 4: LearningRateScheduler setting learning rate to 0.00025.
Epoch 4/1000
782/782 [==============================] - 9s 11ms/step - loss: 0.1080 - accuracy: 0.9850 - val_loss: 0.1293 - val_accuracy: 0.9784 - lr: 2.5000e-04

Epoch 5: LearningRateScheduler setting learning rate to 0.0002.
Epoch 5/1000
782/782 [==============================] - 9s 11ms/step - loss: 0.0981 - accuracy: 0.9882 - val_loss: 0.1260 - val_accuracy: 0.9789 - lr: 2.0000e-04

...

Epoch 27: LearningRateScheduler setting learning rate to 3.7037037037037037e-05.
Epoch 27/1000
782/782 [==============================] - 4s 5ms/step - loss: 0.0547 - accuracy: 0.9985 - val_loss: 0.1046 - val_accuracy: 0.9818 - lr: 3.7037e-05

Epoch 28: LearningRateScheduler setting learning rate to 3.571428571428572e-05.
Epoch 28/1000
782/782 [==============================] - 4s 5ms/step - loss: 0.0540 - accuracy: 0.9986 - val_loss: 0.1043 - val_accuracy: 0.9822 - lr: 3.5714e-05

Epoch 29: LearningRateScheduler setting learning rate to 3.4482758620689657e-05.
Epoch 29/1000
782/782 [==============================] - 5s 6ms/step - loss: 0.0542 - accuracy: 0.9983 - val_loss: 0.1049 - val_accuracy: 0.9820 - lr: 3.4483e-05
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `7-train.py`


---
### 8. Save Only the Best

Based on <!--plain-NL-->`7-train.py`<!--inline-NL-->, update the function <!--plain-NL-->`def train_model(network, data, labels, batch_size, epochs, validation_data=None, early_stopping=False, patience=0, learning_rate_decay=False, alpha=0.1, decay_rate=1, save_best=False, filepath=None, verbose=True, shuffle=False):`<!--inline-NL--> to also save the best iteration of the model:<!--plain-NL-->

- `save_best` is a boolean indicating whether to save the model after each epoch if it is the best


a model is considered the best if its validation loss is the lowest that the model has obtained
- a model is considered the best if its validation loss is the lowest that the model has obtained
- `filepath` is the file path where the model should be saved

- a model is considered the best if its validation loss is the lowest that the model has obtained

```
ubuntu@alexa-ml:~/keras$ cat 8-main.py 
#!/usr/bin/env python3
"""
Main file
"""

# Force Seed - fix for Keras
SEED = 8

import os
os.environ['PYTHONHASHSEED'] = str(SEED)
os.environ['TF_ENABLE_ONEDNN_OPTS']= '0'
import random
random.seed(SEED)
import numpy as np
np.random.seed(SEED)
import tensorflow as tf
tf.random.set_seed(SEED)


# Imports
build_model = __import__('1-input').build_model
optimize_model = __import__('2-optimize').optimize_model
one_hot = __import__('3-one_hot').one_hot
train_model = __import__('8-train').train_model 


if __name__ == '__main__':
    datasets = np.load('MNIST.npz')
    X_train = datasets['X_train']
    X_train = X_train.reshape(X_train.shape[0], -1)
    Y_train = datasets['Y_train']
    Y_train_oh = one_hot(Y_train)
    X_valid = datasets['X_valid']
    X_valid = X_valid.reshape(X_valid.shape[0], -1)
    Y_valid = datasets['Y_valid']
    Y_valid_oh = one_hot(Y_valid)

    lambtha = 0.0001
    keep_prob = 0.95
    network = build_model(784, [256, 256, 10], ['relu', 'relu', 'softmax'], lambtha, keep_prob)
    alpha = 0.001
    beta1 = 0.9
    beta2 = 0.999
    optimize_model(network, alpha, beta1, beta2)
    batch_size = 64
    epochs = 1000
    train_model(network, X_train, Y_train_oh, batch_size, epochs,
                validation_data=(X_valid, Y_valid_oh), early_stopping=True,
                patience=3, learning_rate_decay=True, alpha=alpha,
                save_best=True, filepath='network1.keras')

ubuntu@alexa-ml:~/keras$ ./8-main.py 

Epoch 1: LearningRateScheduler setting learning rate to 0.001.
Epoch 1/1000
782/782 [==============================] - 10s 11ms/step - loss: 0.3262 - accuracy: 0.9205 - val_loss: 0.1918 - val_accuracy: 0.9600 - lr: 0.0010

Epoch 2: LearningRateScheduler setting learning rate to 0.0005.
Epoch 2/1000
782/782 [==============================] - 9s 12ms/step - loss: 0.1589 - accuracy: 0.9695 - val_loss: 0.1455 - val_accuracy: 0.9752 - lr: 5.0000e-04

Epoch 3: LearningRateScheduler setting learning rate to 0.0003333333333333333.
Epoch 3/1000
782/782 [==============================] - 10s 13ms/step - loss: 0.1255 - accuracy: 0.9798 - val_loss: 0.1348 - val_accuracy: 0.9768 - lr: 3.3333e-04

Epoch 4: LearningRateScheduler setting learning rate to 0.00025.
Epoch 4/1000
782/782 [==============================] - 8s 11ms/step - loss: 0.1080 - accuracy: 0.9850 - val_loss: 0.1293 - val_accuracy: 0.9784 - lr: 2.5000e-04

Epoch 5: LearningRateScheduler setting learning rate to 0.0002.
Epoch 5/1000
782/782 [==============================] - 10s 13ms/step - loss: 0.0981 - accuracy: 0.9882 - val_loss: 0.1260 - val_accuracy: 0.9789 - lr: 2.0000e-04

...

Epoch 27: LearningRateScheduler setting learning rate to 3.7037037037037037e-05.
Epoch 27/1000
782/782 [==============================] - 5s 6ms/step - loss: 0.0547 - accuracy: 0.9985 - val_loss: 0.1046 - val_accuracy: 0.9818 - lr: 3.7037e-05

Epoch 28: LearningRateScheduler setting learning rate to 3.571428571428572e-05.
Epoch 28/1000
782/782 [==============================] - 4s 6ms/step - loss: 0.0540 - accuracy: 0.9986 - val_loss: 0.1043 - val_accuracy: 0.9822 - lr: 3.5714e-05

Epoch 29: LearningRateScheduler setting learning rate to 3.4482758620689657e-05.
Epoch 29/1000
782/782 [==============================] - 5s 6ms/step - loss: 0.0542 - accuracy: 0.9983 - val_loss: 0.1049 - val_accuracy: 0.9820 - lr: 3.4483e-05
ubuntu@alexa-ml:~/keras$ ls network1.keras
network1.keras
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `8-train.py`


---
### 9. Save and Load Model

Write the following functions:<!--plain-NL-->

- `def save_model(network, filename):` saves an entire model:


`network` is the model to save
`filename` is the path of the file that the model should be saved to
Returns: `None`
- `network` is the model to save
- `filename` is the path of the file that the model should be saved to
- Returns: `None`
- `def load_model(filename):` loads an entire model:


`filename` is the path of the file that the model should be loaded from
Returns: the loaded model
- `filename` is the path of the file that the model should be loaded from
- Returns: the loaded model

- `network` is the model to save
- `filename` is the path of the file that the model should be saved to
- Returns: `None`

- `filename` is the path of the file that the model should be loaded from
- Returns: the loaded model

```
ubuntu@alexa-ml:~/keras$ cat 9-main.py
#!/usr/bin/env python3
"""
Main file
"""

# Force Seed - fix for Keras
SEED = 8

import os
os.environ['PYTHONHASHSEED'] = str(SEED)
os.environ['TF_ENABLE_ONEDNN_OPTS']= '0'
import random
random.seed(SEED)
import numpy as np
np.random.seed(SEED)
import tensorflow as tf
tf.random.set_seed(SEED)


# Imports
one_hot = __import__('3-one_hot').one_hot
train_model = __import__('8-train').train_model 
model = __import__('9-model')

if __name__ == '__main__':
    datasets = np.load('MNIST.npz')
    X_train = datasets['X_train']
    X_train = X_train.reshape(X_train.shape[0], -1)
    Y_train = datasets['Y_train']
    Y_train_oh = one_hot(Y_train)
    X_valid = datasets['X_valid']
    X_valid = X_valid.reshape(X_valid.shape[0], -1)
    Y_valid = datasets['Y_valid']
    Y_valid_oh = one_hot(Y_valid)

    network = model.load_model('network1.keras')
    batch_size = 32
    epochs = 1000
    train_model(network, X_train, Y_train_oh, batch_size, epochs,
                validation_data=(X_valid, Y_valid_oh), early_stopping=True,
                patience=2, learning_rate_decay=True, alpha=0.001)
    model.save_model(network, 'network2.keras')
    network.summary()
    print(network.get_weights())
    del network

    network2 = model.load_model('network2.keras')
    network2.summary()
    print(network2.get_weights())

ubuntu@alexa-ml:~/keras$ ./9-main.py

Epoch 1: LearningRateScheduler setting learning rate to 0.001.
Epoch 1/1000
1563/1563 [==============================] - 9s 5ms/step - loss: 0.1795 - accuracy: 0.9635 - val_loss: 0.1616 - val_accuracy: 0.9713 - lr: 0.0010

Epoch 2: LearningRateScheduler setting learning rate to 0.0005.
Epoch 2/1000
1563/1563 [==============================] - 12s 8ms/step - loss: 0.1070 - accuracy: 0.9856 - val_loss: 0.1349 - val_accuracy: 0.9781 - lr: 5.0000e-04

Epoch 3: LearningRateScheduler setting learning rate to 0.0003333333333333333.
Epoch 3/1000
1563/1563 [==============================] - 9s 6ms/step - loss: 0.0840 - accuracy: 0.9918 - val_loss: 0.1235 - val_accuracy: 0.9800 - lr: 3.3333e-04

Epoch 4: LearningRateScheduler setting learning rate to 0.00025.
Epoch 4/1000
1563/1563 [==============================] - 8s 5ms/step - loss: 0.0737 - accuracy: 0.9939 - val_loss: 0.1154 - val_accuracy: 0.9810 - lr: 2.5000e-04

Epoch 5: LearningRateScheduler setting learning rate to 0.0002.
Epoch 5/1000
1563/1563 [==============================] - 8s 5ms/step - loss: 0.0669 - accuracy: 0.9957 - val_loss: 0.1153 - val_accuracy: 0.9801 - lr: 2.0000e-04

Epoch 6: LearningRateScheduler setting learning rate to 0.00016666666666666666.
Epoch 6/1000
1563/1563 [==============================] - 8s 5ms/step - loss: 0.0623 - accuracy: 0.9965 - val_loss: 0.1112 - val_accuracy: 0.9816 - lr: 1.6667e-04

Epoch 7: LearningRateScheduler setting learning rate to 0.00014285714285714287.
Epoch 7/1000
1563/1563 [==============================] - 8s 5ms/step - loss: 0.0587 - accuracy: 0.9970 - val_loss: 0.1064 - val_accuracy: 0.9813 - lr: 1.4286e-04

Epoch 8: LearningRateScheduler setting learning rate to 0.000125.
Epoch 8/1000
1563/1563 [==============================] - 9s 6ms/step - loss: 0.0566 - accuracy: 0.9975 - val_loss: 0.1048 - val_accuracy: 0.9832 - lr: 1.2500e-04

Epoch 9: LearningRateScheduler setting learning rate to 0.00011111111111111112.
Epoch 9/1000
1563/1563 [==============================] - 9s 6ms/step - loss: 0.0539 - accuracy: 0.9978 - val_loss: 0.1065 - val_accuracy: 0.9819 - lr: 1.1111e-04

Epoch 10: LearningRateScheduler setting learning rate to 0.0001.
Epoch 10/1000
1563/1563 [==============================] - 11s 7ms/step - loss: 0.0523 - accuracy: 0.9981 - val_loss: 0.1030 - val_accuracy: 0.9833 - lr: 1.0000e-04

Epoch 11: LearningRateScheduler setting learning rate to 9.090909090909092e-05.
Epoch 11/1000
1563/1563 [==============================] - 9s 6ms/step - loss: 0.0513 - accuracy: 0.9981 - val_loss: 0.0994 - val_accuracy: 0.9832 - lr: 9.0909e-05

Epoch 12: LearningRateScheduler setting learning rate to 8.333333333333333e-05.
Epoch 12/1000
1563/1563 [==============================] - 10s 6ms/step - loss: 0.0498 - accuracy: 0.9985 - val_loss: 0.1002 - val_accuracy: 0.9825 - lr: 8.3333e-05

Epoch 13: LearningRateScheduler setting learning rate to 7.692307692307693e-05.
Epoch 13/1000
1563/1563 [==============================] - 10s 6ms/step - loss: 0.0494 - accuracy: 0.9981 - val_loss: 0.0969 - val_accuracy: 0.9837 - lr: 7.6923e-05

Epoch 14: LearningRateScheduler setting learning rate to 7.142857142857143e-05.
Epoch 14/1000
1563/1563 [==============================] - 10s 7ms/step - loss: 0.0479 - accuracy: 0.9988 - val_loss: 0.0966 - val_accuracy: 0.9833 - lr: 7.1429e-05

Epoch 15: LearningRateScheduler setting learning rate to 6.666666666666667e-05.
Epoch 15/1000
1563/1563 [==============================] - 11s 7ms/step - loss: 0.0474 - accuracy: 0.9985 - val_loss: 0.0960 - val_accuracy: 0.9837 - lr: 6.6667e-05

Epoch 16: LearningRateScheduler setting learning rate to 6.25e-05.
Epoch 16/1000
1563/1563 [==============================] - 8s 5ms/step - loss: 0.0461 - accuracy: 0.9989 - val_loss: 0.0955 - val_accuracy: 0.9831 - lr: 6.2500e-05

Epoch 17: LearningRateScheduler setting learning rate to 5.882352941176471e-05.
Epoch 17/1000
1563/1563 [==============================] - 13s 9ms/step - loss: 0.0460 - accuracy: 0.9989 - val_loss: 0.0933 - val_accuracy: 0.9835 - lr: 5.8824e-05

Epoch 18: LearningRateScheduler setting learning rate to 5.555555555555556e-05.
Epoch 18/1000
1563/1563 [==============================] - 10s 6ms/step - loss: 0.0454 - accuracy: 0.9990 - val_loss: 0.0932 - val_accuracy: 0.9837 - lr: 5.5556e-05

Epoch 19: LearningRateScheduler setting learning rate to 5.2631578947368424e-05.
Epoch 19/1000
1563/1563 [==============================] - 10s 6ms/step - loss: 0.0443 - accuracy: 0.9993 - val_loss: 0.0929 - val_accuracy: 0.9843 - lr: 5.2632e-05

Epoch 20: LearningRateScheduler setting learning rate to 5e-05.
Epoch 20/1000
1563/1563 [==============================] - 9s 6ms/step - loss: 0.0445 - accuracy: 0.9987 - val_loss: 0.0925 - val_accuracy: 0.9837 - lr: 5.0000e-05

Epoch 21: LearningRateScheduler setting learning rate to 4.761904761904762e-05.
Epoch 21/1000
1563/1563 [==============================] - 9s 6ms/step - loss: 0.0438 - accuracy: 0.9993 - val_loss: 0.0938 - val_accuracy: 0.9834 - lr: 4.7619e-05

Epoch 22: LearningRateScheduler setting learning rate to 4.545454545454546e-05.
Epoch 22/1000
1563/1563 [==============================] - 9s 6ms/step - loss: 0.0434 - accuracy: 0.9990 - val_loss: 0.0911 - val_accuracy: 0.9836 - lr: 4.5455e-05

Epoch 23: LearningRateScheduler setting learning rate to 4.347826086956522e-05.
Epoch 23/1000
1563/1563 [==============================] - 10s 6ms/step - loss: 0.0434 - accuracy: 0.9989 - val_loss: 0.0924 - val_accuracy: 0.9828 - lr: 4.3478e-05

Epoch 24: LearningRateScheduler setting learning rate to 4.1666666666666665e-05.
Epoch 24/1000
1563/1563 [==============================] - 10s 6ms/step - loss: 0.0426 - accuracy: 0.9991 - val_loss: 0.0920 - val_accuracy: 0.9832 - lr: 4.1667e-05
Model: "model"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 input_1 (InputLayer)        [(None, 784)]             0

 dense (Dense)               (None, 256)               200960

 dropout (Dropout)           (None, 256)               0

 dense_1 (Dense)             (None, 256)               65792

 dropout_1 (Dropout)         (None, 256)               0

 dense_2 (Dense)             (None, 10)                2570

=================================================================
Total params: 269322 (1.03 MB)
Trainable params: 269322 (1.03 MB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________
[array([[ 4.9656790e-32,  4.3917174e-32, -4.8977366e-32, ...,
        -4.5926517e-32,  8.6207582e-33, -1.3832739e-32],
       [ 4.6782477e-32,  5.5539886e-32, -5.7079079e-32, ...,
         5.5577202e-32,  1.4002830e-32, -3.9161465e-32],
       [-2.0177172e-32,  4.2760376e-32,  7.1549836e-33, ...,
         5.3708507e-32, -4.6761471e-32, -4.8687718e-32],
       ...,
       [-1.9896182e-32,  5.0971551e-33, -1.4021029e-32, ...,
         5.2524661e-32, -2.3340851e-33, -2.9050051e-33],
       [ 1.8921073e-32,  4.7803047e-32, -8.6395426e-33, ...,
        -5.2557293e-32, -4.4593013e-32, -4.0252541e-32],
       [-5.1641583e-33, -5.3305178e-32, -1.7745671e-32, ...,
        -4.8143899e-33,  1.4154974e-32, -4.2641681e-32]], dtype=float32), array([-1.75625160e-02,  2.38614380e-02, -3.84415276e-02, -1.07868770e-02,
       -2.52650231e-02,  3.68613228e-02,  1.73959732e-02, -1.82547960e-02,
       -2.59543844e-02,  2.32362393e-02, -3.85221317e-02,  2.47119442e-02,
        6.42312169e-02, -2.31926851e-02,  6.15435243e-02,  5.50865792e-02,
       -1.25715164e-02, -4.63420972e-02,  7.89976865e-02,  2.94253393e-03,
       -1.02322079e-01, -1.38261355e-02, -2.68811565e-02, -5.21523729e-02,
        8.07127431e-02,  4.56745587e-02,  1.63595885e-01, -3.63889113e-02,
       -6.77807331e-02,  6.62615569e-03, -1.50769837e-02,  7.68990293e-02,
       -6.26982236e-03, -2.89552901e-02, -2.42170170e-02,  1.04601808e-01,
       -2.80837975e-02, -3.57521027e-02, -1.07769771e-02,  7.09208995e-02,
        7.45427012e-02,  1.82902720e-02, -4.78790738e-02, -3.45297158e-02,
       -7.53630511e-03, -2.55092774e-02,  2.25215089e-02, -2.16000769e-02,
       -3.93025316e-02,  1.77104957e-02,  5.75819798e-02,  2.16920618e-02,
       -1.22017674e-02,  4.11647419e-03,  2.73455400e-02,  6.67569116e-02,
       -1.87870394e-03, -2.81154569e-02,  5.33470213e-02,  8.15945566e-02,
        1.03007048e-01, -7.18834698e-02,  7.43013769e-02, -3.95426713e-02,
       -7.09563028e-03,  2.95166988e-02, -4.18169498e-02, -3.08827106e-02,
       -1.00774597e-02,  1.58848669e-02, -6.19071834e-02,  9.93519207e-04,
        1.29316133e-02, -4.55454719e-04,  4.42109779e-02, -7.97727481e-02,
        1.59326214e-02,  2.01745257e-02,  2.68713459e-02,  1.06956057e-01,
        5.98613694e-02,  9.75977182e-02, -3.21767032e-02,  3.55101307e-03,
       -2.18588188e-02, -3.38149257e-02, -1.18252065e-03, -6.49806783e-02,
        1.04250886e-01, -8.27167705e-02, -7.89505467e-02,  6.92818873e-03,
       -3.55526023e-02,  3.17099653e-02, -1.40522674e-01,  1.29687846e-01,
       -7.20400363e-02, -3.75990979e-02, -4.31945585e-02,  8.67470913e-03,
       -1.66965201e-02, -5.95600381e-02, -8.46499577e-02, -2.77765077e-02,
       -2.85331681e-02, -3.59828360e-02,  4.52273116e-02, -2.36150785e-03,
       -4.54839505e-02, -1.84390731e-02, -1.96880996e-02,  3.04260198e-02,
        5.68410717e-02, -1.20003652e-02, -1.64393000e-02,  4.91620228e-03,
        7.45085329e-02, -1.21694077e-02, -1.99243315e-02,  6.59814775e-02,
       -4.13557291e-02,  2.49204803e-02, -1.17288651e-02,  3.34597491e-02,
        3.43753546e-02, -6.98342361e-03,  1.47913839e-03, -2.42696293e-02,
       -1.43720470e-02, -1.74468700e-02,  4.07791398e-02,  3.15824412e-02,
        2.22639591e-02, -1.21490052e-02,  4.43179300e-03,  3.10461912e-02,
       -3.69075537e-02, -5.08116074e-02,  1.17415354e-01, -3.64092812e-02,
        1.85413416e-02, -9.89102423e-02,  4.89672683e-02, -9.68448166e-03,
        1.96690224e-02,  4.71767113e-02, -9.94545445e-02, -6.75309524e-02,
       -4.36580693e-03,  3.97164561e-02,  7.25484118e-02,  4.54341760e-04,
       -3.67116258e-02,  1.86359398e-02,  7.73076117e-02,  9.88827422e-02,
        3.31477597e-02,  8.67311954e-02, -3.02941557e-02, -3.76639552e-02,
        8.27071443e-02, -7.56450072e-02, -2.41178218e-02,  4.66995463e-02,
       -3.68905924e-02,  3.97340842e-02,  5.69537319e-02, -6.86988421e-03,
        3.82982753e-02, -8.97749215e-02, -3.44097577e-02, -6.42272234e-02,
        2.52821706e-02, -4.53554802e-02, -4.21960801e-02, -3.66484113e-02,
       -1.50382370e-02, -2.95945513e-03, -6.37735415e-04, -5.70940636e-02,
       -5.70005849e-02,  2.47773472e-02,  4.54030894e-02, -5.58227971e-02,
       -1.25297522e-02, -6.58111125e-02,  8.56711417e-02, -4.69941050e-02,
        2.02306360e-02,  2.55649653e-03, -1.76524222e-02,  1.48931984e-02,
       -1.41139189e-02, -3.94307002e-02, -4.65882495e-02, -1.01299686e-02,
        4.20647450e-02, -2.35837139e-02, -7.87560493e-02, -1.12320026e-02,
        5.44794649e-02, -3.80145498e-02, -4.74508293e-03, -7.19793290e-02,
       -5.54356836e-02,  2.96915658e-02,  5.18085025e-02,  8.78287628e-02,
        1.76864248e-02,  1.92190129e-02,  3.57445627e-02,  6.47621648e-03,
        2.79603563e-02, -2.16989107e-02, -1.79182030e-02,  1.40695333e-01,
       -1.07239494e-02,  7.65939578e-02, -1.50439062e-03,  2.37921402e-02,
        1.54382298e-02, -4.04764004e-02, -4.01846282e-02,  2.58538127e-02,
       -7.82667100e-03,  7.86434337e-02, -4.15743701e-03, -3.96438263e-04,
       -5.80447577e-02,  1.88093796e-01,  7.73134157e-02,  9.24269259e-02,
       -2.82247923e-02, -6.81674555e-02,  1.04359360e-02,  1.07250646e-01,
        6.41890848e-03,  3.06504779e-02, -4.73784767e-02,  4.60019149e-02,
        3.00909989e-02,  4.80746478e-02, -1.39184352e-02, -1.08398564e-01,
        1.57273598e-02, -8.50313157e-02,  4.29840945e-02, -4.16836403e-02,
       -3.66492495e-02, -9.13757905e-02, -7.68706053e-02, -4.60796580e-02,
        4.32244539e-02,  1.60541255e-02,  1.30462940e-05, -6.56545116e-03],
      dtype=float32), array([[-4.5997430e-02,  3.9724290e-02, -1.3397273e-02, ...,
        -7.5473256e-02,  8.8088233e-03, -9.4537415e-02],
       [ 2.8984664e-02,  8.0262288e-02, -4.0608842e-02, ...,
        -1.0203673e-01,  2.2942042e-02, -2.6878027e-02],
       [ 3.0804440e-02,  1.1548622e-01, -2.5646241e-02, ...,
        -3.8015328e-03,  2.5274275e-02, -6.3170046e-02],
       ...,
       [ 2.7550068e-02,  1.2686612e-01, -1.0378199e-02, ...,
        -8.5032023e-03,  2.4102896e-02, -3.0741006e-02],
       [ 4.5107488e-02,  3.2530397e-02, -4.2936575e-02, ...,
         5.8845215e-02,  1.1548084e-01,  5.3854853e-02],
       [-5.3364815e-31,  5.8101564e-31, -5.6213419e-31, ...,
         5.5438613e-31, -5.7799791e-31,  5.5831303e-31]], dtype=float32), array([ 4.59229499e-02,  1.42772272e-01, -1.72097571e-02,  1.56033024e-01,
        4.56781611e-02,  4.68072705e-02,  1.72208771e-01,  1.50796011e-01,
        1.30147636e-01,  1.88945219e-01,  6.87050298e-02,  5.30313067e-02,
       -3.15672718e-02,  1.25964075e-01,  4.45851423e-02,  1.23975780e-02,
        1.20336473e-01,  2.54543964e-02, -2.47216988e-02, -1.29715316e-02,
       -1.97745916e-02,  6.54436275e-02, -6.87990636e-02,  9.35242549e-02,
       -2.06978451e-02, -4.54364270e-02,  9.12649482e-02,  5.82153015e-02,
        1.30326539e-01,  2.82189921e-02,  1.39028266e-01, -1.97611712e-02,
        3.61321680e-02,  1.81861922e-01, -2.37019379e-02,  5.25296964e-02,
       -4.98479642e-02,  1.27283052e-01, -2.93462109e-02, -2.89733689e-02,
        9.22334567e-02,  1.01390816e-01,  1.02031261e-01,  4.33292612e-02,
        1.12845898e-01, -1.89257134e-02,  4.04454581e-02,  1.05000898e-01,
        1.07168272e-01,  4.29851897e-02, -1.87522881e-02,  7.02546835e-02,
       -1.39709786e-02, -1.99081525e-02,  8.47429559e-02,  2.12942269e-02,
        3.94135434e-03,  7.34297112e-02,  6.41163290e-02,  3.48262675e-02,
        1.07542396e-01,  6.66825473e-02,  6.32665157e-02,  3.00869774e-02,
        4.32115495e-02,  1.60349563e-01, -7.06749111e-02,  3.69371213e-02,
       -6.83237761e-02, -3.63985710e-02,  8.15328117e-03, -5.93466237e-02,
        1.36982918e-01,  1.35196671e-01,  5.95793221e-03,  1.64357647e-01,
       -4.05739844e-02,  2.48681568e-02, -4.74792197e-02, -3.02808397e-02,
       -2.17252839e-02,  4.95546237e-02,  1.00808181e-01, -1.33082978e-02,
        3.71380597e-02, -6.73180521e-02,  3.31788622e-02, -2.10716482e-02,
        2.53368970e-02,  1.10705756e-01,  9.02492478e-02,  1.53050929e-01,
        1.05277948e-01, -7.85541907e-03,  1.66880116e-01,  2.79654339e-02,
        6.93125501e-02,  2.88134650e-03,  7.96954632e-02,  6.40256051e-03,
       -4.97197285e-02, -3.35000455e-02,  3.90239395e-02,  5.57232387e-02,
       -4.40557227e-02,  1.58747748e-01,  1.04127876e-01, -1.56791136e-02,
       -7.22720521e-03,  7.48040155e-02, -2.00373726e-03,  1.32099003e-01,
        9.11661908e-02,  1.71629060e-02,  4.69528325e-02,  7.41026597e-03,
       -2.68851686e-02, -2.73385569e-02,  8.17873329e-03,  2.17585247e-02,
       -6.71064630e-02,  7.51386210e-02, -1.71873402e-02,  1.59057379e-01,
        2.44248956e-02,  1.05590306e-01,  8.24843347e-02, -1.67889725e-02,
       -3.21964659e-02,  1.46952018e-01, -4.20108549e-02,  2.69232858e-02,
        4.56483802e-03, -2.16609426e-02, -3.51020582e-02,  9.60301235e-02,
       -6.69141039e-02,  6.10258020e-02, -1.13274492e-02,  5.53947575e-02,
        9.54231918e-02,  4.76127230e-02,  1.23572797e-01,  7.83822164e-02,
        8.32578391e-02,  2.38968618e-02, -5.58536425e-02,  1.77204292e-02,
        1.38252586e-01,  6.94604442e-02,  7.09299594e-02, -5.20773642e-02,
        1.76198244e-01, -4.92898189e-02, -4.17218693e-02,  1.09242305e-01,
       -6.76132180e-03,  4.28602509e-02,  1.68294594e-01,  1.68386742e-01,
       -5.76385856e-02,  9.84097645e-02,  1.48191974e-01, -2.84406953e-02,
        1.42889440e-01,  1.84281878e-02,  1.93440303e-01,  3.76270078e-02,
        1.67220771e-01,  6.34078011e-02,  8.44985992e-03,  1.40222445e-01,
        6.78402409e-02, -1.44842481e-02,  4.58042733e-02,  3.29661928e-02,
        8.96665305e-02,  1.65626317e-01, -2.77456138e-02,  1.07176133e-01,
        8.78257602e-02, -5.40350098e-03, -8.41083284e-03, -4.08283398e-02,
       -2.99310815e-02,  1.18130043e-01, -1.50466163e-04,  1.67059392e-01,
        1.96807176e-01,  1.47676244e-01, -2.13360190e-02,  1.74955040e-01,
        6.27517924e-02, -1.83805451e-02,  8.38876888e-02, -2.03164108e-02,
        9.73259583e-02,  1.54831246e-01,  8.89534317e-03,  1.52697966e-01,
       -4.68331352e-02, -2.55660061e-02, -3.76809016e-02,  2.99420245e-02,
        1.71439588e-01, -3.43420729e-02,  1.65894732e-01,  1.56399328e-02,
       -2.66216993e-02,  1.54767722e-01,  5.29400632e-02,  8.65736529e-02,
        9.96439382e-02,  4.54599829e-03,  2.00976115e-02,  8.27111378e-02,
        4.71463166e-02,  5.26427031e-02,  8.41828659e-02,  6.93706796e-02,
       -4.50787246e-02,  1.16726995e-01, -4.24910756e-03,  1.14290779e-02,
        6.96549565e-02,  2.13756170e-02,  3.40374783e-02,  9.86892283e-02,
        3.76018360e-02,  8.91576707e-02, -4.86361347e-02,  6.16077743e-02,
        2.16929186e-02,  1.46149129e-01, -3.51966955e-02,  1.37653038e-01,
       -2.16989443e-02,  1.55914709e-01, -1.56704914e-02,  2.06916183e-02,
        1.32328793e-01,  1.13750182e-01,  5.18698692e-02, -3.82212996e-02,
        1.14233382e-01,  3.95671725e-02,  1.22629190e-02,  8.59811008e-02,
       -1.95367951e-02,  1.04966071e-02,  3.77094708e-02, -1.00103940e-03,
        7.25086480e-02,  1.66858256e-01,  2.27597103e-01,  1.47489741e-01],
      dtype=float32), array([[-0.08476736, -0.1764006 , -0.02580684, ...,  0.00646442,
         0.05702282,  0.01345878],
       [-0.152402  , -0.06106262,  0.1726747 , ...,  0.0412994 ,
         0.22838612, -0.4059306 ],
       [ 0.24278152, -0.04385173, -0.16811378, ...,  0.25357112,
        -0.12283809, -0.29232424],
       ...,
       [ 0.11379576,  0.1648541 , -0.05916017, ..., -0.26861203,
         0.23434496,  0.13696764],
       [ 0.1736983 , -0.1937701 ,  0.09263327, ..., -0.22861221,
         0.17688444, -0.27816498],
       [-0.13327701, -0.22805803, -0.05980655, ..., -0.20988573,
         0.19641885,  0.2544963 ]], dtype=float32), array([-0.00973917, -0.07873288, -0.002357  , -0.03964433,  0.02684775,
       -0.0314567 , -0.08538326, -0.07465444,  0.18579467,  0.02639077],
      dtype=float32)]
Model: "model"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 input_1 (InputLayer)        [(None, 784)]             0

 dense (Dense)               (None, 256)               200960

 dropout (Dropout)           (None, 256)               0

 dense_1 (Dense)             (None, 256)               65792

 dropout_1 (Dropout)         (None, 256)               0

 dense_2 (Dense)             (None, 10)                2570

=================================================================
Total params: 269322 (1.03 MB)
Trainable params: 269322 (1.03 MB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________
[array([[ 4.9656790e-32,  4.3917174e-32, -4.8977366e-32, ...,
        -4.5926517e-32,  8.6207582e-33, -1.3832739e-32],
       [ 4.6782477e-32,  5.5539886e-32, -5.7079079e-32, ...,
         5.5577202e-32,  1.4002830e-32, -3.9161465e-32],
       [-2.0177172e-32,  4.2760376e-32,  7.1549836e-33, ...,
         5.3708507e-32, -4.6761471e-32, -4.8687718e-32],
       ...,
       [-1.9896182e-32,  5.0971551e-33, -1.4021029e-32, ...,
         5.2524661e-32, -2.3340851e-33, -2.9050051e-33],
       [ 1.8921073e-32,  4.7803047e-32, -8.6395426e-33, ...,
        -5.2557293e-32, -4.4593013e-32, -4.0252541e-32],
       [-5.1641583e-33, -5.3305178e-32, -1.7745671e-32, ...,
        -4.8143899e-33,  1.4154974e-32, -4.2641681e-32]], dtype=float32), array([-1.75625160e-02,  2.38614380e-02, -3.84415276e-02, -1.07868770e-02,
       -2.52650231e-02,  3.68613228e-02,  1.73959732e-02, -1.82547960e-02,
       -2.59543844e-02,  2.32362393e-02, -3.85221317e-02,  2.47119442e-02,
        6.42312169e-02, -2.31926851e-02,  6.15435243e-02,  5.50865792e-02,
       -1.25715164e-02, -4.63420972e-02,  7.89976865e-02,  2.94253393e-03,
       -1.02322079e-01, -1.38261355e-02, -2.68811565e-02, -5.21523729e-02,
        8.07127431e-02,  4.56745587e-02,  1.63595885e-01, -3.63889113e-02,
       -6.77807331e-02,  6.62615569e-03, -1.50769837e-02,  7.68990293e-02,
       -6.26982236e-03, -2.89552901e-02, -2.42170170e-02,  1.04601808e-01,
       -2.80837975e-02, -3.57521027e-02, -1.07769771e-02,  7.09208995e-02,
        7.45427012e-02,  1.82902720e-02, -4.78790738e-02, -3.45297158e-02,
       -7.53630511e-03, -2.55092774e-02,  2.25215089e-02, -2.16000769e-02,
       -3.93025316e-02,  1.77104957e-02,  5.75819798e-02,  2.16920618e-02,
       -1.22017674e-02,  4.11647419e-03,  2.73455400e-02,  6.67569116e-02,
       -1.87870394e-03, -2.81154569e-02,  5.33470213e-02,  8.15945566e-02,
        1.03007048e-01, -7.18834698e-02,  7.43013769e-02, -3.95426713e-02,
       -7.09563028e-03,  2.95166988e-02, -4.18169498e-02, -3.08827106e-02,
       -1.00774597e-02,  1.58848669e-02, -6.19071834e-02,  9.93519207e-04,
        1.29316133e-02, -4.55454719e-04,  4.42109779e-02, -7.97727481e-02,
        1.59326214e-02,  2.01745257e-02,  2.68713459e-02,  1.06956057e-01,
        5.98613694e-02,  9.75977182e-02, -3.21767032e-02,  3.55101307e-03,
       -2.18588188e-02, -3.38149257e-02, -1.18252065e-03, -6.49806783e-02,
        1.04250886e-01, -8.27167705e-02, -7.89505467e-02,  6.92818873e-03,
       -3.55526023e-02,  3.17099653e-02, -1.40522674e-01,  1.29687846e-01,
       -7.20400363e-02, -3.75990979e-02, -4.31945585e-02,  8.67470913e-03,
       -1.66965201e-02, -5.95600381e-02, -8.46499577e-02, -2.77765077e-02,
       -2.85331681e-02, -3.59828360e-02,  4.52273116e-02, -2.36150785e-03,
       -4.54839505e-02, -1.84390731e-02, -1.96880996e-02,  3.04260198e-02,
        5.68410717e-02, -1.20003652e-02, -1.64393000e-02,  4.91620228e-03,
        7.45085329e-02, -1.21694077e-02, -1.99243315e-02,  6.59814775e-02,
       -4.13557291e-02,  2.49204803e-02, -1.17288651e-02,  3.34597491e-02,
        3.43753546e-02, -6.98342361e-03,  1.47913839e-03, -2.42696293e-02,
       -1.43720470e-02, -1.74468700e-02,  4.07791398e-02,  3.15824412e-02,
        2.22639591e-02, -1.21490052e-02,  4.43179300e-03,  3.10461912e-02,
       -3.69075537e-02, -5.08116074e-02,  1.17415354e-01, -3.64092812e-02,
        1.85413416e-02, -9.89102423e-02,  4.89672683e-02, -9.68448166e-03,
        1.96690224e-02,  4.71767113e-02, -9.94545445e-02, -6.75309524e-02,
       -4.36580693e-03,  3.97164561e-02,  7.25484118e-02,  4.54341760e-04,
       -3.67116258e-02,  1.86359398e-02,  7.73076117e-02,  9.88827422e-02,
        3.31477597e-02,  8.67311954e-02, -3.02941557e-02, -3.76639552e-02,
        8.27071443e-02, -7.56450072e-02, -2.41178218e-02,  4.66995463e-02,
       -3.68905924e-02,  3.97340842e-02,  5.69537319e-02, -6.86988421e-03,
        3.82982753e-02, -8.97749215e-02, -3.44097577e-02, -6.42272234e-02,
        2.52821706e-02, -4.53554802e-02, -4.21960801e-02, -3.66484113e-02,
       -1.50382370e-02, -2.95945513e-03, -6.37735415e-04, -5.70940636e-02,
       -5.70005849e-02,  2.47773472e-02,  4.54030894e-02, -5.58227971e-02,
       -1.25297522e-02, -6.58111125e-02,  8.56711417e-02, -4.69941050e-02,
        2.02306360e-02,  2.55649653e-03, -1.76524222e-02,  1.48931984e-02,
       -1.41139189e-02, -3.94307002e-02, -4.65882495e-02, -1.01299686e-02,
        4.20647450e-02, -2.35837139e-02, -7.87560493e-02, -1.12320026e-02,
        5.44794649e-02, -3.80145498e-02, -4.74508293e-03, -7.19793290e-02,
       -5.54356836e-02,  2.96915658e-02,  5.18085025e-02,  8.78287628e-02,
        1.76864248e-02,  1.92190129e-02,  3.57445627e-02,  6.47621648e-03,
        2.79603563e-02, -2.16989107e-02, -1.79182030e-02,  1.40695333e-01,
       -1.07239494e-02,  7.65939578e-02, -1.50439062e-03,  2.37921402e-02,
        1.54382298e-02, -4.04764004e-02, -4.01846282e-02,  2.58538127e-02,
       -7.82667100e-03,  7.86434337e-02, -4.15743701e-03, -3.96438263e-04,
       -5.80447577e-02,  1.88093796e-01,  7.73134157e-02,  9.24269259e-02,
       -2.82247923e-02, -6.81674555e-02,  1.04359360e-02,  1.07250646e-01,
        6.41890848e-03,  3.06504779e-02, -4.73784767e-02,  4.60019149e-02,
        3.00909989e-02,  4.80746478e-02, -1.39184352e-02, -1.08398564e-01,
        1.57273598e-02, -8.50313157e-02,  4.29840945e-02, -4.16836403e-02,
       -3.66492495e-02, -9.13757905e-02, -7.68706053e-02, -4.60796580e-02,
        4.32244539e-02,  1.60541255e-02,  1.30462940e-05, -6.56545116e-03],
      dtype=float32), array([[-4.5997430e-02,  3.9724290e-02, -1.3397273e-02, ...,
        -7.5473256e-02,  8.8088233e-03, -9.4537415e-02],
       [ 2.8984664e-02,  8.0262288e-02, -4.0608842e-02, ...,
        -1.0203673e-01,  2.2942042e-02, -2.6878027e-02],
       [ 3.0804440e-02,  1.1548622e-01, -2.5646241e-02, ...,
        -3.8015328e-03,  2.5274275e-02, -6.3170046e-02],
       ...,
       [ 2.7550068e-02,  1.2686612e-01, -1.0378199e-02, ...,
        -8.5032023e-03,  2.4102896e-02, -3.0741006e-02],
       [ 4.5107488e-02,  3.2530397e-02, -4.2936575e-02, ...,
         5.8845215e-02,  1.1548084e-01,  5.3854853e-02],
       [-5.3364815e-31,  5.8101564e-31, -5.6213419e-31, ...,
         5.5438613e-31, -5.7799791e-31,  5.5831303e-31]], dtype=float32), array([ 4.59229499e-02,  1.42772272e-01, -1.72097571e-02,  1.56033024e-01,
        4.56781611e-02,  4.68072705e-02,  1.72208771e-01,  1.50796011e-01,
        1.30147636e-01,  1.88945219e-01,  6.87050298e-02,  5.30313067e-02,
       -3.15672718e-02,  1.25964075e-01,  4.45851423e-02,  1.23975780e-02,
        1.20336473e-01,  2.54543964e-02, -2.47216988e-02, -1.29715316e-02,
       -1.97745916e-02,  6.54436275e-02, -6.87990636e-02,  9.35242549e-02,
       -2.06978451e-02, -4.54364270e-02,  9.12649482e-02,  5.82153015e-02,
        1.30326539e-01,  2.82189921e-02,  1.39028266e-01, -1.97611712e-02,
        3.61321680e-02,  1.81861922e-01, -2.37019379e-02,  5.25296964e-02,
       -4.98479642e-02,  1.27283052e-01, -2.93462109e-02, -2.89733689e-02,
        9.22334567e-02,  1.01390816e-01,  1.02031261e-01,  4.33292612e-02,
        1.12845898e-01, -1.89257134e-02,  4.04454581e-02,  1.05000898e-01,
        1.07168272e-01,  4.29851897e-02, -1.87522881e-02,  7.02546835e-02,
       -1.39709786e-02, -1.99081525e-02,  8.47429559e-02,  2.12942269e-02,
        3.94135434e-03,  7.34297112e-02,  6.41163290e-02,  3.48262675e-02,
        1.07542396e-01,  6.66825473e-02,  6.32665157e-02,  3.00869774e-02,
        4.32115495e-02,  1.60349563e-01, -7.06749111e-02,  3.69371213e-02,
       -6.83237761e-02, -3.63985710e-02,  8.15328117e-03, -5.93466237e-02,
        1.36982918e-01,  1.35196671e-01,  5.95793221e-03,  1.64357647e-01,
       -4.05739844e-02,  2.48681568e-02, -4.74792197e-02, -3.02808397e-02,
       -2.17252839e-02,  4.95546237e-02,  1.00808181e-01, -1.33082978e-02,
        3.71380597e-02, -6.73180521e-02,  3.31788622e-02, -2.10716482e-02,
        2.53368970e-02,  1.10705756e-01,  9.02492478e-02,  1.53050929e-01,
        1.05277948e-01, -7.85541907e-03,  1.66880116e-01,  2.79654339e-02,
        6.93125501e-02,  2.88134650e-03,  7.96954632e-02,  6.40256051e-03,
       -4.97197285e-02, -3.35000455e-02,  3.90239395e-02,  5.57232387e-02,
       -4.40557227e-02,  1.58747748e-01,  1.04127876e-01, -1.56791136e-02,
       -7.22720521e-03,  7.48040155e-02, -2.00373726e-03,  1.32099003e-01,
        9.11661908e-02,  1.71629060e-02,  4.69528325e-02,  7.41026597e-03,
       -2.68851686e-02, -2.73385569e-02,  8.17873329e-03,  2.17585247e-02,
       -6.71064630e-02,  7.51386210e-02, -1.71873402e-02,  1.59057379e-01,
        2.44248956e-02,  1.05590306e-01,  8.24843347e-02, -1.67889725e-02,
       -3.21964659e-02,  1.46952018e-01, -4.20108549e-02,  2.69232858e-02,
        4.56483802e-03, -2.16609426e-02, -3.51020582e-02,  9.60301235e-02,
       -6.69141039e-02,  6.10258020e-02, -1.13274492e-02,  5.53947575e-02,
        9.54231918e-02,  4.76127230e-02,  1.23572797e-01,  7.83822164e-02,
        8.32578391e-02,  2.38968618e-02, -5.58536425e-02,  1.77204292e-02,
        1.38252586e-01,  6.94604442e-02,  7.09299594e-02, -5.20773642e-02,
        1.76198244e-01, -4.92898189e-02, -4.17218693e-02,  1.09242305e-01,
       -6.76132180e-03,  4.28602509e-02,  1.68294594e-01,  1.68386742e-01,
       -5.76385856e-02,  9.84097645e-02,  1.48191974e-01, -2.84406953e-02,
        1.42889440e-01,  1.84281878e-02,  1.93440303e-01,  3.76270078e-02,
        1.67220771e-01,  6.34078011e-02,  8.44985992e-03,  1.40222445e-01,
        6.78402409e-02, -1.44842481e-02,  4.58042733e-02,  3.29661928e-02,
        8.96665305e-02,  1.65626317e-01, -2.77456138e-02,  1.07176133e-01,
        8.78257602e-02, -5.40350098e-03, -8.41083284e-03, -4.08283398e-02,
       -2.99310815e-02,  1.18130043e-01, -1.50466163e-04,  1.67059392e-01,
        1.96807176e-01,  1.47676244e-01, -2.13360190e-02,  1.74955040e-01,
        6.27517924e-02, -1.83805451e-02,  8.38876888e-02, -2.03164108e-02,
        9.73259583e-02,  1.54831246e-01,  8.89534317e-03,  1.52697966e-01,
       -4.68331352e-02, -2.55660061e-02, -3.76809016e-02,  2.99420245e-02,
        1.71439588e-01, -3.43420729e-02,  1.65894732e-01,  1.56399328e-02,
       -2.66216993e-02,  1.54767722e-01,  5.29400632e-02,  8.65736529e-02,
        9.96439382e-02,  4.54599829e-03,  2.00976115e-02,  8.27111378e-02,
        4.71463166e-02,  5.26427031e-02,  8.41828659e-02,  6.93706796e-02,
       -4.50787246e-02,  1.16726995e-01, -4.24910756e-03,  1.14290779e-02,
        6.96549565e-02,  2.13756170e-02,  3.40374783e-02,  9.86892283e-02,
        3.76018360e-02,  8.91576707e-02, -4.86361347e-02,  6.16077743e-02,
        2.16929186e-02,  1.46149129e-01, -3.51966955e-02,  1.37653038e-01,
       -2.16989443e-02,  1.55914709e-01, -1.56704914e-02,  2.06916183e-02,
        1.32328793e-01,  1.13750182e-01,  5.18698692e-02, -3.82212996e-02,
        1.14233382e-01,  3.95671725e-02,  1.22629190e-02,  8.59811008e-02,
       -1.95367951e-02,  1.04966071e-02,  3.77094708e-02, -1.00103940e-03,
        7.25086480e-02,  1.66858256e-01,  2.27597103e-01,  1.47489741e-01],
      dtype=float32), array([[-0.08476736, -0.1764006 , -0.02580684, ...,  0.00646442,
         0.05702282,  0.01345878],
       [-0.152402  , -0.06106262,  0.1726747 , ...,  0.0412994 ,
         0.22838612, -0.4059306 ],
       [ 0.24278152, -0.04385173, -0.16811378, ...,  0.25357112,
        -0.12283809, -0.29232424],
       ...,
       [ 0.11379576,  0.1648541 , -0.05916017, ..., -0.26861203,
         0.23434496,  0.13696764],
       [ 0.1736983 , -0.1937701 ,  0.09263327, ..., -0.22861221,
         0.17688444, -0.27816498],
       [-0.13327701, -0.22805803, -0.05980655, ..., -0.20988573,
         0.19641885,  0.2544963 ]], dtype=float32), array([-0.00973917, -0.07873288, -0.002357  , -0.03964433,  0.02684775,
       -0.0314567 , -0.08538326, -0.07465444,  0.18579467,  0.02639077],
      dtype=float32)]
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `9-model.py`


---
### 10. Save and Load Weights

Write the following functions:<!--plain-NL-->

- `def save_weights(network, filename, save_format='keras'):` saves a model’s weights:


`network` is the model whose weights should be saved
`filename` is the path of the file that the weights should be saved to
`save_format` is the format in which the weights should be saved
Returns: `None`
- `network` is the model whose weights should be saved
- `filename` is the path of the file that the weights should be saved to
- `save_format` is the format in which the weights should be saved
- Returns: `None`
- `def load_weights(network, filename):` loads a model’s weights:


`network` is the model to which the weights should be loaded
`filename` is the path of the file that the weights should be loaded from
Returns: `None`
- `network` is the model to which the weights should be loaded
- `filename` is the path of the file that the weights should be loaded from
- Returns: `None`

- `network` is the model whose weights should be saved
- `filename` is the path of the file that the weights should be saved to
- `save_format` is the format in which the weights should be saved
- Returns: `None`

- `network` is the model to which the weights should be loaded
- `filename` is the path of the file that the weights should be loaded from
- Returns: `None`

```
ubuntu@alexa-ml:~/keras$ cat 10-main.py
#!/usr/bin/env python3
"""
Main file
"""

# Force Seed - fix for Keras
SEED = 8

import os
os.environ['PYTHONHASHSEED'] = str(SEED)
os.environ['TF_ENABLE_ONEDNN_OPTS']= '0'
import random
random.seed(SEED)
import numpy as np
np.random.seed(SEED)
import tensorflow as tf
tf.random.set_seed(SEED)


# Imports
one_hot = __import__('3-one_hot').one_hot
train_model = __import__('8-train').train_model
model = __import__('9-model')
weights = __import__('10-weights')

if __name__ == '__main__':

    network = model.load_model('network2.keras')
    weights.save_weights(network, 'weights2.keras')
    del network

    network2 = model.load_model('network1.keras')
    print(network2.get_weights())
    weights.load_weights(network2, 'weights2.keras')
    print(network2.get_weights())

ubuntu@alexa-ml:~/keras$ ./10-main.py
[array([[ 6.8687044e-32,  9.0365781e-32, -6.9969967e-32, ...,
        -7.5882081e-32,  8.6207582e-33, -1.3832739e-32],
       [ 4.6782477e-32,  6.1503475e-32, -5.7079079e-32, ...,
         6.1566511e-32,  1.2322533e-31, -3.9161465e-32],
       [-2.0177172e-32,  4.2760376e-32,  7.1549836e-33, ...,
         5.3708507e-32, -7.1413539e-32, -7.7795345e-32],
       ...,
       [-1.9896182e-32, -1.0454332e-31, -1.4021029e-32, ...,
         5.2524661e-32, -2.3340851e-33, -2.9050051e-33],
       [ 1.8921073e-32,  4.7803047e-32, -1.1281708e-31, ...,
        -8.3903695e-32, -9.0987453e-32, -4.0252541e-32],
       [ 1.0646973e-31, -8.5559896e-32, -1.7745671e-32, ...,
         9.8652447e-32,  1.2371795e-31, -9.6694014e-32]], dtype=float32), array([ 0.0159985 ,  0.01609657, -0.00391597,  0.0158889 ,  0.03265441,
        0.03733731,  0.03911147, -0.01638691, -0.01726748,  0.03069957,
        0.00188487,  0.04417622,  0.04475984,  0.02236687,  0.0365424 ,
        0.02763822,  0.00730724,  0.00950179,  0.07017363,  0.00118265,
       -0.04993275,  0.00683798,  0.00013741, -0.00990106,  0.06785184,
        0.03535983,  0.07510231, -0.00021168, -0.02512436,  0.04734792,
       -0.00860031,  0.03216172,  0.03087124,  0.01021669,  0.00463291,
        0.07288454, -0.02040217,  0.01277106,  0.00805098,  0.07037719,
        0.04194392,  0.02530297, -0.0131576 ,  0.0155299 ,  0.0119625 ,
        0.02260724,  0.02429646,  0.00193895,  0.02690104,  0.04398982,
        0.05230867,  0.03726577,  0.00011056,  0.06942687,  0.03119843,
        0.04084213, -0.00512498,  0.00700322,  0.02645292,  0.03560783,
        0.06474689, -0.02649247,  0.05919816, -0.00255153,  0.04608544,
        0.01073583, -0.00442728, -0.01458027,  0.00963576,  0.02570731,
       -0.02993961,  0.04849999,  0.04762531,  0.00295237,  0.02905255,
       -0.03856414, -0.00176542,  0.01686547,  0.01427205,  0.05937463,
        0.05129961,  0.05713202, -0.01060039,  0.03183909,  0.021347  ,
        0.00186173,  0.053302  , -0.0206427 ,  0.04249553, -0.0470331 ,
       -0.02142146,  0.00739546,  0.01038704,  0.03651251, -0.04113393,
        0.08019137, -0.02154687, -0.00096575, -0.01082896,  0.01530979,
        0.00796662, -0.01957909, -0.01853861,  0.00066505, -0.02573178,
        0.00406473,  0.03210957,  0.01924897, -0.00089802,  0.00215174,
       -0.0196881 ,  0.012052  ,  0.04675637,  0.02614512,  0.01719036,
        0.02307913,  0.05300315,  0.01406047,  0.01953608,  0.0448747 ,
       -0.00725447,  0.03857031,  0.01188387,  0.02332218,  0.04615263,
       -0.00362715, -0.00390897,  0.01571964, -0.00106687, -0.00039396,
        0.02379779,  0.03522784,  0.02275405,  0.01416512,  0.01459002,
        0.04896466, -0.03290658, -0.04109657,  0.07816873,  0.00260098,
        0.01711044, -0.04589766,  0.05111458,  0.03000178,  0.03368411,
        0.02188729, -0.03221881, -0.04146759,  0.02354525,  0.03433561,
        0.05302689,  0.0151716 , -0.00716805,  0.03536733,  0.02834564,
        0.04757504,  0.03148516,  0.05490476, -0.01306117, -0.01049297,
        0.04986533, -0.02324402,  0.00038705,  0.02436667, -0.00170058,
        0.03431134,  0.0500191 ,  0.00263986,  0.00415503, -0.03692554,
       -0.00618118, -0.01879745,  0.05802204, -0.00814142, -0.0054947 ,
       -0.00902351,  0.00771954,  0.02750819,  0.00426296, -0.00603896,
       -0.04011999, -0.00025819,  0.00180804, -0.00109898, -0.00642176,
       -0.024834  ,  0.04163915, -0.00970772, -0.00307145,  0.00767057,
        0.02982363, -0.00335148, -0.01608791, -0.00141304, -0.00106744,
        0.01304504,  0.0232571 , -0.02358371, -0.03701007, -0.01529578,
        0.05232991, -0.01056104,  0.02083805, -0.00495247, -0.01380538,
        0.01892439,  0.03027001,  0.03789084,  0.01078089,  0.00065609,
        0.02012425,  0.01444606,  0.02587366, -0.02731432, -0.00305503,
        0.07569042,  0.02562355,  0.04627955,  0.00125313,  0.01935815,
        0.00549665,  0.00966644, -0.01979041,  0.02139456,  0.01018829,
        0.05347256,  0.0246698 , -0.00321089, -0.01715113,  0.10867858,
        0.03760035,  0.06826299, -0.023545  , -0.03262253,  0.02011916,
        0.04055405,  0.02386587,  0.01705379, -0.00060789,  0.03251206,
        0.05883861,  0.03153532,  0.00152546, -0.02980431,  0.00470632,
       -0.03765285,  0.00528458, -0.00281341, -0.03664925, -0.04029598,
       -0.00994935, -0.01772901,  0.04451664,  0.01632361,  0.01928386,
        0.04241366], dtype=float32), array([[-0.00740346,  0.01610546, -0.0791522 , ..., -0.06927478,
        -0.05405676, -0.07385128],
       [ 0.00966634,  0.05925936, -0.02512412, ..., -0.04228801,
         0.03285716, -0.06957922],
       [ 0.06055839,  0.07894616, -0.00762011, ..., -0.04066965,
         0.01574101, -0.09476731],
       ...,
       [ 0.04746953,  0.12883297, -0.00186962, ..., -0.05722182,
        -0.01673071, -0.02611563],
       [ 0.03277116,  0.01197327, -0.04927905, ...,  0.07259046,
         0.11797545,  0.07964441],
       [ 0.09562671, -0.0591891 ,  0.05589048, ...,  0.091759  ,
         0.11040771,  0.03373072]], dtype=float32), array([ 0.04983794,  0.05429855,  0.00275323,  0.08333261,  0.02990129,
        0.01394431,  0.08193313,  0.0592178 ,  0.06271514,  0.08470981,
        0.04175733,  0.04022794,  0.00927613,  0.05715157,  0.04401079,
        0.0171712 ,  0.07070772,  0.0127839 , -0.0247217 , -0.0103661 ,
       -0.02709031,  0.0335232 , -0.01586338,  0.04124172,  0.00701242,
       -0.01673202,  0.03051964,  0.0221475 ,  0.03477995,  0.0236982 ,
        0.07579698,  0.00594354,  0.03178247,  0.05830335,  0.025994  ,
        0.00990086, -0.00958981,  0.05885611, -0.00497651, -0.00294633,
        0.06973684,  0.05395087,  0.03732046,  0.02544391,  0.06849102,
       -0.01892571,  0.01086217,  0.04126438,  0.05322574,  0.0379288 ,
       -0.01875229,  0.03880391,  0.00682591,  0.01514171,  0.05050893,
        0.02957509,  0.02167288,  0.04502465,  0.04976227,  0.04339173,
        0.03716925,  0.03963427,  0.02910236,  0.02158571,  0.05127705,
        0.05732799, -0.00931883,  0.03946995, -0.01987154, -0.01495461,
        0.03282965,  0.00086367,  0.05915523,  0.06071794,  0.02997075,
        0.07438988,  0.00605735,  0.01467397,  0.00689062, -0.03028084,
        0.01961253,  0.01908787,  0.06011633, -0.0133083 ,  0.05307035,
       -0.02581513,  0.01901913, -0.0138604 ,  0.02278147,  0.0497014 ,
        0.03696053,  0.06594232,  0.02716302,  0.01284047,  0.05746389,
        0.02399735,  0.04538381, -0.00360895,  0.05284876,  0.02234786,
        0.00147371, -0.00189739,  0.03062023,  0.01851306,  0.01374537,
        0.03887219,  0.04003473,  0.02406961,  0.01952952,  0.04287028,
        0.00989886,  0.05493129,  0.03153781,  0.02674642,  0.04102696,
        0.01034358,  0.01735938,  0.00395719,  0.02525512,  0.02375544,
       -0.02168416,  0.02622127,  0.02957983,  0.06653526,  0.02662926,
        0.05307979,  0.02957094,  0.02190825,  0.00294503,  0.07439245,
       -0.01383213,  0.03542937,  0.01685172,  0.00735377,  0.00312375,
        0.04540668, -0.01843502,  0.04032867,  0.03358072,  0.04615807,
        0.04442742,  0.03177047,  0.04232168,  0.04689997,  0.02063263,
        0.01207836, -0.03515808,  0.02027568,  0.05868972,  0.03319027,
        0.07080349, -0.01151136,  0.07055011, -0.0100769 , -0.00376861,
        0.03749242,  0.00787648, -0.00798151,  0.0434277 ,  0.07697598,
       -0.01540194,  0.04623866,  0.05996273, -0.0284407 ,  0.05800312,
        0.01843232,  0.05775481,  0.02500775,  0.04552989,  0.02080979,
        0.00724255,  0.06077718,  0.04407776, -0.01544976,  0.01063875,
        0.01933946,  0.04942191,  0.07131659, -0.00744803,  0.043902  ,
        0.03054532,  0.02541935, -0.00841083,  0.00571373, -0.00879351,
        0.03848893,  0.01224614,  0.06816484,  0.0775245 ,  0.04700489,
        0.01034331,  0.07671379,  0.04234593,  0.00437359,  0.03378299,
       -0.01783803,  0.03822733,  0.0616619 ,  0.00928902,  0.06082476,
       -0.01658934, -0.02556601, -0.00814961,  0.00926871,  0.06764287,
       -0.0147952 ,  0.07665675,  0.0262103 , -0.00319083,  0.05079631,
        0.04501105,  0.02677827,  0.01067662,  0.0299787 , -0.00132411,
        0.03172626,  0.02886265,  0.01346109,  0.03603879,  0.03539719,
        0.00489198,  0.05692615,  0.00906275,  0.02719059,  0.03469951,
        0.0026572 ,  0.04822573,  0.05481759,  0.03409682,  0.04177761,
       -0.01268073,  0.00454819,  0.01193685,  0.08543165, -0.00886926,
        0.06032844,  0.0184938 ,  0.05496425, -0.01567049,  0.03110963,
        0.06999363,  0.06594428,  0.02077428,  0.02094924,  0.05497451,
        0.04648358,  0.01472044,  0.06464803,  0.00803588, -0.00836375,
        0.01436058,  0.01215286,  0.03192806,  0.05115401,  0.08560728,
        0.05733834], dtype=float32), array([[-0.09454866, -0.25967893, -0.09040809, ...,  0.01416557,
         0.00757021, -0.00511737],
       [-0.09016082, -0.06444883,  0.13812979, ...,  0.04056182,
         0.20885876, -0.34564796],
       [ 0.2263625 ,  0.05947161, -0.12175548, ...,  0.25581512,
        -0.11083326, -0.23549727],
       ...,
       [ 0.08040285,  0.12019178,  0.03804717, ..., -0.2041479 ,
         0.19790643,  0.12031059],
       [ 0.13237333, -0.18444417,  0.0473572 , ..., -0.19954799,
         0.13429458, -0.19718347],
       [-0.09072073, -0.23292018, -0.06994608, ..., -0.12928647,
         0.17068446,  0.195294  ]], dtype=float32), array([-0.00990264, -0.01396461, -0.0016505 , -0.02961294,  0.0278171 ,
        0.00639426, -0.03299631, -0.01989491,  0.03755097,  0.00377197],
      dtype=float32)]
[array([[ 4.9656790e-32,  4.3917174e-32, -4.8977366e-32, ...,
        -4.5926517e-32,  8.6207582e-33, -1.3832739e-32],
       [ 4.6782477e-32,  5.5539886e-32, -5.7079079e-32, ...,
         5.5577202e-32,  1.4002830e-32, -3.9161465e-32],
       [-2.0177172e-32,  4.2760376e-32,  7.1549836e-33, ...,
         5.3708507e-32, -4.6761471e-32, -4.8687718e-32],
       ...,
       [-1.9896182e-32,  5.0971551e-33, -1.4021029e-32, ...,
         5.2524661e-32, -2.3340851e-33, -2.9050051e-33],
       [ 1.8921073e-32,  4.7803047e-32, -8.6395426e-33, ...,
        -5.2557293e-32, -4.4593013e-32, -4.0252541e-32],
       [-5.1641583e-33, -5.3305178e-32, -1.7745671e-32, ...,
        -4.8143899e-33,  1.4154974e-32, -4.2641681e-32]], dtype=float32), array([-1.75625160e-02,  2.38614380e-02, -3.84415276e-02, -1.07868770e-02,
       -2.52650231e-02,  3.68613228e-02,  1.73959732e-02, -1.82547960e-02,
       -2.59543844e-02,  2.32362393e-02, -3.85221317e-02,  2.47119442e-02,
        6.42312169e-02, -2.31926851e-02,  6.15435243e-02,  5.50865792e-02,
       -1.25715164e-02, -4.63420972e-02,  7.89976865e-02,  2.94253393e-03,
       -1.02322079e-01, -1.38261355e-02, -2.68811565e-02, -5.21523729e-02,
        8.07127431e-02,  4.56745587e-02,  1.63595885e-01, -3.63889113e-02,
       -6.77807331e-02,  6.62615569e-03, -1.50769837e-02,  7.68990293e-02,
       -6.26982236e-03, -2.89552901e-02, -2.42170170e-02,  1.04601808e-01,
       -2.80837975e-02, -3.57521027e-02, -1.07769771e-02,  7.09208995e-02,
        7.45427012e-02,  1.82902720e-02, -4.78790738e-02, -3.45297158e-02,
       -7.53630511e-03, -2.55092774e-02,  2.25215089e-02, -2.16000769e-02,
       -3.93025316e-02,  1.77104957e-02,  5.75819798e-02,  2.16920618e-02,
       -1.22017674e-02,  4.11647419e-03,  2.73455400e-02,  6.67569116e-02,
       -1.87870394e-03, -2.81154569e-02,  5.33470213e-02,  8.15945566e-02,
        1.03007048e-01, -7.18834698e-02,  7.43013769e-02, -3.95426713e-02,
       -7.09563028e-03,  2.95166988e-02, -4.18169498e-02, -3.08827106e-02,
       -1.00774597e-02,  1.58848669e-02, -6.19071834e-02,  9.93519207e-04,
        1.29316133e-02, -4.55454719e-04,  4.42109779e-02, -7.97727481e-02,
        1.59326214e-02,  2.01745257e-02,  2.68713459e-02,  1.06956057e-01,
        5.98613694e-02,  9.75977182e-02, -3.21767032e-02,  3.55101307e-03,
       -2.18588188e-02, -3.38149257e-02, -1.18252065e-03, -6.49806783e-02,
        1.04250886e-01, -8.27167705e-02, -7.89505467e-02,  6.92818873e-03,
       -3.55526023e-02,  3.17099653e-02, -1.40522674e-01,  1.29687846e-01,
       -7.20400363e-02, -3.75990979e-02, -4.31945585e-02,  8.67470913e-03,
       -1.66965201e-02, -5.95600381e-02, -8.46499577e-02, -2.77765077e-02,
       -2.85331681e-02, -3.59828360e-02,  4.52273116e-02, -2.36150785e-03,
       -4.54839505e-02, -1.84390731e-02, -1.96880996e-02,  3.04260198e-02,
        5.68410717e-02, -1.20003652e-02, -1.64393000e-02,  4.91620228e-03,
        7.45085329e-02, -1.21694077e-02, -1.99243315e-02,  6.59814775e-02,
       -4.13557291e-02,  2.49204803e-02, -1.17288651e-02,  3.34597491e-02,
        3.43753546e-02, -6.98342361e-03,  1.47913839e-03, -2.42696293e-02,
       -1.43720470e-02, -1.74468700e-02,  4.07791398e-02,  3.15824412e-02,
        2.22639591e-02, -1.21490052e-02,  4.43179300e-03,  3.10461912e-02,
       -3.69075537e-02, -5.08116074e-02,  1.17415354e-01, -3.64092812e-02,
        1.85413416e-02, -9.89102423e-02,  4.89672683e-02, -9.68448166e-03,
        1.96690224e-02,  4.71767113e-02, -9.94545445e-02, -6.75309524e-02,
       -4.36580693e-03,  3.97164561e-02,  7.25484118e-02,  4.54341760e-04,
       -3.67116258e-02,  1.86359398e-02,  7.73076117e-02,  9.88827422e-02,
        3.31477597e-02,  8.67311954e-02, -3.02941557e-02, -3.76639552e-02,
        8.27071443e-02, -7.56450072e-02, -2.41178218e-02,  4.66995463e-02,
       -3.68905924e-02,  3.97340842e-02,  5.69537319e-02, -6.86988421e-03,
        3.82982753e-02, -8.97749215e-02, -3.44097577e-02, -6.42272234e-02,
        2.52821706e-02, -4.53554802e-02, -4.21960801e-02, -3.66484113e-02,
       -1.50382370e-02, -2.95945513e-03, -6.37735415e-04, -5.70940636e-02,
       -5.70005849e-02,  2.47773472e-02,  4.54030894e-02, -5.58227971e-02,
       -1.25297522e-02, -6.58111125e-02,  8.56711417e-02, -4.69941050e-02,
        2.02306360e-02,  2.55649653e-03, -1.76524222e-02,  1.48931984e-02,
       -1.41139189e-02, -3.94307002e-02, -4.65882495e-02, -1.01299686e-02,
        4.20647450e-02, -2.35837139e-02, -7.87560493e-02, -1.12320026e-02,
        5.44794649e-02, -3.80145498e-02, -4.74508293e-03, -7.19793290e-02,
       -5.54356836e-02,  2.96915658e-02,  5.18085025e-02,  8.78287628e-02,
        1.76864248e-02,  1.92190129e-02,  3.57445627e-02,  6.47621648e-03,
        2.79603563e-02, -2.16989107e-02, -1.79182030e-02,  1.40695333e-01,
       -1.07239494e-02,  7.65939578e-02, -1.50439062e-03,  2.37921402e-02,
        1.54382298e-02, -4.04764004e-02, -4.01846282e-02,  2.58538127e-02,
       -7.82667100e-03,  7.86434337e-02, -4.15743701e-03, -3.96438263e-04,
       -5.80447577e-02,  1.88093796e-01,  7.73134157e-02,  9.24269259e-02,
       -2.82247923e-02, -6.81674555e-02,  1.04359360e-02,  1.07250646e-01,
        6.41890848e-03,  3.06504779e-02, -4.73784767e-02,  4.60019149e-02,
        3.00909989e-02,  4.80746478e-02, -1.39184352e-02, -1.08398564e-01,
        1.57273598e-02, -8.50313157e-02,  4.29840945e-02, -4.16836403e-02,
       -3.66492495e-02, -9.13757905e-02, -7.68706053e-02, -4.60796580e-02,
        4.32244539e-02,  1.60541255e-02,  1.30462940e-05, -6.56545116e-03],
      dtype=float32), array([[-4.5997430e-02,  3.9724290e-02, -1.3397273e-02, ...,
        -7.5473256e-02,  8.8088233e-03, -9.4537415e-02],
       [ 2.8984664e-02,  8.0262288e-02, -4.0608842e-02, ...,
        -1.0203673e-01,  2.2942042e-02, -2.6878027e-02],
       [ 3.0804440e-02,  1.1548622e-01, -2.5646241e-02, ...,
        -3.8015328e-03,  2.5274275e-02, -6.3170046e-02],
       ...,
       [ 2.7550068e-02,  1.2686612e-01, -1.0378199e-02, ...,
        -8.5032023e-03,  2.4102896e-02, -3.0741006e-02],
       [ 4.5107488e-02,  3.2530397e-02, -4.2936575e-02, ...,
         5.8845215e-02,  1.1548084e-01,  5.3854853e-02],
       [-5.3364815e-31,  5.8101564e-31, -5.6213419e-31, ...,
         5.5438613e-31, -5.7799791e-31,  5.5831303e-31]], dtype=float32), array([ 4.59229499e-02,  1.42772272e-01, -1.72097571e-02,  1.56033024e-01,
        4.56781611e-02,  4.68072705e-02,  1.72208771e-01,  1.50796011e-01,
        1.30147636e-01,  1.88945219e-01,  6.87050298e-02,  5.30313067e-02,
       -3.15672718e-02,  1.25964075e-01,  4.45851423e-02,  1.23975780e-02,
        1.20336473e-01,  2.54543964e-02, -2.47216988e-02, -1.29715316e-02,
       -1.97745916e-02,  6.54436275e-02, -6.87990636e-02,  9.35242549e-02,
       -2.06978451e-02, -4.54364270e-02,  9.12649482e-02,  5.82153015e-02,
        1.30326539e-01,  2.82189921e-02,  1.39028266e-01, -1.97611712e-02,
        3.61321680e-02,  1.81861922e-01, -2.37019379e-02,  5.25296964e-02,
       -4.98479642e-02,  1.27283052e-01, -2.93462109e-02, -2.89733689e-02,
        9.22334567e-02,  1.01390816e-01,  1.02031261e-01,  4.33292612e-02,
        1.12845898e-01, -1.89257134e-02,  4.04454581e-02,  1.05000898e-01,
        1.07168272e-01,  4.29851897e-02, -1.87522881e-02,  7.02546835e-02,
       -1.39709786e-02, -1.99081525e-02,  8.47429559e-02,  2.12942269e-02,
        3.94135434e-03,  7.34297112e-02,  6.41163290e-02,  3.48262675e-02,
        1.07542396e-01,  6.66825473e-02,  6.32665157e-02,  3.00869774e-02,
        4.32115495e-02,  1.60349563e-01, -7.06749111e-02,  3.69371213e-02,
       -6.83237761e-02, -3.63985710e-02,  8.15328117e-03, -5.93466237e-02,
        1.36982918e-01,  1.35196671e-01,  5.95793221e-03,  1.64357647e-01,
       -4.05739844e-02,  2.48681568e-02, -4.74792197e-02, -3.02808397e-02,
       -2.17252839e-02,  4.95546237e-02,  1.00808181e-01, -1.33082978e-02,
        3.71380597e-02, -6.73180521e-02,  3.31788622e-02, -2.10716482e-02,
        2.53368970e-02,  1.10705756e-01,  9.02492478e-02,  1.53050929e-01,
        1.05277948e-01, -7.85541907e-03,  1.66880116e-01,  2.79654339e-02,
        6.93125501e-02,  2.88134650e-03,  7.96954632e-02,  6.40256051e-03,
       -4.97197285e-02, -3.35000455e-02,  3.90239395e-02,  5.57232387e-02,
       -4.40557227e-02,  1.58747748e-01,  1.04127876e-01, -1.56791136e-02,
       -7.22720521e-03,  7.48040155e-02, -2.00373726e-03,  1.32099003e-01,
        9.11661908e-02,  1.71629060e-02,  4.69528325e-02,  7.41026597e-03,
       -2.68851686e-02, -2.73385569e-02,  8.17873329e-03,  2.17585247e-02,
       -6.71064630e-02,  7.51386210e-02, -1.71873402e-02,  1.59057379e-01,
        2.44248956e-02,  1.05590306e-01,  8.24843347e-02, -1.67889725e-02,
       -3.21964659e-02,  1.46952018e-01, -4.20108549e-02,  2.69232858e-02,
        4.56483802e-03, -2.16609426e-02, -3.51020582e-02,  9.60301235e-02,
       -6.69141039e-02,  6.10258020e-02, -1.13274492e-02,  5.53947575e-02,
        9.54231918e-02,  4.76127230e-02,  1.23572797e-01,  7.83822164e-02,
        8.32578391e-02,  2.38968618e-02, -5.58536425e-02,  1.77204292e-02,
        1.38252586e-01,  6.94604442e-02,  7.09299594e-02, -5.20773642e-02,
        1.76198244e-01, -4.92898189e-02, -4.17218693e-02,  1.09242305e-01,
       -6.76132180e-03,  4.28602509e-02,  1.68294594e-01,  1.68386742e-01,
       -5.76385856e-02,  9.84097645e-02,  1.48191974e-01, -2.84406953e-02,
        1.42889440e-01,  1.84281878e-02,  1.93440303e-01,  3.76270078e-02,
        1.67220771e-01,  6.34078011e-02,  8.44985992e-03,  1.40222445e-01,
        6.78402409e-02, -1.44842481e-02,  4.58042733e-02,  3.29661928e-02,
        8.96665305e-02,  1.65626317e-01, -2.77456138e-02,  1.07176133e-01,
        8.78257602e-02, -5.40350098e-03, -8.41083284e-03, -4.08283398e-02,
       -2.99310815e-02,  1.18130043e-01, -1.50466163e-04,  1.67059392e-01,
        1.96807176e-01,  1.47676244e-01, -2.13360190e-02,  1.74955040e-01,
        6.27517924e-02, -1.83805451e-02,  8.38876888e-02, -2.03164108e-02,
        9.73259583e-02,  1.54831246e-01,  8.89534317e-03,  1.52697966e-01,
       -4.68331352e-02, -2.55660061e-02, -3.76809016e-02,  2.99420245e-02,
        1.71439588e-01, -3.43420729e-02,  1.65894732e-01,  1.56399328e-02,
       -2.66216993e-02,  1.54767722e-01,  5.29400632e-02,  8.65736529e-02,
        9.96439382e-02,  4.54599829e-03,  2.00976115e-02,  8.27111378e-02,
        4.71463166e-02,  5.26427031e-02,  8.41828659e-02,  6.93706796e-02,
       -4.50787246e-02,  1.16726995e-01, -4.24910756e-03,  1.14290779e-02,
        6.96549565e-02,  2.13756170e-02,  3.40374783e-02,  9.86892283e-02,
        3.76018360e-02,  8.91576707e-02, -4.86361347e-02,  6.16077743e-02,
        2.16929186e-02,  1.46149129e-01, -3.51966955e-02,  1.37653038e-01,
       -2.16989443e-02,  1.55914709e-01, -1.56704914e-02,  2.06916183e-02,
        1.32328793e-01,  1.13750182e-01,  5.18698692e-02, -3.82212996e-02,
        1.14233382e-01,  3.95671725e-02,  1.22629190e-02,  8.59811008e-02,
       -1.95367951e-02,  1.04966071e-02,  3.77094708e-02, -1.00103940e-03,
        7.25086480e-02,  1.66858256e-01,  2.27597103e-01,  1.47489741e-01],
      dtype=float32), array([[-0.08476736, -0.1764006 , -0.02580684, ...,  0.00646442,
         0.05702282,  0.01345878],
       [-0.152402  , -0.06106262,  0.1726747 , ...,  0.0412994 ,
         0.22838612, -0.4059306 ],
       [ 0.24278152, -0.04385173, -0.16811378, ...,  0.25357112,
        -0.12283809, -0.29232424],
       ...,
       [ 0.11379576,  0.1648541 , -0.05916017, ..., -0.26861203,
         0.23434496,  0.13696764],
       [ 0.1736983 , -0.1937701 ,  0.09263327, ..., -0.22861221,
         0.17688444, -0.27816498],
       [-0.13327701, -0.22805803, -0.05980655, ..., -0.20988573,
         0.19641885,  0.2544963 ]], dtype=float32), array([-0.00973917, -0.07873288, -0.002357  , -0.03964433,  0.02684775,
       -0.0314567 , -0.08538326, -0.07465444,  0.18579467,  0.02639077],
      dtype=float32)]
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `10-weights.py`


---
### 11. Save and Load Configuration

Write the following functions:<!--plain-NL-->

- `def save_config(network, filename):` saves a model’s configuration in JSON format:


`network` is the model whose configuration should be saved
`filename` is the path of the file that the configuration should be saved to
Returns: `None`
- `network` is the model whose configuration should be saved
- `filename` is the path of the file that the configuration should be saved to
- Returns: `None`
- `def load_config(filename):` loads a model with a specific configuration:


`filename` is the path of the file containing the model’s configuration in JSON format 
Returns: the loaded model
- `filename` is the path of the file containing the model’s configuration in JSON format
- Returns: the loaded model

- `network` is the model whose configuration should be saved
- `filename` is the path of the file that the configuration should be saved to
- Returns: `None`

- `filename` is the path of the file containing the model’s configuration in JSON format
- Returns: the loaded model

```
ubuntu@alexa-ml:~/keras$ cat 11-main.py
#!/usr/bin/env python3
"""
Main file
"""

# Force Seed - fix for Keras
SEED = 8

import os
os.environ['PYTHONHASHSEED'] = str(SEED)
os.environ['TF_ENABLE_ONEDNN_OPTS']= '0'
import random
random.seed(SEED)
import numpy as np
np.random.seed(SEED)
import tensorflow as tf
tf.random.set_seed(SEED)


# Imports
model = __import__('9-model')
config = __import__('11-config')

if __name__ == '__main__':
    network = model.load_model('network1.keras')
    config.save_config(network, 'config1.json')
    del network

    network2 = config.load_config('config1.json')
    network2.summary()
    print(network2.get_weights())

ubuntu@alexa-ml:~/keras$ ./11-main.py
Model: "model"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 input_1 (InputLayer)        [(None, 784)]             0

 dense (Dense)               (None, 256)               200960

 dropout (Dropout)           (None, 256)               0

 dense_1 (Dense)             (None, 256)               65792

 dropout_1 (Dropout)         (None, 256)               0

 dense_2 (Dense)             (None, 10)                2570

=================================================================
Total params: 269322 (1.03 MB)
Trainable params: 269322 (1.03 MB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________
[array([[-0.04818622,  0.00550243,  0.02337964, ...,  0.02026194,
         0.0131394 , -0.07112553],
       [ 0.05287497,  0.06082901,  0.04314509, ...,  0.03088981,
         0.04248595,  0.00075459],
       [ 0.04638709,  0.03635878,  0.05495042, ...,  0.06839117,
        -0.00857798,  0.03085373],
       ...,
       [-0.0613957 , -0.03862576,  0.02686254, ..., -0.04878058,
         0.04068351,  0.04458255],
       [-0.00505619,  0.06761421,  0.05864134, ...,  0.03256558,
         0.01839454, -0.02476381],
       [ 0.0515023 , -0.03591438, -0.04894583, ..., -0.00593287,
        -0.01246206, -0.05569786]], dtype=float32), array([0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0.], dtype=float32), array([[-0.06834389, -0.00614704,  0.05084307, ...,  0.10298666,
        -0.09801269, -0.08086289],
       [-0.03144635, -0.09583601, -0.00154829, ..., -0.10761178,
         0.03725404,  0.02306353],
       [ 0.02972815, -0.05188745, -0.00929771, ...,  0.01023427,
         0.04518052, -0.04252121],
       ...,
       [ 0.03875921,  0.09445202, -0.10698001, ..., -0.0808039 ,
        -0.00411727, -0.0102433 ],
       [ 0.09479322, -0.02422538,  0.05551202, ...,  0.02200616,
         0.09498391, -0.09845343],
       [-0.04811655,  0.09030256, -0.08288536, ..., -0.04274771,
         0.0548188 , -0.02225117]], dtype=float32), array([0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
       0.], dtype=float32), array([[-5.15929461e-02,  1.98602080e-02,  3.24262679e-03, ...,
        -1.26510516e-01,  1.05442345e-01, -3.04353237e-03],
       [-7.30873793e-02, -2.36415863e-02,  6.63369894e-04, ...,
        -1.06679678e-01,  1.95398927e-04, -4.28920984e-03],
       [ 2.93952674e-02, -9.34689045e-02,  4.16807681e-02, ...,
         9.66169238e-02, -7.53199756e-02,  9.76608992e-02],
       ...,
       [-4.70205694e-02,  1.26183033e-04,  1.14953309e-01, ...,
         6.69288635e-02,  5.27009368e-04,  5.63070178e-03],
       [-3.25196981e-03, -4.48374525e-02,  1.08623594e-01, ...,
         1.32407665e-01, -3.46630216e-02, -8.71159956e-02],
       [-1.11422606e-01, -1.39142826e-01,  5.03461063e-03, ...,
         4.33745086e-02, -1.44267350e-01,  1.08879745e-01]], dtype=float32), array([0., 0., 0., 0., 0., 0., 0., 0., 0., 0.], dtype=float32)]
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `11-config.py`


---
### 12. Test

Write a function <!--plain-NL-->`def test_model(network, data, labels, verbose=True):`<!--inline-NL--> that tests a neural network:<!--plain-NL-->

- `network` is the network model to test
- `data` is the input data to test the model with
- `labels` are the correct one-hot labels of `data`
- `verbose` is a boolean that determines if output should be printed during the testing process
- Returns: the loss and accuracy of the model with the testing data, respectively

```
ubuntu@alexa-ml:~/keras$ cat 12-main.py 
#!/usr/bin/env python3

import numpy as np
one_hot = __import__('3-one_hot').one_hot
load_model = __import__('9-model').load_model
test_model = __import__('12-test').test_model

if __name__ == '__main__':
    datasets = np.load('MNIST.npz')
    X_test = datasets['X_test']
    X_test = X_test.reshape(X_test.shape[0], -1)
    Y_test = datasets['Y_test']
    Y_test_oh = one_hot(Y_test)

    network = load_model('network2.keras')
    eval=test_model(network, X_test, Y_test_oh)
    print(eval)
    print("Loss:",np.round(eval[0],3))
    print("Accuracy:",np.round(eval[1],3))

ubuntu@alexa-ml:~/keras$ ./12-main.py 
313/313 [==============================] - 1s 2ms/step - loss: 0.0886 - accuracy: 0.9840
[0.08861645311117172, 0.984000027179718]
Loss: 0.089
Accuracy: 0.984
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `12-test.py`


---
### 13. Predict

Write a function <!--plain-NL-->`def predict(network, data, verbose=False):`<!--inline-NL--> that makes a prediction using a neural network:<!--plain-NL-->

- `network` is the network model to make the prediction with
- `data` is the input data to make the prediction with
- `verbose` is a boolean that determines if output should be printed during the prediction process
- Returns: the prediction for the data

```
ubuntu@alexa-ml:~/keras$ cat 13-main.py
#!/usr/bin/env python3

import numpy as np
one_hot = __import__('3-one_hot').one_hot
load_model = __import__('9-model').load_model
predict = __import__('13-predict').predict


if __name__ == '__main__':
    datasets = np.load('MNIST.npz')
    X_test = datasets['X_test']
    X_test = X_test.reshape(X_test.shape[0], -1)
    Y_test = datasets['Y_test']

    network = load_model('network2.keras')
    Y_pred = predict(network, X_test)
    print(Y_pred)
    print(np.argmax(Y_pred, axis=1))
    print(Y_test)

ubuntu@alexa-ml:~/keras$ ./13-main.py
[[4.14261365e-07 2.77715230e-06 2.46788909e-06 ... 9.99889433e-01
  3.21659058e-07 5.39183820e-05]
 [2.41801303e-07 1.77474394e-05 9.99972165e-01 ... 7.00944511e-08
  3.62985361e-07 3.19262455e-12]
 [6.44652664e-06 9.99481380e-01 8.94945479e-05 ... 1.21436868e-04
  2.33942890e-04 1.72974168e-07]
 ...
 [2.64825349e-11 8.92737884e-09 2.33682041e-12 ... 2.90760624e-07
  4.00840383e-09 1.03349157e-06]
 [4.87686300e-08 6.83480472e-09 2.35899744e-09 ... 1.30440378e-08
  1.10479414e-04 1.15318475e-08]
 [7.30051610e-08 1.11085662e-10 3.21268807e-08 ... 1.50277308e-11
  1.99947636e-09 5.05070430e-11]]
[7 2 1 ... 4 5 6]
[7 2 1 ... 4 5 6]
ubuntu@alexa-ml:~/keras$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/keras`
- File: `13-predict.py`