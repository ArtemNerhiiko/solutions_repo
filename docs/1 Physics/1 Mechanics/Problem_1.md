# Problem 1


# Projectile Motion: A Rich Playground for Physics  

Projectile motion, while seemingly simple, offers a rich playground for exploring fundamental principles of physics. The problem is straightforward: analyze how the range of a projectile depends on its angle of projection.  

Yet, beneath this simplicity lies a complex and versatile framework. The equations governing projectile motion involve both linear and quadratic relationships, making them accessible yet deeply insightful.

# 1 Theoretical Foundation:

Projectile motion is the motion of an object thrown (projected) into the air when, after the initial force that launches the object, air resistance is negligible and the only other force that object experiences is the force of gravity. The object is called a projectile, and its path is called its trajectory. It illustrates the interplay between kinematics and Newtonian mechanics. To analyze the motion, we derive the governing equations using fundamental principles, starting with Newton’s second law and basic differential equations. 

We separate projectile motion into the two components of its motion, one along the horizontal axis and the other along the vertical.

- **Horizontal (x-direction):** Motion with constant velocity  
- **Vertical (y-direction):** Motion under constant acceleration due to gravity

  
![maxresdefault](https://github.com/user-attachments/assets/e2641361-67ee-446e-b529-cba56f89e1c9)


The key parameters:

- **$( v_0 )$ = Initial velocity**
- **$( g )$ = Acceleration due to gravity**
- **$( x(t), y(t) )$ = Position coordinates at time $( t )$**
- **$( \theta )$ = Angle of projection**
 
# 1.1 Newton’s Second Law and Differential Equations  

Newton’s second law states: 
$F = ma$

where:
- $( F )$ is the force acting on a mass $( m )$,
- $( a )$ is the acceleration, given by $( \frac{d^2 x}{dt^2} )$.

Since there are no forces acting in the horizontal direction (assuming no air resistance), and gravity acts downward in the vertical direction, we can write the equations of motion separately for each axis.

### General Equations of Motion

- **Horizontal position:**  

  $x = v_0 \cos\theta \cdot t$

- **Vertical position:**  

  $y = v_0 \sin\theta \cdot t - \frac{1}{2} g t^2$

- **Velocity components:**  
 
  $v_x = v_0 \cos\theta, \quad v_y = v_0 \sin\theta - g t$

### Horizontal Motion:

Since there is no horizontal force, acceleration in the \( x \)-direction is zero:  

$a_x = 0$


The velocity in the \( x \)-direction remains constant:  

$v_x = v_0 \cos\theta$
  
Integrating this, we get the horizontal position as a function of time:  

$x(t) = v_0 \cos\theta \cdot t$


### Vertical Motion  
The only force in the vertical direction is gravity, which gives an acceleration:  

**$a_y = -g$**


Applying Newton’s second law:  

**$m \cdot a_y = -mg$**


**$\frac{d v_y}{dt} = -g$**
  
Integrating with respect to time, we obtain the velocity in the \( y \)-direction:  

**$v_y = v_0 \sin\theta - g t$**
 
Integrating again to get the vertical position:  

**$y(t) = v_0 \sin\theta \cdot t - \frac{1}{2} g t^2$**

![Angular-Projectile-Throw-Definitions](https://github.com/user-attachments/assets/68017586-32f8-4d29-a0c4-b10adc65e5a4)


### 1.2 **Euler-Lagrange Equation**
The Euler-Lagrange equation is a fundamental equation in calculus of variations and Lagrangian mechanics. It provides the necessary condition for a function to be an extremum (minimum, maximum, or saddle point) in variational problems, particularly in classical mechanics where it helps derive equations of motion.

**$L = T - V$**

where:
- **$T$** is the kinetic energy,
- **$V$** is the potential energy,

The Euler-Lagrange equation is given by:

**$\frac{d}{dt} \left( \frac{\partial L}{\partial \dot{q}} \right) - \frac{\partial L}{\partial q} = 0$**

where:
- **$( q )$** is the generalized coordinate,
- **$( \dot{q} )$** is the velocity,
- **$(\frac{\partial L}{\partial q})$** is the generalized force term.




# 2.1 Analysis of the Range:

### Horizontal Range and Angle of Projection

The horizontal range $R$ of a projectile is the distance covered by the projectile from the foot of the tower to the point where the projetile hits the ground. It travels horizontally before landing, and it depends on various parameters, including the angle of projection **$θ$**, the initial velocity $v_0$ and the gravitational acceleration **$g$**.
The general equation for the horizontal range of a projectile launched from the ground level is given by:

**$R = \frac{v_0^2 sin(2θ)}{g}$**

Where:

- $( R )$ is the horizontal range
- $( \theta )$ is the angle of projection
- $( v_0 )$ is the initial velocity
- $( g )$ is the gravitational acceleration (usually $( 9.81 \, \text{m/s}^2 )$ on Earth)

### Dependence of Range on the Angle of Projection

From the equation above, the range depends on the **sine of twice the angle** $( 2\theta )$. Let's break this down:

1. **At $( \theta = 0^\circ )$ (horizontal launch)**:  
   The sine term becomes zero, meaning the range $( R )$ is also zero. The projectile doesn't gain any vertical height, so it lands immediately after being launched.
   
2. **At $( \theta = 45^\circ )$**:  
   This is the optimal launch angle for the maximum range. Since $( \sin(90^\circ) = 1 )$, the range is maximized when the angle is $( 45^\circ )$. For angles less than or greater than $( 45^\circ )$, the sine of $( 2\theta )$ decreases, reducing the horizontal range.

3. **For angles larger than 45° (up to 90°)**:  
   The range starts to decrease as the angle increases. At $( \theta = 90^\circ )$ (vertical launch), the sine term becomes zero again, meaning there’s no horizontal motion, and the range is zero.

**The horizontal range is maximized at $( 45^\circ )$**, and any deviation from this angle leads to a reduction in range.

### Influence of Gravitational Acceleration

The gravitational acceleration $( g )$ is a key factor in determining the horizontal range, as it is inversely proportional to the range. If $( g )$ increases, the range decreases, and vice versa. For example:

- On the Moon, where the gravitational acceleration is about **$( 1.6 \, \text{m/s}^2 )$**, the horizontal range would be much greater for the same initial velocity and angle compared to Earth, where **$( g = 9.81 \, \text{m/s}^2 )$**.

This means:
- If gravity is stronger **$(larger ( g ))$**, the projectile spends less time in the air, so the range will be smaller.
- If gravity is weaker **$(smaller ( g ))$**, the projectile stays in the air longer, and the range increases.

### Influence of Initial Velocity

The initial velocity **$( v_0 )$** plays a direct role in determining the horizontal range. The range **$( R )$** is proportional to the square of the initial velocity. This means:

- If the initial velocity is doubled, the horizontal range will increase by a factor of four **$(since ( R \propto v_0^2 ))$**.
- If the velocity is halved, the range will be reduced by a factor of four.

Increasing the initial velocity increases the horizontal range, while decreasing it reduces the range. However, this effect is independent of the angle of projection; the same range increase happens regardless of whether the angle is 30°, 45°, or 60°.

# 3.1 Practical Applications:

### Projectile Motion on Uneven Terrain

Calculating projectile motion on uneven terrain may be useful in such situations:

- Sports science, such as golf or ski jumping,
- Military ballistics for targeting in hilly or mountainous regions.

The adaptation is pretty clear: the landing position of a projectile must be adjusted for variations in elevation. This can be done by introducing a function 
$h(x)$ that describes the terrain height and solving for the intersection of the projectile's path with the terrain function.

### Effect of Air Resistance

In real-world projectile motion, air resistance (also called drag) significantly alters the trajectory of a projectile compared to ideal motion in a vacuum. Compared to ideal projectile motion, air resistance causes the following changes:

1. **Reduced Maximum Height:**

- The projectile reaches a lower peak height.
- The vertical velocity decreases faster due to opposing drag forces.

2. **Non-Symmetric Trajectory:**

- With air resistance, the descent is steeper than the ascent because drag continuously removes energy from the projectile.
- Without air resistance, the projectile’s path is a perfect parabola.

3. **Shorter Range (Horizontal Distance):**

- The horizontal motion is significantly slowed down.

So, the proper calculations and taking into account all factors is important in such applications:

- Aerodynamics in ballistics and sports
- Spacecraft re-entry, where atmospheric drag plays a critical role in slowing down the vehicle.


![projectiles](https://github.com/user-attachments/assets/a1488ea2-8ab6-418a-b535-5ddab0152bcc)

**Adaptation:** 

Air resistance introduces a velocity-dependent drag force, often modeled as $F_d = -kv$ (linear resistance) or $F_d = -kv^2$ (quadratic resistance). These forces cause the projectile to deviate from the ideal parabolic trajectory, leading to a more realistic path that can be computed numerically.

### Coriolis Effect on Large-Scale Motion

This effect is caused by Earth's rotation, slightly deflects long-range projectiles, requiring correction in targeting calculations. Objects moving long distances across the surface of the Earth experience an apparent deflection because they retain the rotational motion of their point of origin. 

**Applications:**

- Weather prediction models
- Ballistic missile trajectory adjustments.

# 4.1 Implementation:

Lets develope a Python simulation of projectile motion, incorporating air resistance, and visualize how the range varies with the launch angle for different initial conditions. 
This code will:

1. **Simulate Projectile Motion:**

- Solves equations of motion using Euler’s method
- Includes quadratic air resistance if enabled

2. **Range vs. Launch Angle Plot:**

- Displays how air resistance reduces range.

3. **Trajectory Visualization:**

- Plots the projectile path for different angles.


![download (8)](https://github.com/user-attachments/assets/1428fc2d-5fcd-440a-9265-1dbce1d804fc)


```python
import numpy as np
import matplotlib.pyplot as plt

# Constants
Cd = 0.47  # Drag coefficient (sphere)
rho = 1.225  # Air density (kg/m^3)
d = 0.1  # Diameter of projectile (m)
A = np.pi * (d / 2) ** 2  # Cross-sectional area (m^2)
m = 0.145  # Mass of projectile (kg), e.g., a baseball
g = 9.81  # Gravity (m/s^2)
v0 = 30  # Initial velocity (m/s)
angles = [30, 45, 60]  # Launch angles in degrees
dt = 0.01  # Time step

# Function to compute trajectory WITH air resistance
def compute_trajectory_with_drag(theta):
    theta_rad = np.radians(theta)
    vx, vy = v0 * np.cos(theta_rad), v0 * np.sin(theta_rad)
    
    x, y = [0], [0]  # Initial positions
    while y[-1] >= 0:
        v = np.sqrt(vx**2 + vy**2)  # Speed
        Fd = 0.5 * Cd * rho * A * v**2  # Drag force
        ax = - (Fd / m) * (vx / v)  # Acceleration in x
        ay = -g - (Fd / m) * (vy / v)  # Acceleration in y

        # Update velocities
        vx += ax * dt
        vy += ay * dt

        # Update positions
        x.append(x[-1] + vx * dt)
        y.append(y[-1] + vy * dt)

    return x, y

# Function to compute trajectory WITHOUT air resistance
def compute_trajectory_no_drag(theta):
    theta_rad = np.radians(theta)
    t_flight = (2 * v0 * np.sin(theta_rad)) / g  # Total time of flight
    t = np.arange(0, t_flight, dt)

    x = v0 * np.cos(theta_rad) * t
    y = v0 * np.sin(theta_rad) * t - 0.5 * g * t**2

    return x, y

# Plot both cases
plt.figure(figsize=(10, 5))

for theta in angles:
    x_drag, y_drag = compute_trajectory_with_drag(theta)
    x_no_drag, y_no_drag = compute_trajectory_no_drag(theta)

    plt.plot(x_drag, y_drag, label=f"With Drag {theta}°", linestyle="dashed")
    plt.plot(x_no_drag, y_no_drag, label=f"No Drag {theta}°", linestyle="solid")

plt.xlabel("Horizontal Distance (m)")
plt.ylabel("Vertical Distance (m)")
plt.title("Projectile Motion With and Without Air Resistance")
plt.legend()
plt.grid()
plt.show()
```



