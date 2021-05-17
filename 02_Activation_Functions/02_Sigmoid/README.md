### Activation Functions
-In artificial neural networks, the activation function of a node defines the output of that node given an input or set of inputs. A standard integrated circuit can be seen as a digital network of activation functions that can be "ON" or "OFF", depending on input. 

### Classification Problem
A classification problem is a problem where we are trying to predict something's class. There are three types of classifications  which are:

1. **Binary Classification** - In this classification there are only two outcomes weather `0` or `1`, true or false.
2. **Multi-class Classification** - In this classification we will have at least 3 classes or targets we are trying to predict.
3. **Multi-label Classification**  - In this classification problem we are trying to predict two outcomes at the same time, for example whether a ped is a `dog and white in color` or `cat and black in color`.

#### Binary Classification
* **Hidden activation** -> ``ReLU``
* **Output activation** -> ``Sigmoid``
* **Loss Function** -> ``BinaryCrossentropy``
* **Optimizers** -> ``Adam``, `Sigmoid`, **etc**

#### Multi-class Classification
* **Hidden activation** -> ``ReLU``
* **Output activation** -> ``Softmax``
* **Loss Function** -> ``CategoricalCrossentropy`` or `SparseCategoricalCrossentropy`
    * **CategoricalCrossentropy** - requires ``one-hot encoded`` labels
    * **SparseCategoricalCrossentropy** - when the target output label is an ``integer``
    
* **Optimizers** -> ``Adam``, `Sigmoid`, **etc**


