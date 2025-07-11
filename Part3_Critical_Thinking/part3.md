# Part 3: Critical Thinking

---

## 1. Ethics & Bias (10 points)

**How might biased training data affect patient outcomes in the case study?**

Biased training data can lead to unfair treatment recommendations:
- **Underrepresented groups** (e.g., minorities, low-income patients) may receive inaccurate risk predictions.
- This could result in **missed interventions** for high-risk patients or **unnecessary monitoring** for low-risk patients.
- It may **widen healthcare disparities** rather than reduce them.

---

**Strategy to mitigate this bias:**

- **Bias Auditing:** Regularly assess the model’s predictions across different demographic groups to detect disparities.
- **Data Augmentation:** Include representative data from underrepresented populations.
- **Fairness Constraints:** Apply algorithms (e.g., reweighing or adversarial debiasing) to reduce bias during training.

---

## 2. Trade-offs (10 points)

**Discuss the trade-off between model interpretability and accuracy in healthcare:**

- **Interpretability:**
  - Essential for clinician trust, regulatory compliance, and understanding predictions.
  - Easier with models like decision trees and logistic regression.
- **Accuracy:**
  - More complex models (e.g., deep learning, ensemble methods) often offer higher predictive accuracy but are less interpretable.

**In healthcare:**
- **Balance is crucial:** A slightly less accurate but interpretable model may be preferable for critical clinical decisions.

---

**Impact of limited computational resources on model choice:**

- Hospitals with limited compute resources may struggle to deploy **resource-heavy models** (e.g., deep learning).
- **Lightweight models** (e.g., logistic regression, pruned decision trees) are preferable in such contexts, offering faster inference and lower hardware costs.
- If using heavier models, consider:
  - **Model quantization** to reduce size.
  - **Edge-cloud hybrid deployment** to offload heavy computation while maintaining low latency.

---



