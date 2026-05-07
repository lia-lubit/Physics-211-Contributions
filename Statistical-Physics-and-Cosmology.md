### Statisical Mechanics and Cosmology 
**Lia Lubit**

Modeling the universe, with its many different types of interacting particles, requires that cosmologists use equations from statistical mechanics. 
In these notes, I link cosmology and statistical mechanics, focusing specifically on the Boltzmann equation and the physics of recombination. 
Recombination occured approximately 378,000 years after the birth of the universe, and saw protons and electrons first join together into neutral atoms. 
Following recombination, more complex atoms were formed. The equations that govern this era come directly from the Boltzmann equation, as we shall see below. 

### Part 1: The Distribution Function

The distribution function $f(t, \vec{x}, \vec{p})$ describes the number of particles that exist in some small piece of phase space, stating that

$$\Delta N = \frac{g}{(2\pi)^3} f(t, \vec{x}, \vec{p}) (\Delta \vec{x})^3 (\Delta \vec{p})^3$$

By computing weighted integrals over the distribution function, we can find expressions for the number density, energy density, and pressure.

Number density: $n = \frac{g}{(2\pi)^3} \int f d^3p$

Energy density: $\rho = \frac{g}{(2\pi)^3} \int E f d^3 p$

Pressure: $P = \frac{g}{(2\pi)^3} \int \frac{p^2}{3E} f d^3 p$

In thermal equilibrium, the distribution function is 

$$f = \left( e^{\frac{E-\mu}{T}} \pm 1 \right)^{-1}$$

Here, E is the relativistic energy, $\mu$ is the chemical potential, and T is the temperature. 
For bosons, we use the minus sign, and for fermions, the plus sign. 

At very low temperatures, the distribution is approximately 

$$f = e^{-\frac{E-\mu}{T}}$$

### Part 2: The Boltzmann Equation in General Relativity
 
Under GR, the Boltzmann equation is 

$$\frac{df}{d\lambda} = C(f)$$

Here, $\lambda$ is an affine parameter and C, the 'collision term,' details the particles' interactions.

In phase space coordinates, with position x and momentum P, we can expand the Boltzmann equation to get

$$\frac{df}{d\lambda} = P^0 \left[ \frac{\partial f}{\partial t} + \frac{\partial f}{\partial x^i} \frac{P^i}{P^0} + \frac{\partial f}{\partial E} \frac{1}{P^0} \frac{dE}{d\lambda} + \frac{\partial f}{\partial \hat{p}^i} \frac{1}{P^0} \frac{d\hat{p}^i}{d\lambda} \right]$$

By taking the moments of the Boltzmann equation, we can get conservation equations for mass and momentum, among other quantities. 

$$\frac{\partial n}{\partial t} + \nabla_x \cdot (n \vec{V}) = 0$$

$$\frac{\partial \vec{V}}{\partial t} + (\vec{V} \cdot \nabla)\vec{V} = -\frac{\nabla_j P_{ij}}{\rho} + \frac{\vec{F}}{m}$$

### Part 3: The Boltzmann Equation in a Smooth Universe

The Boltzmann equation and its moments are extremely useful for cosmology. In order to use it, we must first choose a metric. A classic choice is the FLRW metric:

$$ds^2 = -dt^2 + a^2(t) \left[ \frac{dr^2}{1 - kr^2} + r^2(d\theta^2 + \sin^2\theta d\phi^2) \right]$$

Above $a(t)$ is the scale factor describing the expansion of the universe, $k$ is the curvature parameter ($k=1$ for a closed universe, $k=0$ for flat, and $k=-1$ for open), and $d\Omega^2$ is the metric on a 2-sphere ($d\theta^2 + \sin^2\theta d\phi^2$).

Under this metric, photons obey $P^0 = E$ and $P^i = p\hat{p}^i a^{-1}$, where $E = p$.
The geodesic is then 

$$\frac{dE}{d\lambda} = -\Gamma^0_{\alpha\beta} P^\alpha P^\beta$$

