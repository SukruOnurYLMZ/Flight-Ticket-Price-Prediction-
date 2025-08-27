# Flight-Ticket-Price-Prediction-
Flight Ticket Price Prediction Using Deep Learning Techniques

## 🧠 Interpretation

### 🚀 Best Performing Technique
The **Base Model** achieved the highest performance with the **lowest validation loss (5521)** and the **highest R² score (0.9992)**. This indicates that a simpler architecture without any additional regularization or normalization was able to generalize very well on the given dataset.

### ✅ Techniques That Improved Performance
- The **Batch Normalization + Dropout** model also performed strongly, with a high R² score (0.9864) and relatively low validation loss (97,463).
    - Batch Normalization helped stabilize the training process.
    - Dropout reduced overfitting by randomly deactivating neurons during training.
- This combination clearly outperformed the model using only Dropout, suggesting that regularization is more effective when combined with normalization.

### ❌ Techniques That Decreased Performance
- The **Dropout-only Model** showed a decline in performance with a **validation loss of 309,714** and an **R² score of 0.9567**.
    - This may indicate that the Dropout rate was too high or the model architecture was too simple.
- The **L1 & L2 Regularization Model** performed the worst, with the **lowest R² score (0.8806)** and the **highest validation loss (853,169)**.
    - This suggests that the regularization penalties were too strong, limiting the model’s learning capacity.

### 🧩 General Conclusion
- More complex regularization techniques (Dropout, L1/L2) do not always guarantee better performance, especially on smaller or well-structured datasets.
- The **Base Model** likely had just the right capacity to fit the data without overfitting.
- On larger datasets or more complex problems, techniques like **Batch Normalization + Dropout** may provide better generalization.
