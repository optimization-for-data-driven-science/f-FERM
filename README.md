# f-FERM: Scalable Fair Empirical Risk Minimization via f-divergences
f-FERM is a fair machine learning framework that uses f-divergences to measure fairness violation. f-divergences cover many previous measures for evaluating the group fairness violation, such as KL-divergence, Chi-Square divergence, and total variations. Furthermore, it reformulates the fair empirical risk minimization as a min-max problem such that the gradient estimator of the loss function is available. Therefore, the presented algorithm shows a convergent behavior for any batch size as small as 1. Please visit our paper for the details of our reformulation and convergence guarantees at [ICLR 2024: f-FERM](https://openreview.net/pdf?id=s90VIdza2K).       

## Formulation for Demographic Parity


![alt text](https://github.com/optimization-for-data-driven-science/f-FERM/blob/main/Formula.png)
The objective function consists of two terms: 

1) The mean of a loss function (e.g., logistic regression, NNs, ...) over n data points 

2) f-divergence between the joint distribution of predictions and sensitive attributes and the product of their marginals. This term will be zero if and only if the model is fair under the demographic parity notion.

By determining lambda, one can specify a tradeoff between fairness and accuracy.
