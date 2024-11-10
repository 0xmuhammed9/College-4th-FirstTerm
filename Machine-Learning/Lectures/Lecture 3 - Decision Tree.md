---
Lecture-Date: 2024-10-14
Finish?: false
Study-Date:
---
---
>[!Example] Main Topics
>-
>-
>


___

| Video                   | Link                                        | Recommend |
| ----------------------- | ------------------------------------------- | --------- |
| Decision Tree           | https://www.youtube.com/watch?v=9SFtiNMXf9A | Low       |
| Decision Tree Algorithm | https://www.youtube.com/watch?v=LtfExrMZpi0 | High      |
| Example                 | https://www.youtube.com/watch?v=coOTEc-0OGw | High      |



- A decision tree is a supervised learning algorithm that is used for classification and regression
- If the Entropy is Close to Zero this is good.
- If the Entropy is 1 : The Question is Discarded  ملوش لازمة يعني  
- We Search for Best Information gain to start the tree from it

# Preference bias: Ockham's Razor

### idea : The simplest consistent explanation is the best.

- The smallest decision tree that correctly classifies all of the training examples is best


# Information Gain

- Tell us how important a given attribute of the feature vectors is.
- Use it to decide the ordering of attributes in the nodes of a decision tree.
- Is the mutual information between input attribute a and target variable y.
- The expected reduction in entropy of target variable Y for data sample S, due to sorting on Variable A.
- 