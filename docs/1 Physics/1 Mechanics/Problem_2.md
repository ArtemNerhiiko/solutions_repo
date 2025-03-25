# Problem 2


<span style="font-size: 1.2em; font-weight: bold;">Investigating the Dynamics of a Forced Damped Pendulum</span>


The forced damped pendulum is a captivating example of a physical system with intricate behavior resulting from the interplay of damping, restoring forces, and external driving forces. By introducing both damping and external periodic forcing, the system demonstrates a transition from simple harmonic motion to a rich spectrum of dynamics, including resonance, chaos, and quasiperiodic behavior. These phenomena serve as a foundation for understanding complex real-world systems, such as driven oscillators, climate systems, and mechanical structures under periodic stress.

# 1 Theoretical Foundation:
### Differential equation governing the motion of a forced damped pendulum:

$\frac{d^2\theta}{dt^2} + b\frac{d\theta}{dt} + \frac{g}{L}\sin\theta = A\cos(\omega t)$

The key variables are:
- $θ$: Angular displacement from the vertical (in radians).
- $L$: Length of the pendulum.
- $m$: Mass of the bob.
- $g$: Acceleration due to gravity.
- $b$: Damping coefficient.
- $F₀$: Amplitude of the external forcing.
- $ω$: Angular frequency of the external force.

A forced damped pendulum consists of:
- A mass (bob) attached to a pivot point by a massless rod or string.
- A damping force (e.g., air resistance) proportional to the angular velocity.
- An external periodic force driving the pendulum.

## Deriving the approximate solutions for small-angle oscillations.

### 1. Equation of Motion for a Simple Pendulum

A simple pendulum consists of a mass $m$ attached to a string of length $l$, oscillating under the influence of gravity. The restoring force is given by:

$$ F = -mg \sin\theta $$

Using Newton's second law, $F = ma = m l \frac{d^2\theta}{dt^2}$, we get the equation of motion:

$$
m l \frac{d^2\theta}{dt^2} = -mg \sin\theta
$$

Dividing by $ml$, we obtain:

$$
\frac{d^2\theta}{dt^2} + \frac{g}{l} \sin\theta = 0
$$

### 2. Small-Angle Approximation
For small angles ($\theta \approx 0$), we use the approximation:

$$
\sin\theta \approx \theta
$$

Thus, the equation simplifies to:

$$
\frac{d^2\theta}{dt^2} + \frac{g}{l} \theta = 0
$$

This is a standard **simple harmonic motion (SHM) equation** of the form:

$$
\frac{d^2\theta}{dt^2} + \omega^2 \theta = 0
$$

where $$\omega = \sqrt{\frac{g}{l}}$$ is the angular frequency.

### 3. General Solution

The general solution of a simple harmonic oscillator equation is:

$$
\theta(t) = \theta_0 \cos(\omega t + \phi)
$$

where:
- $$\theta_0$$ is the initial amplitude,
- $$\phi$$ is the phase constant (determined by initial conditions),
- $$\omega = \sqrt{\frac{g}{l}}$$ is the angular frequency.

### 4. Period of Oscillation
The period of oscillation is given by:

$$
T = \frac{2\pi}{\omega} = 2\pi \sqrt{\frac{l}{g}}
$$

This is the approximate period for small-angle oscillations.
