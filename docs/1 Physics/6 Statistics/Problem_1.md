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


![download (21)](https://github.com/user-attachments/assets/4bf5bd57-4181-49a1-915f-04463778913f)



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


## 3 Parameter Exploration:


![download (22)](https://github.com/user-attachments/assets/0d4a0541-e9c5-481c-80b4-5d44e3b1ffbe)


```python
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Set style and seed
sns.set(style="whitegrid")
np.random.seed(0)

# Define population distributions
populations = {
    'Normal': np.random.normal(loc=50, scale=10, size=100000),
    'Exponential (Right-Skewed)': np.random.exponential(scale=10, size=100000),
    'Uniform': np.random.uniform(low=20, high=80, size=100000)
}

# Sample sizes to investigate
sample_sizes = [5, 10, 30, 50, 100]
n_iterations = 1000  # number of samples to draw

# Plot
fig, axes = plt.subplots(len(populations), len(sample_sizes), figsize=(20, 12), sharey='row')
fig.suptitle("CLT: Effect of Population Shape and Sample Size on Sampling Distribution", fontsize=18)

for row, (pop_name, pop_data) in enumerate(populations.items()):
    pop_mean = np.mean(pop_data)
    pop_std = np.std(pop_data)
    
    for col, n in enumerate(sample_sizes):
        sample_means = [
            np.mean(np.random.choice(pop_data, size=n, replace=False))
            for _ in range(n_iterations)
        ]
        
        ax = axes[row, col]
        sns.histplot(sample_means, bins=30, kde=True, ax=ax, color='skyblue', stat='density')
        ax.axvline(pop_mean, color='red', linestyle='--', label='Population Mean')
        
        ax.set_title(f"{pop_name}\nSample Size = {n}")
        if col == 0:
            ax.set_ylabel("Density")
        else:
            ax.set_ylabel("")
        if row == len(populations) - 1:
            ax.set_xlabel("Sample Mean")
        else:
            ax.set_xlabel("")
        
        if col == len(sample_sizes) - 1:
            # Show standard deviation of the sample mean
            std_sample_means = np.std(sample_means)
            ax.text(0.95, 0.9, f"Std: {std_sample_means:.2f}",
                    transform=ax.transAxes, ha='right', va='top', fontsize=10)

plt.tight_layout(rect=[0, 0, 1, 0.95])
plt.legend(loc='upper right')
plt.show()
```


## 4. Practical Applications:

## Reflection on the Importance of the Central Limit Theorem (CLT)

The **Central Limit Theorem (CLT)** is one of the most powerful and foundational concepts in statistics. It allows us to make **inferences about population parameters using sample data**, even when the population distribution is unknown or non-normal.



## 1. Estimating Population Parameters

In many fields, it's impractical or impossible to measure an entire population. Instead, we collect **random samples** and calculate statistics like the mean or proportion.

- **CLT guarantees** that the sampling distribution of these statistics is **approximately normal** for large enough sample sizes.

- This makes it possible to use **confidence intervals** and **hypothesis tests** reliably.

*Example*: Polling agencies can survey just a few thousand people to estimate the national vote share with a known margin of error.



## 2. Quality Control in Manufacturing

Manufacturers frequently use **sample testing** to monitor production quality (e.g., checking whether the mean weight of cereal boxes is within limits).

- Thanks to CLT, even if the **distribution of a single item is skewed**, the **average from a sample** follows a normal distribution.

- This enables the use of **control charts** and **statistical process monitoring**.

*Example*: If the average diameter of bolts in a sample shifts too far from the target, the production line can be stopped and recalibrated.


## 3. Predicting Outcomes in Financial Models

Finance involves uncertainty, and models rely on historical data to estimate expected returns, risks, and probabilities of various outcomes.

- CLT enables the assumption that **portfolios of many independent assets** will have **normally distributed average returns**.

- This is essential for risk measures like **Value at Risk (VaR)** and **confidence intervals** for returns.

*Example*: A financial analyst might use 30-day rolling average returns to predict next-month performance, assuming the averages follow a normal distribution.





