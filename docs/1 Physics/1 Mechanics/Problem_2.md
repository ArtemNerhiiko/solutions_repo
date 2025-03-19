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