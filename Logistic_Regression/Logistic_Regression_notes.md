# Logistic Regression 
- Logistic regression is used for binary classification (e.g., 0 or 1).

- It predicts the probability of input belonging to class 1.

- Uses the sigmoid function to map real numbers into probabilities between 0 and 1.

## 🧠 Model Formula
- Linear part: z = **w.x** + b

- Sigmoid output: y_hat = 1 / (1 + exp(-z))

## 📏 Sigmoid Function
- Input: scalar or vector (z)

- Output: values in range (0, 1)

- Interpreted as a probability

- sigmoid(0) = 0.5 (model is unsure)

- Accepts both:

- Single example → scalar z

- Multiple examples → vector z

## ⚖️ Threshold for Classification
- Default threshold = 0.5

- If y_hat >= threshold → predict class 1

- If y_hat < threshold → predict class 0

- You can raise threshold (e.g., to 0.7) to require more confidence before predicting class 1
- 
**Changing the threshold:**

- Does not change the sigmoid curve

- Does change the decision rule

## Decision Boundary
- The decision boundary is where the model is unsure — where y_hat = threshold

- For default threshold 0.5 → boundary is where z = 0

- For other thresholds → boundary is where z = ln(t / (1 - t))

- It’s a line (2D), plane (3D), or hyperplane (nD) in the feature space

- The shape of the boundary depends on weights w

- Conceptual, not a physical object

**On the Sigmoid Plot**
- X-axis = z

- Y-axis = sigmoid(z)

- Vertical line at z = 0 is the decision boundary (when threshold = 0.5)

- Horizontal line at y = 0.5 shows the cutoff probability

## Conceptual Clarifications
- Changing the threshold changes predictions, not the sigmoid shape

- The decision boundary in feature space separates inputs into class 0 or 1

- In the sigmoid plot, the boundary appears as:

- Vertical (in terms of z)

- Horizontal (in terms of probability cutoff)

- The boundary is vertical in feature space if one feature is dominant or if there's only one feature

