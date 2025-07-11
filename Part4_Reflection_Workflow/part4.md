# Part 4: Reflection & Workflow Diagram (10 points)

---

## 1. Reflection (5 points)

### What was the most challenging part of the workflow? Why?

The **most challenging part** was designing an appropriate **preprocessing pipeline and model selection**:
- Ensuring data cleaning, handling missing values, and feature engineering were aligned with the prediction task.
- Choosing a model that balances **accuracy with interpretability**, especially in healthcare where explainability is crucial.

### How would you improve your approach with more time/resources?

- **Engage with domain experts** to refine the features that best indicate readmission risk.
- Collect a **larger, more representative dataset** to improve generalizability.
- Experiment with **automated hyperparameter tuning** using Optuna or Grid Search to optimize model performance systematically.

---

## 2. Diagram (5 points)

### AI Development Workflow Diagram

Below is a **sketched workflow diagram** representing the AI workflow used in this project:

```plaintext
+--------------------+
| 1. Problem Definition |
+--------------------+
          |
          v
+-----------------------------+
| 2. Data Collection & Preprocessing |
+-----------------------------+
          |
          v
+-----------------+
| 3. Model Development |
+-----------------+
          |
          v
+-------------------+
| 4. Evaluation & Deployment |
+-------------------+
          |
          v
+------------+
| 5. Monitoring |
+------------+

