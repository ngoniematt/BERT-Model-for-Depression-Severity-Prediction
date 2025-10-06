# BERT-Model-for-Depression-Severity-Prediction
Code and experiments for a BERT regression model that estimates depression severity from social-media text

Features:

🧠 Regression on continuous severity scores (e.g., 0–1).

🧹 Lightweight preprocessing tuned for noisy social-media text.

⚖️ Imbalance handling: weighted loss and simple oversampling.

📏 Metrics: MSE, MAE, R², accuracy/F1 via thresholded class mapping.

🔁 Reproducibility: fixed seeds, deterministic flags, and run logs.

🔍 Explainability: attention visualisation or SHAP overlays.


Hyperparameters

| Param            | Value  | Notes |
|------------------|--------|-------|
| model_name       | bert-base-uncased | Backbone |
| max_length       | 128    | Tokenised sequence length |
| batch_size       | 16     | Effective batch size if no grad acc |
| lr               | 2e-5   | AdamW learning rate |
| weight_decay     | 0.01   | L2 regularisation |
| epochs           | 5      | Training epochs |
| warmup_ratio     | 0.06   | Linear warmup fraction |
| dropout          | 0.1    | Head dropout |
| use_weighted_loss| true   | Class-imbalance mitigation |
| oversample       | false  | Simple oversampling |
| seed             | 42     | Reproducibility |
