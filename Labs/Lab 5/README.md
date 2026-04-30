1. Why is it often better to impute missing values with the median instead of the mean?
The median is "robust," meaning it isn't easily swayed by outliers. In a dataset like the Titanic, a few passengers with very high fares or very old ages would pull the mean (average) significantly higher, making it unrepresentative of the "typical" passenger. The median stays at the true middle point regardless of those extreme values.

2. What is One-Hot Encoding and why is it necessary?
One-Hot Encoding converts categorical text (like "Male" and "Female") into new binary columns (0s and 1s).

Why it's necessary: Machine learning models are essentially giant calculators—they can't "multiply" or "subtract" the word "Cherbourg." They require numerical input to perform the mathematical operations needed to find patterns and make predictions.

3. Would you need to apply Feature Scaling to a Decision Tree model?
No. Decision Trees are "scale-invariant."

Why: A Decision Tree makes its splits based on whether a value is greater than or less than a certain threshold (e.g., Age > 30). This logic doesn't change whether the age is 30, 0.3, or 3,000. Because each feature is handled independently during a split, the relative scale between different features (like Age vs. Fare) doesn't affect the tree's performance.