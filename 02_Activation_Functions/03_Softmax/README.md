### `Softmax` 
* Softmax converts a vector of values to a probability distribution.
* The softmax of each vector x is computed as:
````
 softmax(x) = exp(x) / tf.reduce_sum(exp(x))
````

* The elements of the output vector are in range (0, 1) and sum to 1.

#### Formular

<p align="center">
    <img src="https://github.com/CrispenGari/Keras-API/blob/main/02_Activation_Functions/02_Sigmoid/sigmoid-equation.png"/>
</p>


