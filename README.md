# Evaluating-Bagging-Boosting-And-Stacking-Model

All three are so-called "meta-algorithms": approaches to combine several machine learning techniques into one predictive model in order to decrease the variance (bagging), bias (boosting) or improving the predictive force (stacking alias ensemble).

Every algorithm consists of two steps:

1. Producing a distribution of simple ML models on subsets of the original data.
2. Combining the distribution into one "aggregated" model.

## Bagging:
It is the way decrease the variance of your prediction by generating additional data for training from your original dataset using combinations with repetitions to produce multisets of the same cardinality/size as your original data. 

## Boosting:
It is a two-step approach, where one first uses subsets of the original data to produce a series of averagely performing models and then "boosts" their performance by combining them together using a particular cost function (for example: majority vote). Unlike bagging, in the classical boosting the subset creation is not random and depends upon the performance of the previous models: every new subsets contains the elements that were (likely to be) misclassified by previous models.

## Stacking:
It is a similar to boosting: you also apply several models to your original data. The difference here is, however, that you don't have just an empirical formula for your weight function, rather you introduce a meta-level and use another model/approach to estimate the input together with outputs of every model to estimate the weights or, in other words, to determine what models perform well and what badly given these input data.

Unlike bagging and boosting, stacking may be (and normally is) used to combine models of different types. The point of stacking is to explore a space of different models for the same problem. 

The idea is to attack a learning problem with different types of models which are capable to learn some part of the problem, but not the whole space of the problem. 

Steps of Stacking:

1. Build multiple different learners and use them to build an intermediate prediction, one prediction for each learned model. 
2. Add a new model which learns from the intermediate predictions the same target. 
3. This final model is said to be stacked on the top of the others, hence the name. 

![alt tag](https://github.com/HinChou/Evaluating-Stacking-Model-With-And-Without-Cross-Validation/blob/master/Stacking%20Chart.jpg)

Thus this might improve the overall performance, and often it ends up with a model which is better than any individual intermediate model. 

### Notice
Stacking does not gives any guarantee of improving the overall predictive power, as is often the case with any machine learning technique.

### Importance:
As you see, these all are different approaches to combine several models into a better one, and there is no single winner here: everything depends upon your domain and what you're going to do. You can still treat stacking as a sort of more advances boosting, however, the difficulty of finding a good approach for your meta-level makes it difficult to apply this approach in practice.

![alt tag](https://github.com/HinChou/Evaluating-Bagging-Boosting-And-Stacking-Model/blob/master/Bagging_Boosting_Stacking_Comparison_Table.jpg)

References:
* http://stats.stackexchange.com/questions/18891/bagging-boosting-and-stacking-in-machine-learning
* https://www.quora.com/What-is-stacking-in-machine-learning

