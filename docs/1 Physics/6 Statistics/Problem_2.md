# Problem 2

## Theoretical Foundation:

## Estimating π Using a Unit Circle and Random Points

You can estimate π by randomly generating points inside a square that encloses a **unit circle**, and then calculating the ratio of points that fall **inside the circle** to the total number of points in the **square**.

This method is known as a **Monte Carlo simulation**.

## Step 1: Define the Square and Circle

- The **unit circle** is centered at the origin $(0, 0)$ with radius $r = 1$.

- The **bounding square** goes from $-1$ to $1$ in both x and y, so the side length is 2.

### Areas:
- **Area of the circle**: 

$A_{\text{circle}} = \pi r^2 = \pi(1)^2 = \pi$

- **Area of the square**: 

$A_{\text{square}} = (2)^2 = 4$

## Step 2: Generate Random Points

Generate a large number $N$ of random points $(x, y)$ such that:  

$ -1 \leq x \leq 1,\quad -1 \leq y \leq 1 $

For each point, check whether it falls **inside the circle** using the inequality:  
$x^2 + y^2 \leq 1$

Let $N_{\text{in}}$ be the number of points that fall **inside the circle**.

## Step 3: Use the Ratio to Estimate π

Since the ratio of areas is approximately equal to the ratio of points:  

$\frac{A_{\text{circle}}}{A_{\text{square}}} \approx \frac{N_{\text{in}}}{N}$

Substituting the area values:  

$\frac{\pi}{4} \approx \frac{N_{\text{in}}}{N}$

Multiplying both sides by 4:

$\boxed{\pi \approx 4 \cdot \frac{N_{\text{in}}}{N}}$

## Final Formula

$\pi \approx 4 \times \frac{\text{Number of points inside the circle}}{\text{Total number of points in the square}}$

