# Problem 1

## 1. Simulating Sampling Distributions:



![450475176-1581d6e9-bc43-4428-ba31-b958ac109b6a](https://github.com/user-attachments/assets/38c9d246-f087-4dcf-8887-4220149af904)




```python
# Re-import required libraries due to session reset
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Set seed for reproducibility
np.random.seed(42)

# Population size
population_size = 100000

# Generate population datasets
uniform_population = np.random.uniform(low=0, high=100, size=population_size)
exponential_population = np.random.exponential(scale=10, size=population_size)
binomial_population = np.random.binomial(n=10, p=0.5, size=population_size)

# Plot the population distributions
plt.figure(figsize=(18, 5))

# Uniform Distribution
plt.subplot(1, 3, 1)
sns.histplot(uniform_population, bins=50, kde=True, color='skyblue')
plt.title("Uniform Distribution (Population)")
plt.xlabel("Value")
plt.ylabel("Frequency")

# Exponential Distribution
plt.subplot(1, 3, 2)
sns.histplot(exponential_population, bins=50, kde=True, color='orange')
plt.title("Exponential Distribution (Population)")
plt.xlabel("Value")
plt.ylabel("Frequency")

# Binomial Distribution
plt.subplot(1, 3, 3)
sns.histplot(binomial_population, bins=30, kde=False, color='green')
plt.title("Binomial Distribution (Population)")
plt.xlabel("Value")
plt.ylabel("Frequency")

plt.tight_layout()
plt.show()
```


## 2. Sampling and Visualization:


![450475176-1581d6e9-bc43-4428-ba31-b958ac109b6a](https://github.com/user-attachments/assets/e1075f22-4beb-4a50-8f7f-d9c53601691c)


```python
import numpy as np
import matplotlib.pyplot as plt

# Set seed for reproducibility
np.random.seed(42)

# Create a non-normal population (e.g., exponential distribution)
population = np.random.exponential(scale=2.0, size=100000)

# Sample sizes to investigate
sample_sizes = [5, 10, 30, 50]
n_iterations = 1000  # number of samples to draw for each size

# Plot setup
fig, axes = plt.subplots(2, 2, figsize=(12, 10))
axes = axes.flatten()

for idx, n in enumerate(sample_sizes):
    sample_means = []
    
    for _ in range(n_iterations):
        sample = np.random.choice(population, size=n, replace=False)
        sample_means.append(np.mean(sample))
    
    # Plot histogram of sample means
    axes[idx].hist(sample_means, bins=30, color='skyblue', edgecolor='black', density=True)
    axes[idx].set_title(f"Sample Size = {n}")
    axes[idx].set_xlabel("Sample Mean")
    axes[idx].set_ylabel("Frequency")

plt.suptitle("Sampling Distributions of Sample Means", fontsize=16)
plt.tight_layout(rect=[0, 0, 1, 0.96])
plt.show()
```






