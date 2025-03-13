# Problem 1


# Projectile Motion: A Rich Playground for Physics  

Projectile motion, while seemingly simple, offers a rich playground for exploring fundamental principles of physics. The problem is straightforward: analyze how the range of a projectile depends on its angle of projection.  

Yet, beneath this simplicity lies a complex and versatile framework. The equations governing projectile motion involve both linear and quadratic relationships, making them accessible yet deeply insightful.

# 1 Theoretical Foundation:

Projectile motion is the motion of an object thrown (projected) into the air when, after the initial force that launches the object, air resistance is negligible and the only other force that object experiences is the force of gravity. The object is called a projectile, and its path is called its trajectory. It illustrates the interplay between kinematics and Newtonian mechanics. To analyze the motion, we derive the governing equations using fundamental principles, starting with Newton’s second law and basic differential equations. 

We separate projectile motion into the two components of its motion, one along the horizontal axis and the other along the vertical.

- **Horizontal (x-direction):** Motion with constant velocity  
- **Vertical (y-direction):** Motion under constant acceleration due to gravity

  ![images](https://github.com/user-attachments/assets/c2a69a7b-25ad-42b2-8101-1c47d8114b79)


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

$a_y = -g$


Applying Newton’s second law:  

$m \cdot a_y = -mg$


$\frac{d v_y}{dt} = -g$
  
Integrating with respect to time, we obtain the velocity in the \( y \)-direction:  

$v_y = v_0 \sin\theta - g t$
 
Integrating again to get the vertical position:  

$y(t) = v_0 \sin\theta \cdot t - \frac{1}{2} g t^2$

![Angular-Projectile-Throw-Definitions](https://github.com/user-attachments/assets/68017586-32f8-4d29-a0c4-b10adc65e5a4)


### 1.2 **Euler-Lagrange Equation**
The Euler-Lagrange equation is a fundamental equation in calculus of variations and Lagrangian mechanics. It provides the necessary condition for a function to be an extremum (minimum, maximum, or saddle point) in variational problems, particularly in classical mechanics where it helps derive equations of motion.

$L = T - V$

where:
- $T$  is the kinetic energy,
- $V$ is the potential energy.

The Euler-Lagrange equation is given by:

$\frac{d}{dt} \left( \frac{\partial L}{\partial \dot{q}} \right) - \frac{\partial L}{\partial q} = 0$

where:
- $( q )$ is the generalized coordinate,
- $( \dot{q} )$ is the velocity.




# 2.1 Analysis of the Range:

### Horizontal Range and Angle of Projection

The horizontal range $R$ of a projectile is the distance covered by the projectile from the foot of the tower to the point where the projetile hits the ground. It travels horizontally before landing, and it depends on various parameters, including the angle of projection $θ$, the initial velocity $v_0$ and the gravitational acceleration $g$.
The general equation for the horizontal range of a projectile launched from the ground level is given by:

$R = \frac{v_0^2 sin(2θ)}{g}$

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

- On the Moon, where the gravitational acceleration is about $( 1.6 \, \text{m/s}^2 )$, the horizontal range would be much greater for the same initial velocity and angle compared to Earth, where $( g = 9.81 \, \text{m/s}^2 )$.

This means:
- If gravity is stronger $(larger ( g ))$, the projectile spends less time in the air, so the range will be smaller.
- If gravity is weaker $(smaller ( g ))$, the projectile stays in the air longer, and the range increases.

### Influence of Initial Velocity

The initial velocity $( v_0 )$ plays a direct role in determining the horizontal range. The range $( R )$ is proportional to the square of the initial velocity. This means:

- If the initial velocity is doubled, the horizontal range will increase by a factor of four $(since ( R \propto v_0^2 ))$.
- If the velocity is halved, the range will be reduced by a factor of four.

Increasing the initial velocity increases the horizontal range, while decreasing it reduces the range. However, this effect is independent of the angle of projection; the same range increase happens regardless of whether the angle is 30°, 45°, or 60°.







 



