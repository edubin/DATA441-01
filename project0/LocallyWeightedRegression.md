## Introduction to Locally Weighted Regression ##

**Main Idea**: Make predictions as a weighted combination of the input feauture values; the weights can be positive or negative. Expressed as an intuitive equation the idea is as follows:

$$\text{Predicted Value} = weight_1 \cdot \text{Feature}_1 + weight_2 \cdot \text{Feature}_2 + ... + weight_p \cdot \text{Feature}_p $$

<font color='darkred' size=4pt>Message: In Machine Learning the "machine" is learning the weights based on iterative processes. Typically, the updates are based on a gradient descent method for minimizing an objective function, such as the sum of squared errors.
