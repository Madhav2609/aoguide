---
title: Kepler's Laws
prev: /guide/celestial-mechanics/
weight: 1
---

Newton's law of universal gravitation describes gravity as a force by stating that every particle attracts every other particle in the universe with a force that is proportional to the product of their masses and inversely proportional to the square of the distance between their centers of mass. Consider two bodies of masses $m_1$ and $m_2$, with position vectors $\mathbf{r_1}$ and $\mathbf{r_2}$. The force exerted on body 2 due to body 1 is

$$\tag{3.1.1} \mathbf{F} = -\frac{G m_1 m_2}{|\mathbf{r_2} - \mathbf{r_1}|^3} (\mathbf{r_2} - \mathbf{r_1}) $$

Here G is the universal gravitational constant, equal to $6.67430 \times 10^{-11} \: \mathrm{m^3\,kg^{-1}\,s^{-2}}$.

Kepler's two body problem is to calculate and predict the motion of two bodies under the influence of their mutual gravitational attraction. The two bodies are assumed to be point masses, and the force acting on them is given by Newton's law of gravitation.

To solve for the trajectories of the two bodies, it is most convenient to work in the center of mass frame. The center of mass $\mathbf{R}$ of the two body system is given by

$$ \mathbf{R} = \frac{m_1 \mathbf{r_1} + m_2 \mathbf{r_2}}{m_1 + m_2} $$

The position vectors of the two bodies with respect to the center of mass are given by

$$
\mathbf{r_1} = \frac{-m_2}{M} \mathbf{r} + \mathbf{R} \qquad \qquad
\mathbf{r_2} = \frac{m_1}{M} \mathbf{r} + \mathbf{R}
$$

where $M = m_1 + m_2$ is the total mass of the system, and $\mathbf{r} = \mathbf{r_2} - \mathbf{r_1}$ is the vector joining the two bodies, also called the separation vector.

Working in the center of mass frame, $\mathbf{R} = \dot{\mathbf{R}} = \mathbf{0}$. With this, we now only have to solve for the trajectory of the separation vector $\mathbf{r}$, as a function of time. The center of mass frame is an inertial frame, and hence the motion of the two bodies can be described by Newton's second law.

To simplify the algebra, we define the reduced mass $m$ of the two body system as

$$\tag{3.1.2} m = \frac{m_1 m_2}{m_1 + m_2} $$

such that $Mm = m_1 m_2$. Further, we define the gravitational parameter $\mu$ as

$$\tag{3.1.3} \mu = G M = G (m_1 + m_2) $$

The force acting on the two bodies are

$$
\mathbf{F_1} = \mu m \frac{\mathbf{r}}{r^3} \qquad \qquad
\mathbf{F_2} = -\mu m \frac{\mathbf{r}}{r^3}
$$

Using Newton's second law $\mathbf{F} = m \mathbf{a}$, we can write

$$
\ddot{\mathbf{r_1}} = \frac{\mu m}{m_1} \frac{\mathbf{r}}{r^3} \qquad \qquad
\ddot{\mathbf{r_2}} = -\frac{\mu m}{m_2} \frac{\mathbf{r}}{r^3}
$$

Subtracting the two equations, we get

$$\tag{3.1.4} \boxed{\ddot{\mathbf{r}} = -\mu \frac{\mathbf{r}}{r^3}} $$

{{< callout type="remark" >}}
In the limit $m_1 \gg m_2$, we get that

- $M = m_1$
- $m = m_2$
- $\mathbf{r_1} = \mathbf{0}$
- $\mathbf{r_2} = \mathbf{r}$

We see that the trajectory of the separation vector is simply the trajectory of the smaller mass, $m_2$, in the center of mass frame, while the larger mass $m_1$ is at rest.

The separation vector $\mathbf{r}$ also gives the trajectory of one of the bodies when viewed in the frame of the other body (which is a non-inertial frame).
{{< /callout >}}

## Constants of Motion

The total orbital angular momentum is given by

$$
\begin{align*}
\mathbf{L} &= m_1 \mathbf{r_1} \times \mathbf{v_1} + m_2 \mathbf{r_2} \times \mathbf{v_2}\\
        &= m \mathbf{r} \times \mathbf{v}
