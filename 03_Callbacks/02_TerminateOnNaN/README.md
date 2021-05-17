### TerminateOnNaN
Callback that terminates training when a NaN loss is encountered.


````
tf.keras.callbacks.TerminateOnNaN()
````

#### Usage

```python
model = keras.Sequential([
    keras.layers.Dense(64, activation='relu'),
    keras.layers.Dense(32, activation='relu'),
    keras.layers.Dense(16, activation='relu'),
    keras.layers.Dense(1, activation=keras.activations.sigmoid),
])
model.compile(
    loss = keras.losses.BinaryCrossentropy(),
    metrics = ['acc'],
    optimizer = keras.optimizers.Adam(lr=1e-3)
)

"""
"""
NA_CALLBACK = keras.callbacks.TerminateOnNaN()

EPOCHS = 100
VAL_SPLIT = .2
BATCH_SIZE = 32
VERBOSE = 1

history = model.fit(X_train, y_train, epochs=EPOCHS, 
                    validation_split = VAL_SPLIT, batch_size= BATCH_SIZE,
                    verbose = VERBOSE, callbacks = [NA_CALLBACK]
                   )
```

[Docs](https://keras.io/api/callbacks/terminate_on_nan/)