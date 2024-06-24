# Ch1

**Create a model/learner**

choose/design feature

how to use feature

Use scatterplot matrix to explore features' correlation

# Ch2

First two variable type are classical discrete (labels) and continuous variables.

A third variable type is ordered categorical, such as small, medium and
large, where there is an ordering between the values, but no metric notion
is appropriate (the difference between medium and small need not be the
same as that between large and medium). These are discussed further in
Chapter 4

least-square: minimise 2-norm of residual

A large subset of the most popular techniques in use today are variants of
these two simple procedures. In fact 1-nearest-neighbor, the simplest of all,
captures a large percentage of the market for low-dimensional problems.
The following list describes some ways in which these simple procedures
have been enhanced:
• Kernel methods use weights that decrease smoothly to zero with distance from the target point, rather than the effective 0/1 weights used
by k-nearest neighbors.
• In high-dimensional spaces the distance kernels are modified to emphasize some variable more than others.

• Local regression fits linear models by locally weighted least squares,
rather than fitting constants locally.
• Linear models fit to a basis expansion of the original inputs allow
arbitrarily complex models.
• Projection pursuit and neural network models consist of sums of nonlinearly transformed linear models.

When metric averaged square error, the best predition is conditional mean

when metric is L1, the best prediction is conditional median

when classification with 0/1 loss - Bayesian classifier

the error rate of this method is called Bayes rate


The principle of maximum likelihood assumes that the most reasonable
values for θ are those for which the probability of the observed sample is
largest.


Any method that attempts to produce locally varying functions in small isotropic neighborhoods will run
into problems in high dimensions—again the curse of dimensionality. And
conversely, all methods that overcome the dimensionality problems have an
associated—and often implicit or adaptive—metric for measuring neighborhoods, which basically does not allow the neighborhood to be simultaneously small in all directions.


Roughness Penalty and Bayesian Methods

$$
PRSS(f):=RSS(f)+\lambda J(f),
$$

where $J$ will be large for functions f that vary too
rapidly over small regions of input space

Penalty function, or regularization methods, express our prior belief that
the type of functions we seek exhibit a certain type of smooth behavior, and
indeed can usually be cast in a Bayesian framework.

Kernel Methods and Local Regression
These methods can be thought of as explicitly providing estimates of the regression function or conditional expectation by specifying the nature of the
local neighborhood, and of the class of regular functions fitted locally.


Basis Functions and Dictionary Methods

## Excercise

**2.1**

Say $\hat{\vec y}=(y_1,y_2,\cdots,y_n)$.

$$
e_k:=||\vec t_k-\hat{\vec y}||_2^2=\sum_{i\ne k}y_i^2+(1-y_k)^2.
$$

$$
e_p-e_q=y_q^2+(1-y_p)^2-y_p^2-(1-y_q)^2\\
\ \\
=2(y_q-y_p)<0\\
\ \\
\implies e_p<e_q\iff y_p>y_q.
$$

So choose max $y_i$ can minimise error.
