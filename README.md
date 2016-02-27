* By scaling feature, we can get faster convergen when using gradient decent method.
* Two ways to get solution for J(theta)

|Gradient Decent | Normal Equation |
|-----|-----|
| Need to choose alpha | No need to choose alpha | 
|Need many iterations | no need to iterate |
|work well even when n (# of features) is large | need to compute inv(X^TX) : slow when n is large|