### Confusion Matrix
* Compares the predicted values with the true values in a tabular way, if 100% correct, all values in the matrix will be top left to bottom right (diagnol line).
> Compute confusion matrix to evaluate the accuracy of a classification.

```
sklearn.metrics.confusion_matrix()
```

#### Plotting the `confusion_matrix` function:

```python
import itertools
from sklearn.metrics import confusion_matrix
def plot_confusion_matrix(y_true, y_pred, classes=None, figsize=(5, 5), text_size=16): 
      # Create the confustion matrix
      cm = confusion_matrix(y_true, y_pred)
      cm_norm = cm.astype("float") / cm.sum(axis=1)[:, np.newaxis] 
      n_classes = cm.shape[0]
      # Plot the figure and make it pretty
      fig, ax = plt.subplots(figsize=figsize)
      cax = ax.matshow(cm, cmap=plt.cm.Blues) 
      fig.colorbar(cax)
    
      if classes:
        labels = classes
      else:
        labels = np.arange(cm.shape[0])
        
      ax.set(title="Confusion Matrix",
             xlabel="Predicted label",
             ylabel="True label",
             xticks=np.arange(n_classes),
             yticks=np.arange(n_classes), 
             xticklabels=labels,
             yticklabels=labels)

      ax.xaxis.set_label_position("bottom")
      ax.xaxis.tick_bottom()

      threshold = (cm.max() + cm.min()) / 2.
      # Plot the text on each cell
      for i, j in itertools.product(range(cm.shape[0]), range(cm.shape[1])):
        plt.text(j, i, f"{cm[i, j]} ({cm_norm[i, j]*100:.1f}%)",
                 horizontalalignment="center",
                 color="white" if cm[i, j] > threshold else "black",
                 size=text_size)
```