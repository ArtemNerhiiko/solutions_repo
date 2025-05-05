# Problem 3

## 1. Analyzing the possible trajectories (e.g., parabolic, hyperbolic, elliptical) of a payload released near Earth.


The trajectory of a payload released near Earth depends primarily on its velocity relative to Earth and the influence of Earth's gravity. These trajectories can generally be categorized into three conic sections: **elliptical**, **parabolic**, and **hyperbolic**.


### 1. **Elliptical Trajectory (0 < v < vₑ)**

**Description**: The payload moves in an elliptical orbit around Earth.

**Condition**: 

- Initial velocity $v$ is less than the escape velocity $vₑ$.

- $0 < v < vₑ$

**Outcome**: The payload remains bound to Earth and will continue orbiting unless acted upon by another force (e.g., atmospheric drag or propulsion).



### 2. **Parabolic Trajectory (v = vₑ)**

**Description**: The payload follows a parabolic escape trajectory.

**Condition**: 

- Initial velocity $v$ is exactly equal to Earth's escape velocity $vₑ$.

- $v = vₑ$

**Outcome**: The payload escapes Earth's gravity but with zero excess velocity at infinity.



### 3. **Hyperbolic Trajectory (v > vₑ)**

**Description**: The payload follows a hyperbolic path, escaping Earth’s gravity.

**Condition**:

- Initial velocity $v$ exceeds Earth's escape velocity $vₑ$.

- $v > vₑ$

**Outcome**: The payload escapes Earth with positive velocity at infinity, continuing into interplanetary space.



### 4. **Straight-Line (Radial) Trajectory**

**Special Case**: If the payload is released directly upward or downward, the trajectory may still be parabolic, hyperbolic, or elliptical, but without angular momentum (degenerate conic sections).


## Key Terms and Formulas

**Escape Velocity ($vₑ$)**:

$$ vₑ = \sqrt{\frac{2GM}{R}} $$

Where:

- $G$ = gravitational constant

- $M$ = mass of Earth 

- $R$ = distance from Earth’s center to the payload  

**Total Mechanical Energy ($E$)**:

$$ E = \frac{1}{2}mv^2 - \frac{GMm}{r} $$

- If $E < 0$: elliptical 

- If $E = 0$: parabolic  

- If $E > 0$: hyperbolic


## 2. Performing a numerical analysis to compute the path of the payload based on given initial conditions (position, velocity, and altitude).

```python
import numpy as np
import matplotlib.pyplot as plt

# Initial conditions
x0 = 0          # initial horizontal position (m)
y0 = 1000       # initial altitude (m)
vx0 = 200       # initial horizontal velocity (m/s)
vy0 = 0         # initial vertical velocity (m/s)

# Parameters
g = 9.81        # gravity (m/s²)
mass = 10       # mass of payload (kg)
Cd = 0.5        # drag coefficient
rho = 1.225     # air density (kg/m³)
A = 0.1         # cross-sectional area (m²)
dt = 0.01       # time step (s)
t_max = 30      # max simulation time (s)

# Initialize arrays
t = np.arange(0, t_max, dt)
x = np.zeros_like(t)
y = np.zeros_like(t)
vx = np.zeros_like(t)
vy = np.zeros_like(t)

# Set initial conditions
x[0] = x0
y[0] = y0
vx[0] = vx0
vy[0] = vy0

# Simulation loop
for i in range(1, len(t)):
    v = np.sqrt(vx[i-1]**2 + vy[i-1]**2)
    drag = 0.5 * Cd * rho * A * v**2

    # Drag components
    drag_x = drag * (vx[i-1] / v)
    drag_y = drag * (vy[i-1] / v)

    # Update velocities
    ax = -drag_x / mass
    ay = -g - drag_y / mass

    vx[i] = vx[i-1] + ax * dt
    vy[i] = vy[i-1] + ay * dt

    # Update positions
    x[i] = x[i-1] + vx[i] * dt
    y[i] = y[i-1] + vy[i] * dt

    # Stop if payload hits the ground
    if y[i] <= 0:
        x = x[:i+1]
        y = y[:i+1]
        t = t[:i+1]
        break

# Plot trajectory
plt.figure(figsize=(10,5))
plt.plot(x, y)
plt.title("Payload Trajectory")
plt.xlabel("Horizontal Distance (m)")
plt.ylabel("Altitude (m)")
plt.grid()
plt.show()
```