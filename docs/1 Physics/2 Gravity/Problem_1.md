# Problem 1

# Orbital Period and Orbital Radius


## 1. Deriving the relationship between the square of the orbital period and the cube of the orbital radius for circular orbits.

### Step 1: Centripetal Force and Gravitational Force
For a body of mass $m$ orbiting a central mass $M$, the gravitational force provides the necessary centripetal force:

$F_g = F_c$

Using Newton's law of universal gravitation:

$F_g = \frac{GMm}{r^2}$

And the centripetal force:

$F_c = \frac{m v^2}{r}$

Equating both forces:

$\frac{GMm}{r^2} = \frac{m v^2}{r}$

Cancel $m$ (assuming $m \neq 0$):

$\frac{GM}{r^2} = \frac{v^2}{r}$

Rearrange to express velocity:

$v^2 = \frac{GM}{r}$

### Step 2: Expressing Orbital Period $T$
The orbital period $T$ is given by: $T = \frac{2\pi r}{v}$.

Substituting $v$ from above: $T = \frac{2\pi r}{\sqrt{GM/r}}$.

Simplify: $T = 2\pi \sqrt{\frac{r^3}{GM}}$.

### Step 3: Squaring Both Sides
$T^2 = 4\pi^2 \frac{r^3}{GM}$.

Rearrange: $\frac{T^2}{r^3} = \frac{4\pi^2}{GM}$.

Since $\frac{4\pi^2}{GM}$ is a constant for a given central mass $M$, this shows that: $T^2 \propto r^3$.

This is Kepler's Third Law, which states that the square of the orbital period is proportional to the cube of the orbital radius for circular orbits.

## **2. Discussing the implications of this relationship for astronomy, including its role in calculating planetary masses and distances.**  

The relationship  
$T^2 \propto r^3$ 
derived from Kepler’s Third Law has profound implications for astronomy, particularly in calculating planetary masses, determining distances in space, and understanding celestial mechanics.  


### **1. Determining the Mass of Celestial Bodies**  
By modifying the equation

$T^2 = \frac{4\pi^2}{G M} r^3$

we can solve for the mass \( M \) of the central object:  

$M = \frac{4\pi^2 r^3}{G T^2}$  

This allows astronomers to measure the mass of massive celestial bodies such as:  

- **The Sun**: By observing the orbits of planets in our Solar System, we can determine the Sun's mass.  
- **Exoplanet Host Stars**: By studying an exoplanet's orbit around its star, we can estimate the mass of the star.  
- **Galaxies & Black Holes**: By applying the same principle to stars orbiting the center of galaxies, astronomers can estimate the mass of supermassive black holes.  



### **2. Measuring Planetary and Moon Distances**  
If the mass of the central body is known, the equation  

$r^3 = \frac{G M T^2}{4\pi^2}$  

allows astronomers to estimate the distance of a planet or moon from its parent body.  

- **Earth-Moon Distance**: By measuring the Moon’s orbital period around Earth, we can determine its orbital radius.  
- **Jupiter’s Moons**: By observing the orbital periods of moons like Io, Europa, and Ganymede, astronomers estimate their distances from Jupiter.  

This method has been critical in missions like Apollo and space probes navigating our Solar System.  



### **3. Comparing Exoplanetary Systems**  
By observing the transit or radial velocity of exoplanets (planets orbiting other stars), astronomers apply Kepler’s Third Law to:  

- Estimate the **orbital distances** of exoplanets from their stars.  
- Determine the **habitable zone**—the region where liquid water might exist.  
- Compare exoplanetary systems to our own Solar System.  

---

### **4. Establishing Cosmic Distance Scales**  
Kepler’s Law extends beyond planets:  

- **Binary Star Systems**: Measuring the orbital period and separation of two stars in a binary system helps determine their masses and distances.  
- **Galactic Rotation**: Kepler’s Law helps describe how stars orbit within galaxies, leading to discoveries such as **dark matter**, which explains deviations in orbital speeds.  
- **Distance to Other Solar Systems**: By using Kepler’s Law along with parallax and redshift measurements, astronomers can refine the scale of distances in space.  

