1. Scenario: Spam Email Filtering.

Why: You want to be extremely "precise" when you label an email as spam. If the precision is low, the model might accidentally send an important work email or a message from a family member (a False Positive) to the Junk folder. It is much better to see a few actual spam emails in your inbox (lower recall) than to lose one important legitimate email.

2. Scenario: Recall over Precision

Scenario: Cancer Screening or Emergency Brake Systems.

Why: In medical testing, you want to catch every single person who actually has the disease (High Recall). If the model has low recall, it means you are telling a sick person they are healthy (a False Negative), which is life-threatening. A False Positive (telling a healthy person they might be sick) is stressful, but it leads to more tests that will eventually find the truth.

3. Why Cross-Validation is more trustworthy
Answer: A single train-test split is vulnerable to the "luck of the draw." * Depending on your random_state, you might accidentally put all the "easy-to-predict" passengers in your test set, making your model look better than it actually is.

Cross-validation rotates the test set through every piece of data you have. By averaging the scores from 5 different "folds," you get a much more stable and realistic estimate of how the model will perform on data it has never seen before.