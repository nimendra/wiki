## KeyPoint: Randomly select 30 out of 30

Resampling is a statistical technique used to estimate the variability and accuracy of sample statistics by repeatedly drawing new samples from the original dataset. 

## Example: Estimating Average Height

Imagine you have a class of 30 students and you want to estimate the average height of all students in the school. Here's how you could use resampling:

1. Measure the heights of all 30 students in your class. This is your original sample.

2. To resample:
   - Randomly select 30 students from your original sample, with replacement (meaning a student can be selected more than once).
   - Calculate the average height of this new sample.
   - Record this average.

3. Repeat step 2 many times (e.g., 1000 times).

4. Analyze the distribution of these 1000 averages:
   - The mean of these averages provides an estimate of the true average height.
   - The spread of these averages (e.g., standard deviation) gives you an idea of the uncertainty in your estimate.  
   σ = √[ Σ(x - μ)² / N ]

## Benefits of Resampling

1. **Improved Accuracy**: By creating multiple samples, you get a more robust estimate of the average height.

2. **Uncertainty Estimation**: The variation in the resampled averages helps quantify the uncertainty in your estimate.

3. **No Assumptions**: Resampling doesn't require assumptions about the underlying distribution of heights.

This example demonstrates bootstrapping, which is one type of resampling technique. Other resampling methods include cross-validation and permutation tests, each with specific applications in statistics and machine learning[1].

Citations:
[1] https://timespro.com/blog/what-is-resampling-in-data-science-learning-its-goals-and-types
[2] https://www.shiksha.com/online-courses/articles/introduction-to-sampling-and-resampling/
[3] https://www.kdnuggets.com/2023/02/role-resampling-techniques-data-science.html
[4] https://www.statisticssolutions.com/dissertation-resources/sample-size-calculation-and-sample-size-justification/resampling/
[5] https://machinelearningmastery.com/statistical-sampling-and-resampling/
[6] https://www.geeksforgeeks.org/introduction-to-resampling-methods/
[7] https://en.wikipedia.org/wiki/Resampling_%28statistics%29
[8] https://bookdown.org/max/FES/resampling.html