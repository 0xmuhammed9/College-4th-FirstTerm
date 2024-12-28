---
Lecture-Date: 
Finish?: false
Study-Date:
---
---

# 1. Nearest Neighbor 

- One of the Simplest of all machine learning Classifiers.
- Label a new point the same as the closest known point. 

## How does the K-Nearest Work? 
1. Compares a new data entry to the values in a given data set based on tits closeness or similarities in  a given range (K) of neighbors.
2. The algorithm assigns the new data to a class or category in the data set.

### Steps
- Assign a value to K 
- Calculate the distance between the new data entry and all other data.
- Find the K nearest to the new data based on the distance 
- Assign the new data to the majority class in the nearest.


![[Recording 20241216092451.webm]]

### Methods Used 

![[Pasted image 20241216092620.png]]

## Advantages 
1. It is simple to implement 
2. No training is required before classification.
## Disadvantages
1. Can be cost-intensive when working with a large data set.
2. A lot of memory is required for processing large data sets.
3. Choosing the right value of K can be tricky.
	1. If k is too small, sensitive to noise points 
		1. K = 1 , we run the risk of overfitting
	2. If k is too large, neighborhood may include points from other classes.
		1. if k is large (K=N) this is Underfitting 
4. So the K is the **hyperparameter** of the KNN that allows us to trade-off between overfitting (Small K) and underfitting (Large K).


# 2. Bayesian (Naive Bayes)

## What is Bayesian Algorithm?
- Is a classification technique with associate degree assumption of independence among predictors.
- A Naive Bayes Categorize assumes that the presence of a Specific feature in a class is unrelated to the presence of the other feature.

## What is the Naive Bayes Classifier ? 
1. Statistical Classification.
2. One of the simplest supervised leering.
3. Fast, accurate and reliable.
4. Used in Classification and Regression.
5. High Accuracy and Speed on Large Datasets.
6. Assume that the effect of a particular feature in a class is independent of other features.

### Advantages 
1. Very fast and can easily predict the class of a test dataset.
2. Solve multi-class prediction problems.
3. Less training data if the assumption of independence of features holds.
### Disadvantages
1. If test data set has a categorical variable of a category that wasn't present in the training dataset, the model will assign it zero.
2. Hardly find a set of independent features.