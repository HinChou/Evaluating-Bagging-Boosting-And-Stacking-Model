# Evaluating-Stacking-Model-With-And-Without-Cross-Validation

Reference:
https://www.quora.com/What-is-stacking-in-machine-learning

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


