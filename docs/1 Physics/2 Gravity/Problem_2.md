# Problem 2

# Escape Velocities and Cosmic Velocities

## 1. Defining the first, second, and third cosmic velocities, explaining their physical meaning.


### 1. First Cosmic Velocity (Orbital Velocity)

**Definition:**  
The minimum velocity required for an object to enter a stable circular orbit around a celestial body, just above its surface.

**Formula:**  
$v_1 = \sqrt{\frac{GM}{R}}$

- $G$ is the gravitational constant.

- $M$ is the mass of the celestial body.

- $R$ is the radius of the celestial body.

**Physical Meaning:**  
This is the speed needed to counteract gravity with centrifugal force, enabling continuous free fall around the body—i.e., low Earth orbit.

**Example (Earth):**  
Approximately **7.9 km/s**



### 2. Second Cosmic Velocity (Escape Velocity)

**Definition:**  
The minimum speed needed to break free from the gravitational pull of a celestial body without further propulsion.

**Formula:**  
$v_2 = \sqrt{\frac{2GM}{R}}$

**Physical Meaning:**  
At this velocity, an object will escape into space without falling back, moving away indefinitely unless acted upon by other forces.

**Example (Earth):**  
Approximately **11.2 km/s**



### 3. Third Cosmic Velocity (Solar Escape Velocity from Earth Orbit)

**Definition:**  
The speed required to escape the gravitational influence of the **Sun** when starting from **Earth’s orbit**.

**Formula (approximate):**  
$v_3 = \sqrt{\frac{2GM_{\text{Sun}}}{R_{\text{orbit}}}} - v_{\text{Earth orbit}}$

Where:
- $R_{\text{orbit}}$ is the Earth's orbital radius around the Sun.
- $v_{\text{Earth orbit}} \approx 29.8 \text{ km/s}$

**Physical Meaning:**  
This velocity allows a spacecraft to leave the Solar System, overcoming the Sun’s gravitational pull.

**Example (from Earth orbit):**  
Approximately **16.7 km/s** relative to Earth.

These are idealized values and do not consider atmosphere, terrain, or other practical factors in spaceflight.


## 2. Analyzing the mathematical derivations and parameters affecting these velocities.


### 1. First Cosmic Velocity

### Derivation:

The first cosmic velocity is derived by equating **gravitational force** to **centripetal force** for circular motion:

$\frac{GMm}{R^2} = \frac{mv^2}{R}$

Solving for $v$:

$v_1 = \sqrt{\frac{GM}{R}}$

### Parameters:

- $G$: Gravitational constant ($6.674 \times 10^{-11} \, \text{Nm}^2/\text{kg}^2$) – universal and constant.

- $M$: Mass of the planet – more massive planets require higher orbital velocity.

- $R$: Radius from the center of the planet – a lower orbit (smaller $R$) means a higher velocity.



### 2. Second Cosmic Velocity

### Derivation:

Derived using **energy conservation** — the sum of kinetic and potential energy at the surface must be zero at infinity:

$\frac{1}{2}mv^2 - \frac{GMm}{R} = 0$

Solving for $v$:

$v_2 = \sqrt{\frac{2GM}{R}}$

### Parameters:

- Same as the first velocity ($G$, $M$, and $R$).

- Because of the factor of 2, $v_2 = \sqrt{2} \cdot v_1 \approx 1.41 \cdot v_1$



### 3. Third Cosmic Velocity

### Derivation:

To escape the Sun's gravity starting from Earth's orbit, we use energy conservation in the **heliocentric frame**:

$\frac{1}{2}mv^2 - \frac{GM_{\text{Sun}}m}{R_{\text{orbit}}} = 0$

Solving:

$v = \sqrt{\frac{2GM_{\text{Sun}}}{R_{\text{orbit}}}}$

However, Earth is already moving around the Sun with orbital speed $v_{\text{Earth orbit}}$, so the additional speed required is:

$v_3 = \sqrt{\frac{2GM_{\text{Sun}}}{R_{\text{orbit}}}} - v_{\text{Earth orbit}}$

### Parameters:

- $M_{\text{Sun}}$: Mass of the Sun.

- $R_{\text{orbit}}$: Earth's orbital radius around the Sun ($\approx 1.496 \times 10^{11} \, \text{m}$).

- $v_{\text{Earth orbit}}$: Orbital speed of Earth around the Sun ($\approx 29.8 \, \text{km/s}$).


Cosmic velocities increase with the mass of the central body and decrease with distance from its center. They are foundational to space mission design and orbital mechanics.


## 3. Calculating and visualize these velocities for different celestial bodies like Earth, Mars adn Jupyter.


![download (9)](https://github.com/user-attachments/assets/b03e7d19-4b72-4ae8-b716-a58e5cda8f27)


