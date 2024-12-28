---
Lecture-Date: 
Finish?: false
Study-Date:
---
---
# What is K-Mean 

- **Idea**: Group together similar instances.
- **Detect patterns**: 
	- Croup email or search results.
	- Customer shopping patterns
	- Regions of images.
- **Useful** when don't now what you're looking for
- Clustering Results are crucially dependent on the measure of similarity (distance) between (Points) to be Clustered.


![[Recording 20241216084105.webm]]

## Advantages
1. Relatively simple to implement.
2. Scales to large data sets.
3. Guarantees Convergence.
4. Easily adapt to new examples.

## Disadvantages 
1. Choosing (k) manually 
2. Being dependent on initial values.
3. Scaling with number of dimensions


## Example 

### <span style="color:rgb(255, 0, 0)">Normalizing the Data</span>
- We must normalize the data.
- If we don't normalize the data, variables with different scaling will be weighted differently in the distance formula that is being optimized during training.