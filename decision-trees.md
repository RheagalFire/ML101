# Decision Trees

Another popular model in data science for both classification and regression is the [decision tree](https://en.wikipedia.org/wiki/Decision\_tree\_learning). It is a [binary tree](https://en.wikipedia.org/wiki/Binary\_tree) where each node of the tree decides on a particular feature of the dataset, and we descend to the node's left or right child depending on the feature's value.

If a feature is boolean, we go left or right from the node depending on if the feature value is true or false. If a feature is numeric, we can decide to go left or right based on a decision boundary for the feature (e.g. go left if the feature value is less than 1, otherwise go right). The leaves of the decision tree determine the class label to predict (in classification) or the real number value to predict (in regression).

![](<.gitbook/assets/image (10).png>)

Since a decision tree makes decisions based on feature values, the question now becomes how we choose the features to decide on at each node. In general terms, we want to choose the feature value that "best" splits the remaining dataset at each node. we use [Gini Impurity](https://en.wikipedia.org/wiki/Decision\_tree\_learning#Gini\_impurity), MSE (mean squared error), and MAE (mean absolute error) to decide on the best feature at each node.

Play around with this [notebook](https://github.com/RheagalFire/Scratch-Implementations/blob/master/Decision%20Trees.ipynb) to get an intuition behind decision trees.&#x20;

Also, check out [this](https://github.com/justmarkham/DAT8/blob/master/notebooks/17\_decision\_trees.ipynb) very illustrative and end-to-end implementation of decision trees in scikit-learn.

[This ](https://mlu-explain.github.io/decision-tree/)is a great visual representation of the working of decision trees. &#x20;

### What happens when we grow a tree too deep?

&#x20;The **training error** continues to go down as the tree size increases (due to overfitting).

### Example of Gini index

![](<.gitbook/assets/image (11).png>)



* The **maximum value** of the Gini index is 0.5 and occurs when the classes are perfectly balanced in a node.
* The **minimum value** of the Gini index is 0 and occurs when there is only one class represented in a node.
* A node with a lower Gini index is said to be more "pure".

&#x20;The decision tree algorithm will try **every possible split** and will choose the split that **reduces the Gini index (and thus increases the "node purity") the most.**

### Advantages of Decision Trees

* Can be used for regression or classification
* Can be displayed graphically
* Highly interpretable
* Can be specified as a series of rules, and more closely approximate human decision-making than other models
* Prediction is fast
* Features don't need scaling
* Automatically learns feature interactions
* Tends to ignore irrelevant features
* Non-parametric (will outperform linear models if the relationship between features and response is highly non-linear)

### Disadvantages of Decision Trees

* Performance is (generally) not competitive with the best-supervised learning methods
* Can easily overfit the training data (tuning is required)
* Small variations in the data can result in a completely different tree (high variance)
* Recursive binary splitting makes "locally optimal" decisions that may not result in a globally optimal tree
* Doesn't tend to work well if the classes are highly unbalanced.
* Doesn't tend to work well with very small datasets.
