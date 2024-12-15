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

# What is Decision Trees

- Is a **supervised learning** algorithm that is used for classification and regression modeling.


## Decision Trees Components

![[Pasted image 20241215044816.png]]
-  **Internal node**: test on attribute X (Outlook, Humidity, Wind)
-  **Branch from a node:** Selects one value for X (Sunny, Overcast , High)
-  **Leaf node**: predict Y (Yes, No) are the endpoints of the tree.

#### Note
- If features are continuous, internal nodes can test the value of a feature against a threshold.

## Ockham's Razor: preference bias

- **Idea:** The simplest consistent explanation is the best.
- The smallest decision tree that correctly classifies all of the training examples is best.
	- Finding the smallest decision tree


# Choosing the Best Attribute 

- The ID3 algorithm uses the Max-Gain method of selecting the best attribute.
- **Impurity/ Entropy:**
	- Measures the level of **impurity** in a group of examples.
	- Is the mutual Information between input attribute A and target Variable Y.

![[Pasted image 20241215045833.png]]
