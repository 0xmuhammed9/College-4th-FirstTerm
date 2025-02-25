---
Lecture-Date: 2024-10-28
Finish?: false
Study-Date: 2024-12-03
---
 ---


### Support Vector Machines (SVM)

- **Type**: Traditional machine learning algorithm.
- **Purpose**: Primarily used for classification and regression tasks.
- **Mechanism**:
    - SVM finds a hyperplane in an n-dimensional space that distinctly separates data points into classes.
    - It uses the concept of maximizing the margin between data points and the separating hyperplane.
    - Can use kernel tricks (e.g., polynomial or RBF kernels) to handle non-linearly separable data.
- **Advantages**:
    - Works well with smaller datasets.
    - Effective in high-dimensional spaces.
    - Versatile with different kernel functions.
- **Limitations**:
    - Struggles with very large datasets.
    - Performance is sensitive to the choice of kernel and hyperparameters.
- **Example Use Cases**: Text classification, image recognition (with feature extraction), and bioinformatics.
### Deep Learning

- **Type**: A subset of machine learning based on neural networks.
- **Purpose**: Learns hierarchical feature representations directly from raw data.
- **Mechanism**:
    - Deep learning models consist of multiple layers of neurons where each layer extracts increasingly abstract features from the data.
    - Trains on large datasets using gradient descent and backpropagation.
- **Advantages**:
    - Handles large datasets effectively.
    - Learns features automatically without manual extraction.
    - Extremely flexible for various data types (images, text, audio, etc.).
- **Limitations**:
    - Requires substantial computational power.
    - Needs large labeled datasets to perform well.
- **Example Use Cases**: Speech recognition, natural language processing, and autonomous driving.
### Convolutional Neural Networks (CNNs)

- **Type**: A specialized type of deep learning architecture.
- **Purpose**: Designed for spatial data, especially image and video data.
- **Mechanism**:
    - CNNs use convolutional layers to extract spatial features (like edges, textures, and patterns) from images.
    - They combine these with pooling layers to reduce dimensionality and fully connected layers for final classification or prediction.
- **Advantages**:
    - Exceptional performance in image processing tasks.
    - Reduces the need for manual feature extraction.
    - Can generalize well for unseen image data with sufficient training.
- **Limitations**:
    - Computationally intensive, requiring GPUs or TPUs.
    - Requires large labeled datasets for high performance.
- **Example Use Cases**: Facial recognition, medical imaging, object detection.

### Key Differences

|**Feature**|**SVM**|**Deep Learning**|**CNN**|
|---|---|---|---|
|**Type**|Traditional ML algorithm|Neural network-based|Deep learning (specialized)|
|**Input Data**|Features (manually extracted)|Raw data (e.g., images, text)|Image or spatial data|
|**Data Requirements**|Small to medium datasets|Large datasets|Large labeled datasets|
|**Performance**|Effective for structured data|Better for complex, high-dimensional data|Excellent for image-based tasks|
|**Complexity**|Relatively simple|High due to multiple layers|High, tailored for images|

### When to Use Each

- **SVM**: Use when the dataset is small to medium-sized, and the focus is on structured data.
- **Deep Learning**: Use when you have large amounts of data and require learning from unstructured data like text, speech, or raw signals.
- **CNN**: Use for image or video-related tasks requiring feature extraction and classification.


# Support Vector Machine 

- الهدف انى بجيب مساقة بين ال Two Classes  و تكون هي فالمنتصف بالظبط بين نقطتين

![[Pasted image 20241203105749.png]]


# How it Works? 
- The main ideas is about choosing the best **hyperplane** that **maximizes** the margins between classes.
- **Support Vectors**
	- The closest points that identify the best **hyperplane**.
- Hyperplanes
	- Any shape can يفصل the points 

![[Pasted image 20241216105027.png]]

# Strength of SVMs
- Good generalization 
- Works well with few training instances 
- Find globally best model.
- Efficient algorithms.
- SVM Works for Classification and Regression.
- For Linearly separable binary set.

![[Pasted image 20250101095214.png]]
![[Pasted image 20250101095224.png]]