# Problem 1

## Simulating Sampling Distributions:

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


![download (20)](https://github.com/user-attachments/assets/1581d6e9-bc43-4428-ba31-b958ac109b6a)




