# Deep Neural networks. Assignment 1. 

## Solution
You can find solution to this task in Assignment1.ipynb file.

## Task
There is a dataset called MNIST which has items of handwriting -- the digits 0 through 9.

Write an MNIST classifier that trains to 99% accuracy or above, and does it without a fixed number of epochs -- i.e. you should stop training once you reach that level of accuracy.

Some notes:

1. It should succeed in less than 10 epochs, so it is okay to change epochs to 10, but nothing larger
2. When it reaches 99% or greater it should print out the string "Reached 99% accuracy so cancelling training!"
3. If you add any additional variables, make sure you use the same names as the ones used in the class

I've started the code for you below -- how would you finish it?

**Things to Note:**

When coding the class `myCallback`, Python 3 will run into an error
`TypeError: '>' not supported between instances of 'NoneType' and 'float'`.

When using the code
`if(logs.get('accuracy')>0.99):`
For Python 3, use the following equivalent code line
`if logs.get('accuracy') is not None and logs.get('accuracy') > 0.99:`.

You can run the notebook using TensorFlow 2.5.0

```python
#!pip install tensorflow==2.5.0
```

```python
import tensorflow as tf

print(tf.__version__)
```

```python
# GRADED FUNCTION: train_mnist
def train_mnist():
    # Please write your code only where you are indicated.
    # please do not remove # model fitting inline comments.

    # YOUR CODE SHOULD START HERE
    

    # YOUR CODE SHOULD END HERE

    mnist = tf.keras.datasets.mnist

    (x_train, y_train),(x_test, y_test) = mnist.load_data()
    
    # YOUR CODE SHOULD START HERE
    
    # YOUR CODE SHOULD END HERE
    
    model = tf.keras.models.Sequential([
        # YOUR CODE HERE,
        # YOUR CODE HERE,
        # YOUR CODE HERE
    ])

    model.compile(optimizer='adam',
                  loss='sparse_categorical_crossentropy',
                  metrics=['accuracy'])
    
    # model fitting
    history = model.fit(# YOUR CODE HERE
    )
    # model fitting
    
    return history.epoch, history.history['accuracy'][-1]
```

```python
train_mnist()
```