\end{align*}
$$

where $\mathbf{v} = \dot{\mathbf{r}}$. The total energy of the system is given by

$$
\begin{align*}
E &= \frac{1}{2} m_1 v_1^2 + \frac{1}{2} m_2 v_2^2 - \frac{G m_1 m_2}{|\mathbf{r_1} - \mathbf{r_2}|^2} \\
  &= \frac{1}{2} m v^2 - \mu \frac{m}{r^2}
\end{align*}
$$

We define the specific angular momentum and specific energy as

$$
\begin{align*}
\mathbf{h} &= \frac{\mathbf{L}}{m} = \mathbf{r} \times \dot{\mathbf{r}}\\
\tag{3.1.1} \varepsilon &= \frac{E}{m} = \frac{1}{2} v^2 - \frac{\mu}{r}
\end{align*}
$$

Since gravitation is a central force, the angular momentum is conserved. Moreover since it is conservative, the total energy is also conserved. Hence $\mathbf{h}$ and $\varepsilon$ are constants of motion.

Since $\mathbf{h} \cdot \mathbf{r} = 0$, $\mathbf{h}$ lies perpendicular to the plane of motion, and hence defines the plane of motion. We define the eccentricity vector as

$$\tag{3.1.2} \mathbf{e} = -\frac{\mathbf{h} \times \dot{\mathbf{r}}}{\mu} - \frac{\mathbf{r}}{r} $$

Taking its time derivative

$$
\begin{align*}
\frac{d}{dt} \mathbf{e} &= \frac{d}{dt} \left( -\frac{\mathbf{h} \times \dot{\mathbf{r}}}{\mu} - \frac{\mathbf{r}}{r} \right) \\
&= -\frac{1}{\mu} \left(\mathbf{h} \times \ddot{\mathbf{r}} \right) - \left( \frac{\dot{{\mathbf{r}}}}{r} - \frac{\dot{r}}{r^2} \mathbf{r} \right)\\
&= -\frac{1}{\mu} \left( \left( \mathbf{r} \times \dot{\mathbf{r}} \right) \times \left(-\mu \frac{\mathbf{r}}{r^3} \right) \right) - \left( \frac{\dot{{\mathbf{r}}}}{r} - \frac{\dot{r}}{r^2} \mathbf{r} \right)\\
&= \frac{1}{r^3} \left[(\mathbf{r} \cdot \mathbf{r}) \dot{\mathbf{r}} - (\mathbf{r} \cdot \dot{\mathbf{r}}) \times \mathbf{r} \right] - \left( \frac{\dot{{\mathbf{r}}}}{r} - \frac{\dot{r}}{r^2} \mathbf{r} \right)\\
&= \frac{1}{r^3} \left( r^2 \dot{\mathbf{r}} - r \dot{r} \mathbf{r} - r^2 \dot{\mathbf{r}} + r \dot{r} \mathbf{r} \right)\\
&= 0\\
\end{align*}
$$

we find that the eccentricity vector does not change with time, hence is also a constant of motion. It lies in the plane of motion ($\mathbf{h} \cdot \mathbf{e} = 0$) and points in the direction of the periapsis. The magnitude of the eccentricity vector is given by

$$\tag{3.1.3} e = \sqrt{1 + \frac{2 \varepsilon h^2}{\mu^2}} $$

## First Law

The angle between the eccentricity vector and the position vector is called the true anamoly $\theta$

$$ \mathbf{r} \cdot \mathbf{e} = r e \cos \theta = \mathbf{r} \cdot \left( -\frac{\mathbf{h} \times \dot{\mathbf{r}}}{\mu} - \frac{\mathbf{r}}{r} \right) = \frac{h^2}{\mu} - r$$

$$\tag{3.1.4} \implies \boxed{r = \frac{h^2 / \mu}{1 + e \cos \theta}} $$

This, if one may recognize, is the equation of a conic section in polar coordinates, with the focus being at origin and length of the semi-latus rectum being $p = \frac{h^2}{\mu}$, which gives the relation

$$\tag{3.1.5} h = \sqrt{\mu p}$$

The magnitude of $\mathbf{e}$ determines the shape of the trajectory:

