# AI Language Evaluation Metrics

- **False Positive** – The model predicts label **X**, but the actual label is **not X**.  
- **False Negative** – The model **does not** predict label **X**, but the actual label **is X**.  

| Metric   | Formula | Description |
|----------|------------| ----------- |
| **Recall** | $$\frac{TP}{TP + FN}$$ | Measures the proportion of actual positive cases that were correctly identified by the model. Indicates how comprehensive the model is at finding all relevant instances. |
| **Precision** | $$\frac{TP}{TP + FP}$$ | Measures the proportion of predicted positive cases that were actually positive. Indicates how accurate the model is when it predicts a positive result. |
| **F1 Score** | $$2 \times \frac{precision \times recall}{precision + recall} = \frac{2TP}{2TP + FP + FN}$$ | The harmonic mean of precision and recall, providing a single balanced metric that gives equal weight to both false positives and false negatives. Particularly useful when the class distribution is imbalanced. |

Where:
- TP = True Positives (correctly predicted positive cases)
- FN = False Negatives (positive cases incorrectly predicted as negative)
- FP = False Positives (negative cases incorrectly predicted as positive)
