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
Since there are no forces acting in the horizontal direction (assuming no air resistance), and gravity acts downward in the vertical direction, we can write the equations of motion separately for each axis.

### 1.2 General Equations of Motion

- **Horizontal position:**  

  $x = v_0 \cos\theta \cdot t$

- **Vertical position:**  

  $y = v_0 \sin\theta \cdot t - \frac{1}{2} g t^2$

- **Velocity components:**  
 
  $v_x = v_0 \cos\theta, \quad v_y = v_0 \sin\theta - g t$

### 1.3 Horizontal Motion:

Since there is no horizontal force, acceleration in the \( x \)-direction is zero:  

**$a_x = 0$**


The velocity in the \( x \)-direction remains constant:  

$v_x = v_0 \cos\theta$
  
Integrating this, we get the horizontal position as a function of time:  

$x(t) = v_0 \cos\theta \cdot t$


### 1.4 Vertical Motion  
The only force in the vertical direction is gravity, which gives an acceleration:  

$a_y = -g$


Applying Newton’s second law:  

$m \cdot a_y = -mg$


$\frac{d v_y}{dt} = -g$
  
Integrating with respect to time, we obtain the velocity in the \( y \)-direction:  

$v_y = v_0 \sin\theta - g t$
 
Integrating again to get the vertical position:  

$y(t) = v_0 \sin\theta \cdot t - \frac{1}{2} g t^2$
 



