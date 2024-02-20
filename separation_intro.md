# **Fairness** in machine learning

## Intro

In the field of deep learning, especially within the context of fairness, mathematical criteria are developed to ensure that algorithms make decisions that are equitable and do not perpetuate biases present in the data. One such criterion is the concept of **separation**, particularly relevant in binary classification tasks. This concept revolves around ensuring that the predictive model's decisions are fair with respect to a protected variable, such as race, gender, or age.

## Definition of Separation

Separation, in the context of fairness in machine learning, demands that the prediction (\(\hat{y}\)) should be conditionally independent of the protected attribute (\(a\)) given the true outcome (\(y\)). Formally, this can be represented as:

$$
P(\hat{y} | a, y) = P(\hat{y} | y)
$$

This criterion implies that, for individuals with the same outcome ($y$), their predicted outcome ($hat{y}$) should not depend on their protected attribute ($a$).
Essentially, it means that the model's predictions should be equally accurate for all groups defined by the protected attribute when they have the same true label.

## Importance of Separation

The separation measure is crucial for addressing and mitigating discrimination in automated decision-making processes. It targets the fairness of error rates across groups, such as equal false positive rates and false negative rates, ensuring that the algorithm's performance is consistent across different demographics.

## Accuracy vs. Fairness Trade-off

Implementing fairness constraints, like separation, often comes at the cost of overall model accuracy.

Fairness interventions can restrict the model's ability to fully leverage all available information in the training data, some of which may correlate with the protected attribute but also with the target variable. The challenge lies in finding a balance that minimizes unfair bias without unduly compromising the model's predictive performance.
