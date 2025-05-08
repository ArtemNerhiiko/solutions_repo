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


![download (11)](https://github.com/user-attachments/assets/742e0204-c92f-497a-ac06-90a2fe618627)


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


## 3. Discussing how these trajectories relate to orbital insertion, reentry, or escape scenarios.


### Interpreting Payload Trajectories in Orbital Contexts

The numerical simulation we performed models a **suborbital ballistic trajectory** — useful for understanding short-range missiles, sounding rockets, or atmospheric reentry vehicles. Here's how it relates to key orbital scenarios:



## 1. Orbital Insertion


**Minimum speed required** (in low Earth orbit): ~7.8 km/s

In our example, the horizontal velocity is only 200 m/s, far too low for orbit.

**Orbital insertion** requires engines to fire **horizontally**, not vertically, and usually at high altitude (above atmosphere).

In simulation, if you gradually increase `vx0`, you approach a more flattened trajectory, but true orbital insertion needs modeling Earth's curvature and using Newton's law of universal gravitation, not just constant gravity.

**To simulate orbital insertion**:

- Switch to polar coordinates $(r, \theta)$

- Use variable gravity: $F = \frac{GMm}{r^2}$

- Account for Earth's rotation



## 2. Reentry

**Context**: A payload returning from orbit or a suborbital trajectory enters Earth's atmosphere.

- **Our simulation** resembles **controlled reentry** of capsules or spacecraft.

- High-altitude, steep-angle trajectories are common for reentry vehicles.

- Drag becomes dominant in upper atmosphere — it slows the vehicle and heats it up (thermal analysis required).

**Key factors in reentry**:

- Entry angle (too steep = burn up, too shallow = skip off)

- Velocity (orbital reentry ~7.8 km/s; ballistic reentry ~1–3 km/s)

- Heat shielding and structural stress

The drag force reduces vertical and horizontal speed, mimicking reentry deceleration.



## 3. Escape Trajectory

Reaching escape velocity to leave Earth's gravitational field.

**Escape velocity from Earth**: ~11.2 km/s (ignoring atmosphere)

Payload is far below this; it always falls back.

For a true escape:

- `vx0` (and/or `vy0`) must be very high.

- Gravity is not constant — use $F = \frac{GMm}{r^2}$

- Air resistance greatly hinders escape at lower altitudes — so launches are vertical to get above most of the atmosphere first.

## 4. Developing a computational tool to simulate and visualize the motion of the payload under Earth's gravity, accounting for initial velocities and directions.


```python
import numpy as np
import matplotlib.pyplot as plt

# Constants
G = 6.67430e-11  # gravitational constant, m^3/kg/s^2
M_earth = 5.972e24  # mass of Earth, kg
R_earth = 6.371e6  # radius of Earth, m

# Initial parameters
altitude = 800e3  # 800 km above the surface
initial_distance = R_earth + altitude  # from the center of Earth
initial_position = np.array([initial_distance, 0])  # starting on the right side
time_step = 1  # seconds
total_time = 10000  # simulate for ~2.8 hours
num_steps = int(total_time / time_step)

# Initial velocities (km/s converted to m/s)
initial_speeds = np.arange(5e3, 13.5e3, 0.5e3)  # from 5 km/s to 13 km/s

# Storage for trajectories
trajectories = []

for v0 in initial_speeds:
    position = initial_position.copy()
    velocity = np.array([0, v0])  # launch perpendicular to the radius vector
    traj = [position.copy()]
    
    for _ in range(num_steps):
        r = np.linalg.norm(position)
        accel = -G * M_earth * position / r**3
        velocity += accel * time_step
        position += velocity * time_step
        if np.linalg.norm(position) < R_earth:
            break  # object has hit the Earth
        traj.append(position.copy())
    
    trajectories.append(np.array(traj))

# Plotting
fig, ax = plt.subplots(figsize=(8, 8))
earth = plt.Circle((0, 0), R_earth, color='blue', label='Earth')
ax.add_artist(earth)

colors = plt.cm.viridis(np.linspace(0, 1, len(initial_speeds)))

for traj, v0, color in zip(trajectories, initial_speeds, colors):
    ax.plot(traj[:, 0], traj[:, 1], label=f'{v0/1e3:.1f} km/s', color=color)

ax.set_xlim(-2e7, 2e7)
ax.set_ylim(-2e7, 2e7)
ax.set_aspect('equal')
ax.set_title("Trajectories of Payload with Varying Initial Speeds")
ax.set_xlabel("X position (m)")
ax.set_ylabel("Y position (m)")
ax.legend()
plt.grid(True)
plt.show()
```
