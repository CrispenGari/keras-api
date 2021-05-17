### Classfication report
* A Classification report is used to measure the quality of predictions from a classification algorithm. ... The report shows the main classification metrics precision, recall and f1-score on a per-class basis. The metrics are calculated by using true and false positives, true and false negatives.

```
sklearn.metrics.classification_report()
```

#### Plotting the `classification_report`:

```python
import numpy as np
import seaborn as sns
from sklearn.metrics import classification_report
import pandas as pd
report = classification_report(y_true, y_pred, labels=labels, output_dict=True)
sns.heatmap(pd.DataFrame(report).iloc[:-1, :].T, annot=True)
plt.title("Classification Report")
plt.show()
```