- $e = 0$: Circle
- $0 \leq e < 1$: Ellipse
- $e = 1,\, h \neq 0$: Parabola
- $e > 1$: Hyperbola
- $e = 1,\, h = 0$: Straight line (degenerate conic section)

where the focus of the conic section lies at the center of mass of the system.

The individual trajectories of the two bodies in the center of mass frame is therefore

$$ r_1 = \frac{m_2}{M} \frac{h^2 / \mu}{1 + e \cos \theta} \,, \qquad \qquad r_2 = \frac{m_1}{M} \frac{h^2 / \mu}{1 + e \cos \theta} $$

The trajectories of the two bodies however will be oriented opposite to each other, with an angle of $\pi$ radian between them, keeping the center of mass fixed.

The energy of the system can thus be determined by just the eccentricity $e$ and length of semi-latus rectum $p$ of the trajectory. The total energy of the system is given by

$$e^2 = 1 + \frac{2h \varepsilon}{\mu^2} \implies \varepsilon = \frac{1}{2} \left( e^2 - 1 \right) \frac{\mu^2}{h^2}$$

$$\tag{3.1.6} \implies \varepsilon = -\frac{1}{2} \frac{\mu (1 - e^2)}{p}$$

We see that the sign of the total energy depends on the eccentricity of the trajectory

- $0 \leq e < 1$: An elliptical trajectory gives a negative total energy, and hence a bound orbit
- $e = 1$: A parabolic trajectory gives a zero total energy, and hence an unbound orbit
- $e > 1$: A hyperbolic trajectory gives a positive total energy, and hence an unbound orbit

We see that all bound orbits are ellipses, and all unbound orbits are hyperbolae or parabolae.

For our solar system, the sun is much more massive than any of the planets, hence is nearly at the center of mass, or the focus of the elliptical orbits of all planets. This proves Kepler's first law of planetary motion, which states that the orbit of a planet is an ellipse with the sun at one of the foci.

## Second Law

The cross product of two vectors gives the area of a parallelogram possessing sides of those vectors, hence the triangular area $dA$ swept out in a short period of time is given by half the cross product of the $\mathbf{r}$ and $\mathbf{dr}$ vectors, for some short piece of the orbit, $\mathbf{dr}$.

$$ dA = \frac{1}{2}|\mathbf{r} \times \mathbf{dr}| = \frac{1}{2}|\mathbf{r} \times \mathbf{v} dt| = \frac{h}{2} dt $$

$$\tag{3.1.7} \implies \boxed{\frac{dA}{dt} = \frac{h}{2}} $$

which is constant. This proves Kepler's second law of planetary motion, which states that a line segment joining a planet and the sun sweeps out equal areas during equal intervals of time.

## Third Law

Consider two bodies moving in bound elliptical orbits, with the semi-major axis of the orbit being $a$, and the semi-minor axis being $b$. The lengths of the two axes are related by the eccentricity of the orbit, $e$, as

$$ e^2 = 1 - \frac{b^2}{a^2} $$

The area of an ellipse is $\pi a b = \pi a^2 \sqrt{1 - e^2}$. Moreover, the length of the semi-latus rectum is $p = \frac{b^2}{a} = a (1 - e^2)$, hence $h = \sqrt{\mu a (1 - e^2)}$

Integrating the equation of areal velocity, we have

$$
\begin{align*}
dA &= \frac{h}{2} dt\\
\int dA &= \frac{h}{2} \int dt\\
\pi a^2 \sqrt{1 - e^2} &= \frac{1}{2} \sqrt{\mu a (1 - e^2)} P\\
\end{align*}
$$

Rearranging, we get

$$\tag{3.1.8} \boxed{P^2 = \frac{4 \pi^2}{\mu} a^3} $$

where $P$ is the period of one revolution. This is known as Newton's form of the third law. If we work in the units of AU, sidereal years, and solar masses, we have $G M_\odot = 4 \pi^2$. Hence the equation simplifies to

$$\tag{3.1.9} \boxed{a^3 = M P^2} $$

In our solar system, $M = M_\odot + m_{planet} \approx M_\odot = 1$, we get the relation $P^2 = a^3$. This proves Kepler's third law of planetary motion, which states that the square of the period of revolution of a planet is directly proportional to the cube of the semi-major axis of its orbit.
