* By scaling feature, we can get faster convergen when using gradient decent method.
* Two ways to get solution for J(theta)

|Gradient Decent | Normal Equation |
|-----|-----|
| Need to choose alpha | No need to choose alpha | 
|Need many iterations | no need to iterate |
|work well even when n (# of features) is large | need to compute inv(X^TX) : slow when n is large|

## Models ##
1. Linear Model
1. Polynomial Model
1. Logistic Model

## Remarks ##
1. Decision Bounadary may be different by choices for our moddels(hypothesis).
1. Logistic regression을 쓰고, L2 Error를 cost function으로 쓰면 non-convex네요.
	- 그래서 convex로 만드는 Cost function을 찾아요.
	- cost function 정하는 건 어렵네 : Convex도 되야하고, 의미적으로도 맞아야하고!
1. What if multi-classes?
    - one vs rest : h^i_theta(x) = P(y=i : x=theta) for i = 1, 2, 3, ...
    - Pick max_i h^i_theta(x)
1. Why should we use non-linear machine learning? 
    - the example : car detection (image is a just matrix, it cannot be a feature for ML)

## What can we do more when we have unacceptably large errors in its predictions? ##
1. Get more training examples : *Fixes High Variance*
1. Try Smaller sests of features : *Fixes High Variance*
1. Try getting additional features : *Fixes High Bias*
1. Try adding polynomial features : *Fixes High Bias*
1. Try decreasing lambda : *Fixes High Bias*
1. Try increasing lambda : *Fixes High Variance*

## Training / Cross Validation / Test ##
1. ratio = 3:1:1
1. Min J(Theta)
1. Compute J_cv(Theta)
1. Choose a model for the minimal value
1. Estimat generalization error J_test(Theta)

## Bias vs. Variance ##
1. Compare J_train, J_cv, J_test
	1. # of features (ex. degree of polynomial)
	1. penalty term lambda
	1. training set size

1. What if Neural networks
	1. Simple : Prone to underfitting
	1. Complex : Prone to overfitting


# Summary #
1. Linear Regression
1. Logistic Regression
1. Neural Network (Logistic)
1. Support Vector Machine

## PCA ##
1. PCA는 new axis를 찾는 것 : projceted data의 error가 minimize되도록
1. Linear Regression : |y_i - h(x_i)|^2 
1. PCA : distance to the line(plane)

## Anomaly Detection ##
1. Estimate Probability distribution of a feature
1. Usually we use normal distribution

## Anomaly Detection vs. Supervised Learning ##
1. If we have labeled data, what is good choice for anomaly detecting?
1. Anomaly
    1. Very small number of positive examples (0-20) (skewed data)
    1. Large number of negatives : good to estimate probability! (we don't use anomaly for estiation of probability)
    1. Future anomalies may look nothing like any of the anomalous examples we've seen so far(new anomality)
1. Supervised Learning
    1. Large number of positive and negative examples(not skewed data)
    1. Enough positive examples for algorithm to get a sense of what positive examples are like. (enough information for positive/negative situation)
