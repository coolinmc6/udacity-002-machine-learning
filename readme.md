[Back to All Courses](https://github.com/coolinmc6/CS-concepts)

# Udacity: Intro to Machine Learning

Link: [Intro to Machine Learning](https://www.udacity.com/course/intro-to-machine-learning--ud120)


## Lesson #2: Naive Bayes

- [Naive Bayes Classifier](https://en.wikipedia.org/wiki/Naive_Bayes_classifier)
- **Decision Surface** is that line on the scatterplot that allows you to pick
which "type" a new data point more closely matches (e.g. red X's or blue O's)
  - if it's a straight line, we say that it's a **linear** decision surface
- what your ML algorithm does is it takes all of your data and creates a DS
(decision surface) so that with future data, you can make a determination as to
whether it is a red X or blue O

### 19. Quiz: GaussianNB Deployment on Terrain Data

- I don't entirely understand what a Naive Bayes Classifier is or exactly what it's doing. The objective
of the exercise is to use the sklearn Naive Bayes Classifier to classify the terrain
data. [Statistical Classification](https://en.wikipedia.org/wiki/Statistical_classification)

> In statistics, classification is the problem of identifying to which of a set of 
> categories (sub-populations) a new observation belongs, on the basis of a training 
> set of data containing observations (or instances) whose category membership is known

- **Exercise:** The objective of this exercise is to recreate the decision 
boundary found in the lesson video, and make a plot that
visually shows the decision boundary.
- See [l02/19_Quiz1](./l02/19_Quiz1) folder and then `ClassifyNB.py` for the answer
- As a reminder, per the [docs](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.GaussianNB.html),
there are two parameters in the `clf.fit(X,Y)` method. See this code:

```py
# features_train => the data that we're training the model on
# labels_train => the data with the answers
clf.fit(features_train, labels_train)
```

### 20. Quiz: Calculating NB Accuracy

- **accuracy** is defined as the number of test points that are classified 
correctly divided by the total number of test points.
- Here is the correct answer for that quiz:

```py
from sklearn.naive_bayes import GaussianNB
clf = GaussianNB()
clf.fit(features_train, labels_train)
pred = clf.predict(features_train)

import sklearn.metrics import accuracy_score
print accuracy_score(pred, labels_test)
```
- Another way to check accuracy you can do:

```py
print clf.score(features_test, labels_test)
```
