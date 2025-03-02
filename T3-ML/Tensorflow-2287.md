# Project 2287: Tensorflow
----


![1](2287_1.jpg)

## Resources

**Read or watch**:

* [Low Level Intro](https://github.com/tensorflow/docs/blob/master/site/en/r1/guide/low_level_intro.md)**(Excluding`Datasets`and`Feature columns`)**
* [Graphs](https://github.com/tensorflow/docs/blob/master/site/en/r1/guide/graphs.md)
* [Tensors](https://github.com/tensorflow/docs/blob/master/site/en/r1/guide/tensors.md)
* [Variables](https://github.com/tensorflow/docs/blob/master/site/en/r1/guide/variables.md)
* [Placeholders](https://www.databricks.com/tensorflow/placeholders)
* [Save and Restore](https://github.com/tensorflow/docs/blob/master/site/en/r1/guide/saved_model.md)**(Up to`Save and restore models`, excluded)**
* [TensorFlow, why there are 3 files after saving the model?](https://stackoverflow.com/questions/41265035/tensorflow-why-there-are-3-files-after-saving-the-model)
* [Exporting and Importing a MetaGraph](https://docs.w3cub.com/tensorflow~python/meta_graph/)
* [TensorFlow - import meta graph and use variables from it](https://stackoverflow.com/questions/42072234/tensorflow-import-meta-graph-and-use-variables-from-it)

**References**:

* [tf.Graph](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/Graph)
* [tf.Session](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/Session)
  * [tf.Session.run](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/Session#run)

* [tf.Tensor](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/Tensor)
* [tf.Variable](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/Variable)
* [tf.constant](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/constant)
* [tf.placeholder](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/placeholder)
* [tf.Operation](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/Operation)
* [tf.keras.layers](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/keras)
  * [tf.keras.layers.Dense](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/keras/layers/Dense)

* [tf.keras.initializers.VarianceScaling](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/keras/initializers/VarianceScaling)
* [tf.nn](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/nn)
  * [tf.nn.relu](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/nn/relu)
  * [tf.nn.sigmoid](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/math/sigmoid)
  * [tf.nn.tanh](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/math/tanh)

* [tf.losses](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/losses)
  * [tf.losses.softmax_cross_entropy](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/losses/softmax_cross_entropy)

* [tf.train](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/train)
  * [tf.train.import_meta_graph](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/train/import_meta_graph)
  * [tf.train.GradientDescentOptimizer](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/train/GradientDescentOptimizer)
    * [tf.train.GradientDescentOptimizer.minimize](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/train/GradientDescentOptimizer#minimize)

  * [tf.train.Saver](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/train/Saver)
    * [tf.train.Saver.save](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/train/Saver#save)
    * [tf.train.Saver.restore](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/train/Saver#restore)

* [tf.add_to_collection](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/add_to_collection)
* [tf.get_collection](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/get_collection)
* [tf.global_variables_initializer](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/global_variables_initializer)
* [tf.argmax](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/argmax)
* [tf.math.equal](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/math/equal)
* [tf.set_random_seed](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/set_random_seed)
* [tf.keras.backend.name_scope](https://www.tensorflow.org/versions/r2.6/api_docs/python/tf/compat/v1/keras/backend/name_scope)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What is tensorflow?
* What is a session? graph?
* What are tensors?
* What are variables? constants? placeholders? How do you use them?
* What are operations? How do you use them?
* What are namespaces? How do you use them?
* How to train a neural network in tensorflow
* What is a checkpoint?
* How to save/load a model with tensorflow
* What is the graph collection?
* How to add and get variables from the collection
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
* Unless otherwise noted, you are not allowed to import any module except`import tensorflow.compat.v1 as tf`
* All your files must be executable
* The length of your files will be tested using`wc`
## More Info

### Installing Tensorflow 2.15

``
```
$ pip install --user tensorflow==2.15
```
### Optimize Tensorflow (Optional)

to make use of your GPU, follow the steps in the[tensorflow official website](https://www.tensorflow.org/install/pip).
This will make training MUCH faster!### Note

During this project, your main task is to delve into Tensorflow v1. Be sure to anticipate the upcoming project on**Tensorflow 2 & Keras**, which will enhance your understanding of Tensorflow v2.

After completing this project, you can further explore the differences betwen**Tensorflow v1**and**Tensorflow v2**by consulting the following resources:

* [TensorFlow 1.x vs TensorFlow 2 - Behaviors and APIs](https://www.tensorflow.org/guide/migrate/tf1_vs_tf2)
* [Tensorflow 1.xvs. Tensorflow 2.x: What’s the Difference?](https://www.geeksforgeeks.org/tensorflow-1-xvs-tensorflow-2-x-whats-the-difference/)

----
## Tasks
---
### 0. Placeholders

Write the function <!--plain-NL-->`def create_placeholders(nx, classes):`<!--inline-NL--> that returns two placeholders, <!--plain-NL-->`x`<!--inline-NL--> and <!--plain-NL-->`y`<!--inline-NL-->, for the neural network:<!--plain-NL-->

- `nx`: the number of feature columns in our data
- `classes`: the number of classes in our classifier
- Returns: placeholders named `x` and `y`, respectively


`x` is the placeholder for the input data to the neural network
`y` is the placeholder for the one-hot labels for the input data
- `x` is the placeholder for the input data to the neural network
- `y` is the placeholder for the one-hot labels for the input data

- `x` is the placeholder for the input data to the neural network
- `y` is the placeholder for the one-hot labels for the input data

```
ubuntu@alexa-ml:~/tensorflow$ cat 0-main.py 
#!/usr/bin/env python3

import tensorflow.compat.v1 as tf
tf.disable_eager_execution()

create_placeholders = __import__('0-create_placeholders').create_placeholders

x, y = create_placeholders(784, 10)
print(x)
print(y)
ubuntu@alexa-ml:~/tensorflow$ ./0-main.py 
Tensor("x:0", shape=(?, 784), dtype=float32)
Tensor("y:0", shape=(?, 10), dtype=float32)
ubuntu@alexa-ml:~/0x02-tensorflow$ 

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/tensorflow`
- File: `0-create_placeholders.py`


---
### 1. Layers

Write the function <!--plain-NL-->`def create_layer(prev, n, activation):`<!--inline-NL-->

- `prev` is the tensor output of the previous layer
- `n` is the number of nodes in the layer to create
- `activation` is the activation function that the layer should use
- use `tf.keras.initializers.VarianceScaling(mode='fan_avg')` to implement`He et. al` initialization for the layer weights
- each layer should be given the name `layer`
- Returns: the tensor output of the layer

```
ubuntu@alexa-ml:~/tensorflow$ cat 1-main.py 
#!/usr/bin/env python3

import tensorflow.compat.v1 as tf
tf.disable_eager_execution()

create_placeholders = __import__('0-create_placeholders').create_placeholders
create_layer = __import__('1-create_layer').create_layer

x, y = create_placeholders(784, 10)
l = create_layer(x, 256, tf.nn.tanh)
print(l)
ubuntu@alexa-ml:~/tensorflow$ ./1-main.py 
Tensor("layer/Tanh:0", shape=(?, 256), dtype=float32)
ubuntu@alexa-ml:~/tensorflow$ 

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/tensorflow`
- File: `1-create_layer.py`


---
### 2. Forward Propagation

Write the function <!--plain-NL-->`def forward_prop(x, layer_sizes=[], activations=[]):`<!--inline-NL--> that creates the forward propagation graph for the neural network:<!--plain-NL-->

- `x` is the placeholder for the input data
- `layer_sizes` is a list containing the number of nodes in each layer of the network
- `activations` is a list containing the activation functions for each layer of the network
- Returns: the prediction of the network in tensor form
- For this function, you should import your `create_layer` function with `create_layer = __import__('1-create_layer').create_layer`

```
ubuntu@alexa-ml:~/tensorflow$ cat 2-main.py 
#!/usr/bin/env python3

import tensorflow.compat.v1 as tf
tf.disable_eager_execution()

create_placeholders = __import__('0-create_placeholders').create_placeholders
forward_prop = __import__('2-forward_prop').forward_prop

x, y = create_placeholders(784, 10)
y_pred = forward_prop(x, [256, 256, 10], [tf.nn.tanh, tf.nn.tanh, None])
print(y_pred)
ubuntu@alexa-ml:~/tensorflow$ ./2-main.py 
Tensor("layer_2/BiasAdd:0", shape=(?, 10), dtype=float32)
ubuntu@alexa-ml:~/tensorflow$ 

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/tensorflow`
- File: `2-forward_prop.py`


---
### 3. Accuracy

Write the function <!--plain-NL-->`def calculate_accuracy(y, y_pred):`<!--inline-NL--> that calculates the accuracy of a prediction:<!--plain-NL-->

- `y` is a placeholder for the labels of the input data
- `y_pred` is a tensor containing the network’s predictions
- Returns: a tensor containing the decimal accuracy of the prediction 
*hint*:  accuracy = correct_predictions / all_predictions

```
ubuntu@alexa-ml:~/tensorflow$ cat 3-main.py 
#!/usr/bin/env python3

import tensorflow.compat.v1 as tf
tf.disable_eager_execution()

create_placeholders = __import__('0-create_placeholders').create_placeholders
forward_prop = __import__('2-forward_prop').forward_prop
calculate_accuracy = __import__('3-calculate_accuracy').calculate_accuracy

x, y = create_placeholders(784, 10)
y_pred = forward_prop(x, [256, 256, 10], [tf.nn.tanh, tf.nn.tanh, None])
accuracy = calculate_accuracy(y, y_pred)
print(accuracy)
ubuntu@alexa-ml:~/tensorflow$ ./3-main.py 
Tensor("Mean:0", shape=(), dtype=float32)
ubuntu@alexa-ml:~/tensorflow$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/tensorflow`
- File: `3-calculate_accuracy.py`


---
### 4. Loss

Write the function <!--plain-NL-->`def calculate_loss(y, y_pred):`<!--inline-NL--> that calculates the softmax cross-entropy loss of a prediction:<!--plain-NL-->

- `y` is a placeholder for the labels of the input data
- `y_pred` is a tensor containing the network’s predictions
- Returns: a tensor containing the loss of the prediction

```
ubuntu@alexa-ml:~/tensorflow$ cat 4-main.py 
#!/usr/bin/env python3

import tensorflow.compat.v1 as tf
tf.disable_eager_execution()

create_placeholders = __import__('0-create_placeholders').create_placeholders
forward_prop = __import__('2-forward_prop').forward_prop
calculate_loss = __import__('4-calculate_loss').calculate_loss

x, y = create_placeholders(784, 10)
y_pred = forward_prop(x, [256, 256, 10], [tf.nn.tanh, tf.nn.tanh, None])
loss = calculate_loss(y, y_pred)
print(loss)
ubuntu@alexa-ml:~/tensorflow$ ./4-main.py 
Tensor("softmax_cross_entropy_loss/value:0", shape=(), dtype=float32)
ubuntu@alexa-ml:~/tensorflow$ 

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/tensorflow`
- File: `4-calculate_loss.py`


---
### 5. Train_Op

Write the function <!--plain-NL-->`def create_train_op(loss, alpha):`<!--inline-NL--> that creates the training operation for the network:<!--plain-NL-->

- `loss` is the loss of the network’s prediction
- `alpha` is the learning rate
- Returns: an operation that trains the network using gradient descent

```
ubuntu@alexa-ml:~/tensorflow$ cat 5-main.py 
#!/usr/bin/env python3

import tensorflow.compat.v1 as tf
tf.disable_eager_execution()

create_placeholders = __import__('0-create_placeholders').create_placeholders
forward_prop = __import__('2-forward_prop').forward_prop
calculate_loss = __import__('4-calculate_loss').calculate_loss
create_train_op = __import__('5-create_train_op').create_train_op


x, y = create_placeholders(784, 10)
y_pred = forward_prop(x, [256, 256, 10], [tf.nn.tanh, tf.nn.tanh, None])
loss = calculate_loss(y, y_pred)
train_op = create_train_op(loss, 0.01)
print(train_op)
ubuntu@alexa-ml:~/tensorflow$ ./5-main.py 
name: "GradientDescent"
op: "NoOp"
input: "^GradientDescent/update_layer/kernel/ResourceApplyGradientDescent"
input: "^GradientDescent/update_layer/bias/ResourceApplyGradientDescent"
input: "^GradientDescent/update_layer_1/kernel/ResourceApplyGradientDescent"
input: "^GradientDescent/update_layer_1/bias/ResourceApplyGradientDescent"
input: "^GradientDescent/update_layer_2/kernel/ResourceApplyGradientDescent"
input: "^GradientDescent/update_layer_2/bias/ResourceApplyGradientDescent"

ubuntu@alexa-ml:~/tensorflow$ 

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/tensorflow`
- File: `5-create_train_op.py`


---
### 6. Train

Write the function <!--plain-NL-->`def train(X_train, Y_train, X_valid, Y_valid, layer_sizes, activations, alpha, iterations, save_path="/tmp/model.ckpt"):`<!--inline-NL--> that builds, trains, and saves a neural network classifier:<!--plain-NL-->

- `X_train` is a `numpy.ndarray` containing the training input data
- `Y_train` is a `numpy.ndarray` containing the training labels
- `X_valid` is a `numpy.ndarray` containing the validation input data
- `Y_valid` is a `numpy.ndarray` containing the validation labels
- `layer_sizes` is a list containing the number of nodes in each layer of the network
- `activations` is a list containing the activation functions for each layer of the network
- `alpha` is the learning rate
- `iterations` is the number of iterations to train over
- `save_path` designates where to save the model
- Add the following to the graph’s collection


placeholders `x` and `y`
tensors `y_pred`, `loss`, and `accuracy`
operation `train_op`
- placeholders `x` and `y`
- tensors `y_pred`, `loss`, and `accuracy`
- operation `train_op`
- After every 100 iterations, the 0th iteration, and `iterations` iterations, print the following:


`After {i} iterations:` where i is the iteration
`\tTraining Cost: {cost}` where `{cost}` is the training cost
`\tTraining Accuracy: {accuracy}` where `{accuracy}` is the training accuracy
`\tValidation Cost: {cost}` where `{cost}` is the validation cost
`\tValidation Accuracy: {accuracy}` where `{accuracy}` is the validation accuracy
- `After {i} iterations:` where i is the iteration
- `\tTraining Cost: {cost}` where `{cost}` is the training cost
- `\tTraining Accuracy: {accuracy}` where `{accuracy}` is the training accuracy
- `\tValidation Cost: {cost}` where `{cost}` is the validation cost
- `\tValidation Accuracy: {accuracy}` where `{accuracy}` is the validation accuracy
- *Reminder: the 0th iteration represents the model before any training has occurred*
- After training has completed, save the model to `save_path`
- You may use the following imports:


`calculate_accuracy = __import__('3-calculate_accuracy').calculate_accuracy`
`calculate_loss = __import__('4-calculate_loss').calculate_loss`
`create_placeholders = __import__('0-create_placeholders').create_placeholders`
`create_train_op = __import__('5-create_train_op').create_train_op`
`forward_prop = __import__('2-forward_prop').forward_prop`
- `calculate_accuracy = __import__('3-calculate_accuracy').calculate_accuracy`
- `calculate_loss = __import__('4-calculate_loss').calculate_loss`
- `create_placeholders = __import__('0-create_placeholders').create_placeholders`
- `create_train_op = __import__('5-create_train_op').create_train_op`
- `forward_prop = __import__('2-forward_prop').forward_prop`
- You are not allowed to use `tf.saved_model`
- Returns: the path where the model was saved

- placeholders `x` and `y`
- tensors `y_pred`, `loss`, and `accuracy`
- operation `train_op`

- `After {i} iterations:` where i is the iteration
- `\tTraining Cost: {cost}` where `{cost}` is the training cost
- `\tTraining Accuracy: {accuracy}` where `{accuracy}` is the training accuracy
- `\tValidation Cost: {cost}` where `{cost}` is the validation cost
- `\tValidation Accuracy: {accuracy}` where `{accuracy}` is the validation accuracy

- `calculate_accuracy = __import__('3-calculate_accuracy').calculate_accuracy`
- `calculate_loss = __import__('4-calculate_loss').calculate_loss`
- `create_placeholders = __import__('0-create_placeholders').create_placeholders`
- `create_train_op = __import__('5-create_train_op').create_train_op`
- `forward_prop = __import__('2-forward_prop').forward_prop`

```
ubuntu@alexa-ml:~/tensorflow$ cat 6-main.py 
#!/usr/bin/env python3

import numpy as np
import tensorflow.compat.v1 as tf
tf.disable_eager_execution()
train = __import__('6-train').train

def one_hot(Y, classes):
    """convert an array to a one-hot matrix"""
    one_hot = np.zeros((Y.shape[0], classes))
    one_hot[np.arange(Y.shape[0]), Y] = 1
    return one_hot

if __name__ == '__main__':
    lib= np.load('../data/MNIST.npz')
    X_train_3D = lib['X_train']
    Y_train = lib['Y_train']
    X_train = X_train_3D.reshape((X_train_3D.shape[0], -1))
    Y_train_oh = one_hot(Y_train, 10)
    X_valid_3D = lib['X_valid']
    Y_valid = lib['Y_valid']
    X_valid = X_valid_3D.reshape((X_valid_3D.shape[0], -1))
    Y_valid_oh = one_hot(Y_valid, 10)

    layer_sizes = [256, 256, 10]
    activations = [tf.nn.tanh, tf.nn.tanh, None]
    alpha = 0.01
    iterations = 1000

    tf.set_random_seed(0)
    save_path = train(X_train, Y_train_oh, X_valid, Y_valid_oh, layer_sizes,
                      activations, alpha, iterations, save_path="./model.ckpt")
    print("Model saved in path: {}".format(save_path))
ubuntu@alexa-ml:~/tensorflow$ ./6-main.py 
After 0 iterations:
        Training Cost: 2.3389201164245605
        Training Accuracy: 0.1281999945640564
        Validation Cost: 2.3470873832702637
        Validation Accuracy: 0.11900000274181366
After 100 iterations:
        Training Cost: 1.1307156085968018
        Training Accuracy: 0.7742599844932556
        Validation Cost: 1.0977574586868286
        Validation Accuracy: 0.796999990940094
After 200 iterations:
        Training Cost: 0.7912304401397705
        Training Accuracy: 0.8301600217819214
        Validation Cost: 0.7469470500946045
        Validation Accuracy: 0.8515999913215637

...

After 1000 iterations:
        Training Cost: 0.4033987820148468
        Training Accuracy: 0.8895599842071533
        Validation Cost: 0.3675466477870941
        Validation Accuracy: 0.9021000266075134
Model saved in path: ./model.ckpt
ubuntu@alexa-ml:~/tensorflow$ ls model.ckpt*
model.ckpt.data-00000-of-00001  model.ckpt.index  model.ckpt.meta
ubuntu@alexa-ml:~/tensorflow$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/tensorflow`
- File: `6-train.py`


---
### 7. Evaluate

Write the function <!--plain-NL-->`def evaluate(X, Y, save_path):`<!--inline-NL--> that evaluates the output of a neural network:<!--plain-NL-->

- `X` is a `numpy.ndarray` containing the input data to evaluate
- `Y` is a `numpy.ndarray` containing the one-hot labels for `X`
- `save_path` is the location to load the model from
- You are not allowed to use `tf.saved_model`
- Returns: the network’s prediction, accuracy, and loss, respectively

```
ubuntu@alexa-ml:~/tensorflow$ cat 7-main.py 
#!/usr/bin/env python3

import matplotlib.pyplot as plt
import numpy as np
import tensorflow.compat.v1 as tf
tf.disable_eager_execution()
evaluate = __import__('7-evaluate').evaluate

def one_hot(Y, classes):
    """convert an array to a one-hot matrix"""
    one_hot = np.zeros((Y.shape[0], classes))
    one_hot[np.arange(Y.shape[0]), Y] = 1
    return one_hot

if __name__ == '__main__':
    lib= np.load('../data/MNIST.npz')
    X_test_3D = lib['X_test']
    Y_test = lib['Y_test']
    X_test = X_test_3D.reshape((X_test_3D.shape[0], -1))
    Y_test_oh = one_hot(Y_test, 10)

    Y_pred_oh, accuracy, cost = evaluate(X_test, Y_test_oh, './model.ckpt')
    print("Test Accuracy:", accuracy)
    print("Test Cost:", cost)

    Y_pred = np.argmax(Y_pred_oh, axis=1)

    fig = plt.figure(figsize=(10, 10))
    for i in range(100):
        fig.add_subplot(10, 10, i + 1)
        plt.imshow(X_test_3D[i])
        plt.title(str(Y_test[i]) + ' : ' + str(Y_pred[i]))
        plt.axis('off')
    plt.tight_layout()
    plt.show()
ubuntu@alexa-ml:~/tensorflow$ ./7-main.py
Test Accuracy: 0.8997
Test Cost: 0.3778775

```



![1](2287_1.png)

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `supervised_learning/tensorflow`
- File: `7-evaluate.py`