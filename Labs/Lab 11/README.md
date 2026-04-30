Model Parameters: These are internal to the model and are learned automatically from the training data. For example, the weights in a neural network or the coefficients in a linear regression.

Hyperparameters: These are external configurations set by the programmer before training begins. They control the learning process itself. Examples include the number of trees in a Random Forest (n_estimators) or the maximum depth of a tree (max_depth).

2. When would you choose to use Grid Search over Random Search, and vice-versa?
Use Grid Search: When you have a small "search space" (few hyperparameters and few values to test). It is exhaustive and guaranteed to find the best combination within your specified grid, but it becomes very slow as you add more variables.

Use Random Search: When you have a large search space or a limited computational budget. It doesn't check every combination, so it is much faster and often finds a "good enough" or even optimal result by sampling the most important hyperparameters more efficiently.

3. Looking at the AutoGluon leaderboard, which model performed the best? What does AutoML do that makes it so powerful compared to manual tuning?
Best Model: Based on the leaderboard, the WeightedEnsemble_L2 typically performs the best.

Power of AutoML: AutoML is powerful because it automates the most tedious parts of the pipeline: data preprocessing, feature engineering, and model selection. Its "secret sauce" is Ensembling—instead of picking just one model, it combines multiple different models (like LightGBM and Neural Nets) to cancel out individual errors and achieve higher accuracy than manual tuning usually allows.