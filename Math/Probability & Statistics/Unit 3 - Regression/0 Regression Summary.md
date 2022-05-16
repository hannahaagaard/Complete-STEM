# Unit Summary
Tags: #Summary #UAG

Relevant files: [[Stats Unit 3 Lecture 1.pdf|Lecture 1]], [[Stats Unit 3 Lecture 2.pdf|Lecture 2]], [[Stats Unit 3 Lecture 3.pdf|Lecture 3]]

## General Idea
The overall idea of regression is to take in data points and fit sometype of mathematical model to those points. We can think of this by describing the sets of independent and dependent as sets
$$
\large\begin{align}
	Independent &&&& Dependent \\
	\{X_i:=(X_{1i},...,X_{mi})\}_{i=1}^{n} &&&& \{Y_i\}_{i=1}^{n}
\end{align}
$$
From here we can build mathematical machinery to represent the relationships between these two sets which we can then estimate and approximate! In this notation we are going to represent any parameters using $\beta = \{\beta_i\}_{i=1}^{l}$. We can then represent the relationship between these sets like this
$$
\large Y = f(X, \epsilon; \beta)
$$
Where epsilon is the error, noise, or residual! This error is assumed to be i.i.d and independent of $\large X$. In addition the expectation is assumed to be zero.

The way we choose $\large f$ is how we choose different models and each one works with different types of data. In this class we are going to focus on **Linear regression models** (specifically one dimensional ones).  This class of models assumes a constant series of basis functions which take in the independent variables which are then added together. 
$$
\large f(x, \epsilon; \beta) = \beta_0 f_0(x) + \dots+\beta_k f_k(x) + \epsilon, \space \space x \in \Re^m
$$
The main question now becomes how do we find $\large \beta$ given some inputs and outputs?

## [[1 Least Squares Estimator]]
### One dimensional regression
From here on we are going to assume a one dimensional model which has the form
$$
\large Y = \beta_0 + \beta_1X + \epsilon
$$
One of the best estimators for the coefficients is the "Least Squares Estimator" which minimizes the squared difference between each of the points. Then the partial derivative can be taken and solved.
$$
\large\begin{align}
	&&&& \hat{\beta_0} = \bar{Y} - \hat{\beta_1}\bar{X} \\
	\min_{\beta_0, \beta_1 \in \Re} \sum_{i=1}^n(Y_i - \beta_0 - \beta_1 X_i)^2 \Rightarrow 
	&&&& \hat{\beta_1} = \sum_{i=1}^{n}\frac{(X_i - \bar{X})(Y_i - \bar{Y})}{(X_i - \bar{X})^2} =: \frac{S_{xy}}{S_{xx}}
\end{align}
$$

### LS Estimator Properties
There are multiple properties of this estimator that depend on the structure of the residue. It's thus **essential** that the errors are normal, i.i.d., and independent of X. 

Assuming all of these are true then the following is also true
- $\large \hat \beta$ is unbiased
- $\large \hat \beta$ is consistent
- Also assume X is deterministic, then for any real coefficients a,b the following combination is normal $\large a \hat{\beta_0} + b \hat{\beta_1}$

Using these properties and that the previous assumptions we can conclude the following properties when we know $\large\sigma^2$
$$
\large\begin{align}
V(\hat{\beta_0}) = \frac{\sigma^2 \sum_{i=1}^{n}x_i^2}{nS_{xx}}, \\ 
V(\hat{\beta_1}) = \frac{\sigma^2}{S_{xx}}, \\
cov(\hat{\beta_0}, \hat{\beta_1}) = -\sigma^2\frac{\bar x}{S_{xx}} \\
V(a\hat{\beta_0} + b\hat{\beta_1}) = a^2V(\hat{\beta_0}) + b^2V(\hat{\beta_1}) + 2ab \cdot cov(\hat{\beta_0}, \hat{\beta_1}) \\
\text{or } V(a\hat{\beta_0} + b\hat{\beta_1}) = \sigma^2\sigma^2_{ab}\space , \sigma^2_{ab} = \frac{\frac{a^2}{n}\sum_{i=1}^nx_i^2 + b^2 -2ab\bar{x}}{S_{xx}}
\end{align}
$$
This allows us to do amazing things like creating confidence intervals for any of the parameters!

## [[2 Estimating residuals]]
The previous analysis had the asumption that we knew what the variance of the residual is but that assumption is quite rare! However, as in [[3 Confidence Intervals|confidence intervals]] we found we could move away from this assumption by finding an estimator for the variance and then substituting that in!

The best estimator is quite typical for this situation by using the variance estimator
$$
\large\bar{S^2} = \frac{1}{n-2}\sum_{i=1}^n ((\epsilon_i - \bar\epsilon)^2 - (X_i - \bar X)^2\epsilon_i^2/S_{xx})
$$
This estimator results in the very intuitive distributions for the variance and mean
$$
\large\begin{align}
\frac{n-2}{\sigma^2}\hat S^2 \sim \chi^2(n-2) &&
\frac{a \hat\beta_0 + b \hat\beta_1 - a \beta_0 - b \beta_1}{\hat S\sigma_{ab}} \sim T(n-2)
\end{align}
$$


## [[3 Inference & Hypothesis testing]]
### Inferences about the dependant variables
### Hypothesis testing on the regression parameters
## [[4 Correlation & Nonlinear Extensions]]
### Correlation and $R^2$
### Nonlinear extensions