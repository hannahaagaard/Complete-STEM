# Unit Summary
Tags: #Summary #UAG #Math #Inference #Decision

Relevant files: [[Stats Unit 2 Lecture 1.pdf|Lecture 1]], [[Stats Unit 2 Lecture 2.pdf|Lecture 2]], [[Stats Unit 2 Lecture 3.pdf|Lecture 3]], [[Stats Unit 2 Lecture 4.pdf|Lecture 4]]

## What is a hypothesis test?
Relevant links: [[Stats Unit 2 Lecture 1.pdf|Lecture 1]]
- Instead of trying to figure out the specific value of something you're trying to put it into a region
- Create two sitations and calculate the probability of observing the data given a model of the data
	- Assumed situation null hypothesis : $H_0$
	- Other situation is the alternative hypothesis: $H_a$
	- Create a test statistic to calculate given data: $U$
		- **The distribution of $U$ must be known under $H_0$ 
	- Create a rejection region to discriminate between the hypotheses: $RR$
	- Have a significance level: $a$ 
		- Describes the probability of the test statistic is in the rejection region under $H_0$ 
		- In a formula: $\large{\mathbb{P}^0(U \in RR) = \alpha}$
		- $\alpha \in (0, 1) \text{ and } \alpha \ll 1$
- Construct a hypothesis test using
	- A test statistic: $U$
	- A rejection region which describes a region of $U$
- Input of a hypothesis test
	- The nature of the parameters $\theta$ (using in making the test statistic)
	- A null hypothesis ($H_0$) which is a subset of all possible values of $\theta$
	- An alternative hypothesis ($H_a$) which is another subset of all possible values of $\theta$ 
	- A significance level $\alpha \in (0, 1)$
- Process
	- Calculate test statistic
	- If the test statistic is in $RR$ we reject $H_0$ and say $H_a$ is more likely
	- Otherwise we fail to reject $H_0$

### Types of Hypothesis Tests
The relationship between $H_0$ and $H_a$ is very important and there are largely three different situations
$$
\begin{align}

	H_0 = \{\theta = \theta_0\} &&
	H_a = \begin{cases} 
			\theta \lt \theta_0 \text{ (left tailed)} \\
			\theta \ne \theta_0 \text{ (simple / singleton) }\\
			\theta \gt \theta_0 \text{ (right tailed)}
		  \end{cases}
