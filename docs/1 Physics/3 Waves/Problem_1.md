# Problem 1

A circular wave on the water surface, emanating from a point source located at $(x_0, y_0)$, can be described by the Single Disturbance equation:

$$
\eta(x, y, t) = \frac{A}{\sqrt{r}} \cdot \cos(kr - \omega t + \phi)
$$

where:

- $\eta(x, y, t)$ is the displacement of the water surface at point $(x, y)$ and time $t$,

- $A$ is the amplitude of the wave,

- $k = \frac{2\pi}{\lambda}$ is the wave number, related to the wavelength $\lambda$,

- $\omega = 2\pi f$ is the angular frequency, related to the frequency $f$,

- $r = \sqrt{(x - x_0)^2 + (y - y_0)^2}$ is the distance from the source to the point $(x, y)$,

- $\phi$ is the initial phase.


## Interference Pattern from Point Sources at Square Vertices

### 1. Geometry

- Regular polygon: **Square**

- Sources: 4 point sources at vertices

### 2. Coordinates

- $S_1 = (-a/2, a/2),\quad S_2 = (a/2, a/2),\quad S_3 = (a/2, -a/2),\quad S_4 = (-a/2, -a/2)$

### 3. Wave Equation (for each source)

$$
\eta_i(x, y, t) = \frac{A}{\sqrt{r_i}} \cos(k r_i - \omega t + \phi_i)
$$

Where:

- $r_i = \sqrt{(x - x_i)^2 + (y - y_i)^2}$

### 4. Total Surface Displacement

$$
\eta_{\text{total}}(x, y, t) = \sum_{i=1}^{4} \frac{A}{\sqrt{r_i}} \cos(k r_i - \omega t + \phi_i)
$$

### 5. Interference Analysis

- Constructive: $\Delta r = n \lambda$

- Destructive: $\Delta r = (n + 0.5) \lambda$

- Pattern: Symmetrical, based on square geometry

