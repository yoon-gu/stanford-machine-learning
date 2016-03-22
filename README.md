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
1. Get more training examples
1. Try Smaller sests of features
1. Try getting additional features
1. Try adding polynomial features
1. Try decreasing lambda
1. Try increasing lambda

## Training / Cross Validation / Test ##
1. ratio = 3:1:1
1. Min J(Theta)
1. Compute J_cv(Theta)
1. Choose a model for the minimal value
1. Estimat generalization error J_test(Theta)