# Deep-Learning
| Problem type | Last-layer activation | Loss function |
| --- | :---: | --- |
| Binary classification | sigmoid | binary_crossentropy |
| Multiclass, single-label classification | softmax | categorical_crossentropy |
| Multiclass, multilabel classification | sigmoid | binary_crossentropy |
| Regression to arbitrary values | None | mse |
| Regression to values between 0 and 1 | sigmoid | mse or binary_crossentropy |

# Different result using deep learning in Keras
If you want to get each time the same result you need to add a random seed. See also [https://machinelearningmastery.com/reproducible-results-neural-networks-keras/](https://machinelearningmastery.com/reproducible-results-neural-networks-keras/).

This can be done by just adding:
```python
from numpy.random import seed
seed(42)
```
And in case you are using Tensorflow backend you also need to add:
```python
from tensorflow import set_random_seed
set_random_seed(42)
```
The 42 is just an arbitrary number you can choose at your will. This is just a constant for the random seed so that you will always get the same random initialisations for your weights. This will then cause to give you the same results.
