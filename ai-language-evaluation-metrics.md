# AI Language Evaluation Metrics

## Definitions

- **False Positive** – The model predicts label **X**, but the actual label is **not X**.  
- **False Negative** – The model **does not** predict label **X**, but the actual label **is X**.  

| Metric   | Formula | Description |
|----------|------------| ----------- |
| **Recall**<br>_Effectiveness in avoiding false negatives. 1.0 → no false negatives (FN = 0)_ → **no misses.** | $$\frac{TP}{TP + FN}$$ | Measures the proportion of actual positive cases that were correctly identified by the model. Indicates how comprehensive the model is at finding all relevant instances. |
| **Precision**<br>_Effectiveness in avoiding false positives. 1.0 → no false positives (FP = 0)_ → **no extras.** | $$\frac{TP}{TP + FP}$$ | Measures the proportion of predicted positive cases that were actually positive. Indicates how accurate the model is when it predicts a positive result. |
| **F1 Score**<br>_Effectiveness in avoiding false negatives and false positives. 1.0 → no false negatives and no false positives (FN = FP = 0)._| $$2 \times \frac{precision \times recall}{precision + recall} = \frac{2TP}{2TP + FP + FN}$$ | The harmonic mean of precision and recall, providing a single balanced metric that gives equal weight to both false positives and false negatives. Particularly useful when the class distribution is imbalanced. |

Where:
- TP = True Positives (correctly predicted positive cases)
- FN = False Negatives (positive cases incorrectly predicted as negative)
- FP = False Positives (negative cases incorrectly predicted as positive)

Intuition:

* A Recall score of 100% means: we didn't miss any positives = no True Positives were _missed_ = no False Negatives.
* A Precision score of 100% means there were no False Positives.

## Example - Email Spam Prediction

Imagine we're building a model to detect spam emails.  We have a test set of 100 emails, and our model makes the following predictions:

|                 | Predicted Spam | Predicted Not Spam |
|-----------------|----------------|--------------------|
| **Actual Spam**  |       40       |         10        |
| **Actual Not Spam**|       5        |         45        |

From this table (called a *confusion matrix*), we can calculate TP, FP, FN, and TN:

* **TP (True Positives):** 40 (Emails correctly predicted as spam)
* **FP (False Positives):** 5 (Emails incorrectly predicted as spam)
* **FN (False Negatives):** 10 (Spam emails incorrectly predicted as not spam)
* **TN (True Negatives):** 45 (Emails correctly predicted as not spam)

Now, let's calculate the metrics:

* **Recall:**  $$\frac{TP}{TP + FN} = \frac{40}{40 + 10} = \frac{40}{50} = 0.8 \text{ or } 80\%$$ &mdash; The model correctly identified 80% of the actual spam emails.

* **Precision:** $$\frac{TP}{TP + FP} = \frac{40}{40 + 5} = \frac{40}{45} \approx 0.89 \text{ or } 89\%$$ &mdash; When the model predicted an email as spam, it was correct about 89% of the time.

* **F1 Score:** $$2 \times \frac{precision \times recall}{precision + recall} = 2 \times \frac{0.89 \times 0.8}{0.89 + 0.8} \approx 0.84$$ &mdash; The F1-score provides a balanced measure, considering both precision and recall.

This example shows how the metrics are calculated and what they tell us about the model's performance.  A high recall means the model is good at finding most of the actual positive cases (spam in this example), while high precision means the model is good at not falsely predicting negative cases as positive (not flagging legitimate emails as spam). The F1-score helps balance these two aspects.

## Further Reading

* Microsoft **Azure AI Language** ⬥ [Evaluation metrics for Custom Text Classification from Microsoft Learn](https://learn.microsoft.com/en-us/azure/ai-services/language-service/custom-text-classification/concepts/evaluation-metrics)
* Microsoft **Azure AI Language** ⬥ [Overview](https://learn.microsoft.com/en-us/azure/ai-services/language-service/)
