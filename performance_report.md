## 📊 Conclusion

Model 6 achieves an overall accuracy of **90%**, slightly lower than Models 4 and 5 (both around **91%**). However, a deeper look at the **class-wise precision, recall, and F1-scores** reveals important distinctions in how the models handle different types of clothing in the Fashion-MNIST dataset.

---

### ✅ Strong Classes Across All Models

Classes like **1 (Trouser)**, **5 (Sandal)**, **7 (Sneaker)**, **8 (Bag)**, and **9 (Ankle Boot)** consistently achieve very high precision and recall (typically **0.95–1.00**), showing that these categories are easily separable across all models.

---

### 🟡 Moderate Performance Classes

Classes such as:

- **0 (T-shirt/top)**
- **2 (Pullover)**
- **3 (Dress)**
- **4 (Coat)**

perform well overall. Notably, Model 6 improves slightly in **recall for class 0 (0.89)** and **class 3 (0.89)** compared to other models, suggesting it sometimes captures high-level features more robustly.

---

### ❌ Challenging Class: 6 (Shirt)

All models struggle with **class 6 (Shirt)**:

- Precision ranges: **0.66–0.79**
- Recall ranges: **0.67–0.76**

Model 6 has a **precision of 0.75** and **recall of 0.71**, comparable to Model 4 but slightly under Model 5's stronger handling (**precision 0.74**, **recall 0.76**). This confirms that this class has overlapping features with others and is inherently more difficult to distinguish.

---

### 🔄 Tradeoffs in Model 6 Design

Model 6 uses **stride=2** in its convolutional layers and frequent pooling, aggressively reducing spatial dimensions. While this allows faster computation and better extraction of high-level features, it may lead to a loss in **fine-grained texture details**, slightly impacting performance on more nuanced classes like **Pullover** and **Shirt**.

However, the increase in channel depth (32 → 64 → 128) helps Model 6 maintain competitive performance and even outperform in some areas (e.g., recall for T-shirts and Dresses).

---

### 📋 Model Comparison Summary

| Model     | Accuracy | Precision (Macro Avg) | Recall (Macro Avg) | F1-Score (Macro Avg) | Notes                                     |
|-----------|----------|------------------------|---------------------|-----------------------|-------------------------------------------|
| **Model 4** | 0.91     | 0.91                   | 0.91                | 0.91                  | 3 Conv layers, standard strides           |
| **Model 5** | 0.91     | 0.92                   | 0.91                | 0.92                  | 3 Conv layers, all `padding='same'`       |
| **Model 6** | 0.90     | 0.90                   | 0.90                | 0.90                  | Uses strides and pooling, deeper channels |

---


---

