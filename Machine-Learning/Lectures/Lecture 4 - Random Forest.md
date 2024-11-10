---
Lecture-Date: 2024-10-21
Finish?: false
Study-Date:
---
---
>[!Example] Main Topics
>-
>-
>

# What is Random Forest?

- Is a supervised learning algorithm
- The "Forest" its builds : يعني هي شبه الغابة حرفيا 
- Usually trained with the "bagging" method 
	- يعنى بيجيبوا كذا Algorithm  و يدمجوهم سوا هي دي فكرة ال Bagging  

# How it Works ? 

- Builds multiple decision trees and merges them together to get a more accurate and stable prediction.
- Used for both classification and regression problems. 

### Classification 

![[Pasted image 20241031181202.png]]


![[Recording 20241031181549.webm]]


### Regression 

![[Pasted image 20241031183922.png]]


![[Recording 20241031184011.webm]]


# Example on Random Forest 
- In random Forest uses bootstrap sampling to create multiple datasets by randomly selecting samples.



# Difference between Decision Tree and Random Forest 

- The random forest algorithm randomly selects observations and features to build several decision trees and then averages the results.
- Decision trees might suffer from overfitting.
- Random forest prevents this by creating random subsets of the features and building smaller trees using those subsets.
- The randomness helps in reducing the correlation between individual trees.
- Can't overfit as easily as a single.


# Hyperparameter tuning 

1. n_estimators: 
	1. the number of decision trees in the forest.
	2. increasing this hyperparameter improves the performance of the model.
	3. But increases the computational cost of training and predicting.
2. max_depth: 
	1. the maximum depth of each decision tree in the forest.
	2. Setting a higher value for max_depth can lead to overfitting.
	3. Setting it too low can lead to underfitting.