## 
Kepler’s Third Law,  
$$ T^2 \propto r^3 $$  
plays a crucial role in understanding the motion of celestial bodies in our Solar System. Below are some real-world applications, including the Moon’s orbit around Earth and planetary orbits.

## **3.Analyzing real-world examples, such as the Moon's orbit around Earth or the orbits of planets in the Solar System**

### **1. The Moon’s Orbit Around Earth**
The Moon follows an approximately circular orbit around Earth, allowing us to apply Kepler’s Third Law to estimate its orbital parameters.

### **Key Data:**
- **Orbital period**: $T = 27.32$ days

- **Average orbital radius**: $r = 3.84 \times 10^5$ km

- **Mass of Earth**: $M = 5.97 \times 10^{24}$ kg

Using Kepler’s Law,  
$$ T^2 = \frac{4\pi^2 r^3}{G M} $$  
we can verify the Moon's period and refine models of its motion.

### **Applications:**
- Predicting lunar phases and eclipses.
- Calculating Earth-Moon distance changes due to tidal interactions.
- Assisting in spacecraft navigation for lunar missions.


### **2. Planetary Orbits in the Solar System**
Kepler’s Third Law helps us understand the motion of planets around the Sun.

### **Kepler’s Law Applied to the Planets**
For planets orbiting the Sun,  

$\frac{T^2}{r^3} = \text{constant}$ 

where \( T \) is measured in years and \( r \) in astronomical units (AU).

### **3. Jupiter’s Moons and Exoplanet Studies**
Kepler’s Law applies to moons orbiting planets as well as exoplanets orbiting distant stars.

### **Galilean Moons of Jupiter**
- Galileo observed that the four largest moons of Jupiter (Io, Europa, Ganymede, Callisto) follow Keplerian orbits.
- This allowed early astronomers to estimate Jupiter’s mass and confirm the heliocentric model.

### **Exoplanet Detection**
- By measuring an exoplanet’s transit period and orbital radius, scientists estimate the **mass** and **habitable zone** of exoplanetary systems.
- Example: Kepler-186f was discovered using Kepler’s Third Law, confirming it orbits within its star’s habitable zone.

## 4. Implement a computational model to simulate circular orbits and verify the relationship.

### $T^2$ vs $r^3$

![download (12)](https://github.com/user-attachments/assets/f41b11bd-62aa-4f05-9fe0-9229d5a3e207)

As expected from Kepler's Third Law, the relationship is perfectly linear, showing that the square of the orbital period is directly proportional to the cube of the orbital radius. Let me know if you'd like to try this with different parameters or units. 

### A $T^2$ vs $r^3$ plot for different planets


![download (14)](https://github.com/user-attachments/assets/b4ef40ad-1b77-454b-bdf3-83664c9d4580)




## 4.1 Using Kepler's Third Law to Find Mass of the Sun and Earth

### Formula (Newton's Version of Kepler’s Third Law):

$T^2 = (4π^2 * r^3) / (G * M)$

Solving for M (mass of the central body):

$M = (4π^2 * r³) / (G * T^2)$

Where:
- T = orbital period (in seconds)

- r = orbital radius (in meters)

- $G =$ gravitational constant = $6.674 × 10^{-11} m^3 kg^{-1} s^P{-2}$

- M = mass of the central object being orbited (Sun or Earth)



### 1. Mass of the Sun (using Earth's orbit)

- T = 1 year = 365.25 × 24 × 3600 = 31,557,600 s
- r = 1 AU = 1.496 × 10¹¹ m

Now plug into the formula:

$M = (4 * π^2 * (1.496 × 10^11)^3) / (6.674 × 10^-11 * (31,557,600)^2)$

$M ≈ 1.989 × 10^30 kg$

**Mass of the Sun ≈ 1.989 × 10³⁰ kg**


### 2. Mass of the Earth (using Moon's orbit)

- T = 27.32 days = 27.32 × 24 × 3600 = **2,360,592 s**
- r = average distance from Moon to Earth = **3.844 × 10⁸ m**

Plug into the formula:

M = (4 * π² * (3.844 × 10⁸)³) / (6.674 × 10⁻¹¹ * (2,360,592)²)

M ≈ **5.97 × 10²⁴ kg**

**Mass of the Earth ≈ 5.97 × 10²⁴ kg**







