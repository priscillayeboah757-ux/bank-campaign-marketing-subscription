# bank-campaign-marketing-subscription
Predicting whether a customer will subscribe to a term deposit after campaign

Evaluation Metrics
Precision (Class 1 - Yes): 0.77, this means that the model predicts that a customer will subscribe, it is correct 77% of the time. This helps minimize wasted effort on customers unlikely to subscribe.
Recall (Class 1 - Yes): 0.78, this also successfully identifies 78% of all actual subscribers in the dataset. This ensures we don't miss out on too many potential conversions.
F1-Score: 0.77, shwing that a balanced harmonic mean of precision and recall, showing stable model behavior.
ROC-AUC: 0.8539, showing a high AUC of ~0.85 indicates excellent discriminative power. The model is highly capable of distinguishing between subscribers and non-subscribers.

Business Value & Customer Prioritization
This model resembles a standard predictive routing or CRM lead-scoring system. In a real business setting, you can use this model to prioritize customers for future campaigns as follows:

Propensity Scoring: Instead of predicting a binary 'yes' or 'no', we can extract the predicted probability (using predict_proba). Customers with a high probability (e.g., > 80%) can be labeled as "High Value Targets".
Resource Optimization: Call center agents can contact customers in descending order of their subscription probability. This maximizes conversions early in the campaign and reduces call center overhead costs (minimizing contact with "low propensity" customers).
Optimal Contact Timing: Features like duration (the length of the last call) have high predictive power. While duration is only known after a call starts, historical indicators like poutcome (previous campaign success) allow marketing teams to filter targets even before picking up the phone.