While particles in a smooth universe are in thermal equilibrium with a thermal bath, the collision term C is zero. 

Therefore, the Boltzmann equation reduces to

$$\frac{df}{d\lambda} = P^0 \left[ \frac{\partial f}{\partial t} + \frac{\partial f}{\partial E} \frac{1}{E} \frac{dE}{d\lambda} \right] = 0$$

or 

$$\frac{1}{T} \frac{dT}{dt} = -\frac{1}{a} \frac{da}{dt}$$

The solution to this equation is $T \propto 1/a$.

The 0th moment of the Boltzmann equation is 

$$\frac{1}{a^3} \frac{d(na^3)}{dt} = 0 \implies n \propto \frac{1}{a^3}$$

### Part 3: Particle Reactions

We can use the above equation to learn about particle number densities in chemical reactions. The most common chemical reactions in the early universe take the form $1+2 \leftrightarrow 3+4$ reaction:

$$e^- + p^+ \rightleftharpoons e^- + p^+$$

$$e^- + \gamma \rightleftharpoons e^- + \gamma$$

$$e^- + p^+ \rightleftharpoons H + \gamma$$

For these types of reactions, we can rewrite the smooth-universe Boltzmann equation as

$$\frac{1}{a^3} \frac{d(n_1 a^3)}{dt} = -\alpha n_1 n_2 + \beta n_3 n_4$$

where $\alpha = \langle \sigma v \rangle$ is the thermally averaged cross-section coming from the collision term. 

In equilibrium

$$\beta = \alpha \left( \frac{n_1 n_2}{n_3 n_4} \right)_{\text{eq}}$$

and so

$$\frac{1}{a^3} \frac{d(n_1 a^3)}{dt} = -\langle \sigma v \rangle \left( n_1 n_2 - n_3 n_4 \left( \frac{n_1 n_2}{n_3 n_4} \right)_{\text{eq}} \right)$$

or 

$$\frac{1}{a^3} \frac{d(n_1 a^3)}{dt} = -\langle \sigma v \rangle \left( n_1 n_2 - n_3 n_4 \left[ \frac{n_1 n_2}{n_3 n_4} \right]_{eq} \right)$$

Above, $\Gamma_1 = n_2 \langle\sigma v\rangle$ is the interaction rate and $H$ is the expansion rate. This equation has three regimes:

1. When $\Gamma_1$ is much larger than $H$, then many interactions happen in the time it takes the universe to increase in size, 
and so it is easy to maintain equilibrium. 

2. When $\Gamma_1$ is less than $H$, the interactions are too slow to keep the system in equilibrium. Cosmologists call this 'decoupling.' After decopuling, the particle species evolves on its own, separate from the rest of the particles.

3. When $\Gamma_1$ is much less than $H$, our equation becomes

$$\frac{d(n_1 a^3)}{dx} \approx 0 \implies n_1 \propto 1/a^3$$

This equations describes the regular volume dilution that occurs in an expanding universe.
From this point on, though the volume of the universe increases, the number of particles per co-moving volume remains the same. As such, the particle density starts decreasing with the volume. Cosmologists call this 'freeze out', and consider it a possible source of dark matter. 

The first regime, before decoupling, is particularly interesting. In this case, $\frac{\Gamma_1}{H}$ is very large. Dividing both sides of our earlier equation by this fraction, we see that 

$$\left(1 - \frac{n_3 n_4}{n_1 n_2} \left( \frac{n_1 n_2}{n_3 n_4} \right)_{\text{eq}}\right) \approx 0$$

From here we get the so-called 'Saha approximation':

$$\frac{n_1 n_2}{n_3 n_4} \approx \left( \frac{n_1 n_2}{n_3 n_4} \right)_{\text{eq}}$$

Solving the Saha approximation equation allows us to see how different number densities and combinations of number densities change over time.
It is particularly useful for tracking the evolution of the universe from an opaque plasma to a transparent body of atoms. 
At some point, the Saha equation breaks down, and we are forced to solve the full, much more complication, Boltzmann equations.
(We'll leave that to the reader.)

### References
