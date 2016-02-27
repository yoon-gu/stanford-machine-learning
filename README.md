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
	- 그래서 convex로 만드는 Cose function을 찾아요.
	- cost function 정하는 건 어렵네 : Convex도 되야하고, 의미적으로도 맞아야하고!