\end{align}
$$
### Types of Error
[Wiki page](https://en.wikipedia.org/wiki/Type_I_and_type_II_errors)
Generally the intuition of decreasing $\alpha$ is a good idea but making it too small is dangerous as well due to the different types of error. The idea of each of the types of error can be summarized really quickly in the following table

\ | $H_0$ is true | $H_0$ is false
--| -----| ---
Failed to reject $H_0$ | True negative: $\large\mathbb{P} = 1 - \alpha$ | False negative / Type 2 Error $\large\mathbb{P} = \beta$
Rejected $H_0$ | False positive / Type 1 Error (false positive) $\large\mathbb{P} = \alpha$ | True positive $\large\mathbb{P} = 1 - \beta$
Effectively $\alpha$ and $\beta$ describe the probability of a type 1 or type 2 error occuring

Assuming a singleton situation the following definitions can be used to the error rates!
$$
\large\begin{align}
	\alpha = \mathbb{P}^0(U \in RR) \\
	\beta = \mathbb{P}^\alpha(U \notin RR)
\end{align}
$$
## [[1 Normal Sample Tests]]
Relevant links: [[Stats Unit 2 Lecture 1.pdf|Lecture 1]]
Here we are assuming that all random variables have a normal distribution behind them of some mean and variance. Typically it's assumed that the variance is known but this is not always the case.

#### Mean categorization
The first situation which comes up is when you're trying to categorize the mean. *The example here is assuming that the variance is not known.* This results in using a T-distribution instead of a normal distribution
$$
\large\begin{align}
	H_0 = \{\mu = \mu_0\} \\\\ 
	H_\alpha = 
		\begin{cases}
			\mu \lt \mu_0 \\
			\mu \gt \mu_0 \\
			\mu \ne \mu_0
		\end{cases} \\\\
\end{align}
$$
	The rejection region is respective
$$
\large\begin{flalign}
	U = \sqrt{n}\frac{\bar{Y} - \mu}{S} \sim T(n-1) \\\\
	RR = \begin{cases}
		(-\infty, -t_{\alpha}], \\
		[t_{\alpha}, \infty), \space\\
		(-\infty, -t_{\alpha/2}]\space \cup \space [t_{\alpha/2}, \infty),
	\end{cases}
\end{flalign}
$$
#### Mean difference
There is also a test which is useful for categorizing the difference between two means. **However this assumes that the variances are equal. I.E:  $\large\sigma_1^2 = \sigma_2^2$**

$$
\large\begin{align}
	H_0 = \{\mu_1 - \mu_2 = D_0\} \\\\
	H_\alpha = \begin{cases}
		\mu_1 - \mu_2 \lt D_0 \\
		\mu_1 - \mu_2 \gt D_0 \\
		\mu_1 - \mu_2 \ne D_0
	\end{cases}
\end{align}
$$
$$
\large\begin{align}
S_p^2 = \frac{(n_1 - 1)S_1^2 + (n_2 - 1)S_2^2}{n_1 + n_2 - 2} && 
U = \frac{\bar{Y} - \bar{Z} - D_0}{S_p \sqrt{1/n_1 + 1/n_2}} 
	\sim T(n_1 + n_2 - 2)
\end{align}
$$
all of this is assuming $\large\mathbb{P}^0$ so assuming that the null hypothesis is right

#### Variance categorization
This is categorizing the variance of a normal distribution. There is a natural test statistic and hypothesis set for this situation
$$
\large\begin{align}
	\text{Hypothesis set }\\
	H_0 = \{\sigma^2 = \sigma^2_0\} \\
	H_\alpha = \begin{cases}
		\sigma^2 \lt \sigma^2_0\\
		\sigma^2 \gt \sigma^2_0\\
		\sigma^2 \ne \sigma^2_0
	\end{cases}
\end{align}
$$
$$
\large\begin{align}
	U = \frac{n - 1}{\sigma_0^2}S^2 \sim \chi^2(n-1)\\\\
	RR = \begin{cases}
		(0, \chi_{1-\alpha}^2] \\
		[\chi_{\alpha}^2, \infty) \\
		(0, \chi_{1-\alpha/2}^2] \space \cup \space [\chi_{\alpha/2}^2, \infty)
	\end{cases}
\end{align}
$$

## [[2 Asymptotic Tests]]
Relevant links: [[Stats Unit 2 Lecture 2.pdf|Lecture 2]]

This entire seciton is about using the Central Limit Theorem and various theorems to approximate normal distributions with large sample sizes

#### Mean Categorization
This is very similar to before with the mean categorization. Really the only difference is that you need to use an estimator which is asymptotically normal to the mean instead of only using the sample mean.

Effectively this means that the math is very similar but there is an additional step to determining what an asymptotic estimator to use. 

#### Mean difference
Previously it was assumed that the variance of both distributions was the same. However, in the example we are not going to assume that this is the case. Instead we will assume that we have roughly the same number of samples in either pool. This is represented in the following quantity being bounded

$$
\frac{|n_1 - n_2|}{\sqrt{n_1} + \sqrt{n_2}}
$$
Using this we can construct the following hypothesis set and test statistic
$$
\large\begin{align}
	H_0 = \{\mu_1 - \mu_2 = D_0\} \\\\
	H_\alpha = \begin{cases}
		\mu_1 - \mu_2 \lt D_0 \\
		\mu_1 - \mu_2 \gt D_0 \\
		\mu_1 - \mu_2 \ne D_0
	\end{cases}
\end{align}
$$
$$
\begin{align}
	U = \frac{\bar{Y} - \bar{Z} - D_0}{\sqrt{\hat{\sigma_1}^2/n_1 + \hat{\sigma_2}^2/n_2}} \to N(0, 1)
\end{align}
$$
And this particular construction uses the normal rejection regions!

## [[3 Designing Tests & Statistics]]
Generally you can only improve the statistics of a test by doing one of two things
1. Increasing the number of samples
2. Finding/making a more efficient test statistic

This section is entirely about how you go about designing better tests and comparing between the different tests

### Choosing Sample Sizes
Do you remember how in [[#Types of Error]] we gave some definitions for type 1 and 2 error? Well using those definitions assuming singleton / simple hypothesis tests we can actually figure out about how large our samples need to be! 

Using the singleton definitions we can derive two equations *which hold under technical assumptions*. Those equations describe how the error probabilities (in particular $\beta$) relates to the CDF of a normal distribution (yes this is under Asymptotic behavior)

$$
\large\begin{align}
	\beta = \mathbb{P}^{\alpha}(U_n \le z_\alpha - \frac{\sqrt{n}(\theta_\alpha - \theta_0)}{\hat{\sigma_n}})

	& \approx \Phi(z_\alpha - \frac{\sqrt{n}(\theta_\alpha - \theta_0)}{\hat{\sigma_n}}) \\\\

\text{which leads to} \\\\

n = \frac{(z_\alpha + z_\beta)^2 \hat{\sigma_n}^2}{(\theta_\alpha - \theta_\beta)^2}

\end{align}
$$
This isn't fully indep. of n due to the variance estimator but you can just take a small sample to approximate and then go from there!

### P-value
This communicates the minimum $\alpha$ needed in order to reject the null hypothesis. That way you can choose what results you would like to accept or reject depending on how strict you need to be!

### Power of Tests
The power of a test describes the probability of a false positive using the test statistic for this hypothesis test. Formally it's defined at:
$$
\large Power(\theta_0):= \mathbb{P}^{\theta}(U \in RR)
$$
This definition gives a method to compare different tests in addition, to the confidence level that they produce. We do have a theorem though
>[!note]- Neyman-Pearson Lemma
>For simple hypothesis tests the most powerful $\large \alpha$-tests is given by:
>
>$$\large U = \frac{L(Y_1, \dots, Y_n; \theta_0)}{L(Y_1, \dots, Y_n; \theta_\alpha)}, RR = \lbrack 0, r(\alpha))$$
>
>where L is the likelihood function and $r(\alpha)$ is chosen so that:
>$$\large \mathbb{P}^{\theta_0}(U < r(\alpha)) = \alpha$$
>
>**Requirements**
>---
>1. Need to know how to compute the likelihood function
>2. Need to know the distribution of $\large U$ under $\large H_0$


### General likelihood ratio tests
## [[4 ANOVA & Categorical Data]]
