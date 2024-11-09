---
Lecture-Date: 2024-10-07
Finish?: true
Study-Date: 2024-10-15
---
---
>[!Example] Main Topics
>- Types of Machine Learning 
>- No
>


# Types of Machine Learning 
1. Supervised (Inductive) learning 
	1. Training data 
	2. Desired outputs (Labels/Labeled Data)
2. Unsupervised Learning 
	1. Training data (without desired outputs)
3. Semi-Supervised Learning 
	1. The model learn from himself. By generating its own label from the input data.
4. Reinforcement Learning
	1. The model learn from Reward and Penalties.


# Supervised Learning
- Where the training data you feed to the algorithm includes the desired solutions.
- Called labels id divided into
	- Classification 
	- Regression

## 1. Classification 
- you train the data with their class.
- The model must learn how to classify the data. 

## 2. Regression 
- Predict a target numeric value (price of car).
- Called predictor.
- To train the system, you need to give it many examples of cars, including both their predictors and their labels.


# Unsupervised Learning 
 - The training data is unlabeled.
 - The model tries to learn without a teacher
 - The model find structure and pattern in the data on its own. 
	 - Given input 
	 - Hidden Output


## 1. Clustering 
- Try to find structure and pattern in the data on its own to divide the visitor into clusters.
![[Recording 20241109160125.webm]]

## 2. Dimensionality Reduction 
- The goal is to simplify the data without losing too much information, it has two types 
	- Merge several correlated features into one (Feature extraction).
	- Select features from many features which is more related to problem (feature Selection)
- <span style="color:rgb(0, 176, 80)">Advantages</span> 
	- Model will run faster 
	- Data will take up less space and memory

## 3. Anomaly Detection 
- Know as outliers detection
- Used to identify the unusual patterns or observation in data known as (Outliers or anomalies).


## 4. Association rule Learning 
- The goad is to dig into large amounts of data and discover interesting relations between attributes.



# Semi-Supervised Learning 

- Are combination of unsupervised and supervised algorithms
![[Recording 20241109161247.webm]]

# Self-Supervised Learning 
- the idea is that by solving these tasks, the model learns useful representations of data, which can then be used for others tasks such as classification, detection , or segmentation.

# Reinforcement Learning 

- Learning by Reward o Punishment. 


# Types of Learning From another perspective 

## 1. In batch Learning 
- The system is incapable of learning incrementally. 
- it must be trained using all the available data.
- This will generally take a lot of time and computing resources.
- so it is typically done offline.
- <span style="color:rgb(0, 176, 80)">Steps</span>
	-  First the system is trained 
	- then it is launched into production and runs without learning anymore 
	- It just applies what it has learned.
	- This called offline learning
- The machine learning model is trained using the entire dataset at once

## 2. In Online Learning 
- You train the system incrementally by feeding it data instances sequentially, individually or by small groups called mini-batches.
- The system can learn about new data on the fly.


## 3. Instance-Based learning
- The system learns the examples by heart, then generalizes to new cases by comparing them to the learned examples.

## 4. Model-based Learning
- Is another way to generalize from a set of 


# Main challenges in ML

- If data is <span style="color:rgb(255, 0, 0)">Bad</span> due to 
	- Insufficient Quantity of Training Data 
		- 
	- Nonrepresentative Training Data 
		- Sampling Noise 
		- Sampling Bias
	- Poor-Quality Data 
		- Incomplete Data 
		- Inconsistent Data 
		- Outdated Data
	- Irrelevant Features 
		- Feature engineering


# Overfitting the Training Data
- It means that the model performs well on the training data, but it does not generalize well.
- Key characteristic of overfitting : 
	- High Training Accuracy 
	- Poor Generalization
	- Capturing Noise 
	- Complex Models:
- Cause of Overfitting:
	- **Too Complex Models**: Models with too many parameters relative to the amount of training data are prone to overfitting.
	- **Insufficient Data**: Data sets is small, the model may find it easier to memorize the data rather than generalize from it.
	- **Noise in Data**: If the training data contains noise or irrelevant patterns, the model may learns these as if they are genuine features 

