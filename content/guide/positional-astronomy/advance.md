---
title: Advanced Topics
weight: 7
---

## Analemma and the Equation of Time

The analemma is the shape created by plotting the position of the Sun in the sky at the same civil time each day over the course of a year. The shape resembles a figure-eight and is a result of the tilt of the Earth's axis and its elliptical orbit around the Sun.

The northernmost and southernmost points of the analemma are the solstices. Deviation from the arc joining these points is due to the difference between the true Sun and the mean Sun.

If the axial tilt $\varepsilon$ is zero, the analemma would become an arc of a great circle. If the eccentricity $e$ of the orbit is zero, it will become a perfect figure-eight. If both are zero, the analemma will be a single point.

The following requires knowledge of Kepler's laws and orbital anomalies, covered in chapter 3.2.

When viewed from different locations and at different times of the day, the position and orientation of the analemma change; however, the shape remains the same. Thus, without loss of generality, assume the observer is at the North Pole, and the Sun's position is measured at noon. The altitude of the Sun will just be its declination $\delta$, and its azimuth will be the difference in the right ascension of the Sun and the Mean Sun. Since the Mean Sun moves at a constant rate, its right ascension is just its mean anomaly $M$. Let the ecliptic longitude of the Sun be $\lambda$, and its true anomaly be $\theta$. These two are related by

$$\tag{1.6.1} \lambda = \theta - \theta_\gamma $$

where $\theta_\gamma$ is the true anomaly of the vernal equinox. The true anomaly of the Earth is related to the mean anomaly of the Mean Sun by

$$\tag{1.6.2} \int_{\theta_\gamma}^{\theta} \frac{d\theta}{(1 + e \cos \theta)^2} = \frac{M}{(1-e^2)^{3/2}} $$

where $e$ is the eccentricity of the orbit. This relation can be derived using Kepler's second law, and the fact that the Mean Sun starts off from the vernal equinox instead of perihelion.

Using conversion identities (1.2.10), we can get the declination and right ascension of the Sun in terms of the ecliptic longitude:

$$\tag{1.6.3} \begin{align*}
\sin \alpha \cos \delta &= \cos \varepsilon \sin \lambda \\
\cos \alpha \cos \delta &= \cos \lambda \\
\sin \delta &= \sin \varepsilon \sin \lambda \\
\end{align*}$$

Since the time period of the Sun and Mean Sun is the same, their mean anomaly too is the same. Thus, the altitude and azimuth of the Sun are

$$\tag{1.6.4} (a, A) = (\delta, \alpha - M) $$

From this, we can conclude that the altitude difference between the lowest and highest points of the analemma is equal to twice the axial tilt of the Earth, $2\varepsilon$. Closely examining the azimuth, we see that it is the difference between the right ascension of the Sun and the mean anomaly of the Mean Sun, which is just the equation of time $\mathcal{E}$. Equation (1.6.3) can be solved numerically to get the equation of time as a function of the mean anomaly $M$, and also the shape of the analemma.

## Path of a Stick's Shadow

Consider the path the shadow of a vertical stick traces out during a day, as the Sun moves across the sky. The shape traced out by the shadow is a conic section—an ellipse, parabola, or hyperbola—depending on the position of the Sun relative to the observer.

Let the latitude of the observer be $\phi$ and the declination of the Sun be $\delta$. The length of the shadow of a unit length stick when the altitude of the Sun is $a$ is

$$ l = \frac{1}{\tan a} $$

We set up our coordinate system with the stick at the origin, the $x$-axis pointing east, and the $y$-axis pointing north. The angle the shadow makes with the north is just the azimuth of the Sun, $A$. Thus,

$$ x = l \sin A = \frac{\sin A}{\tan a} $$
$$ y = l \cos A = \frac{\cos A}{\tan a} $$

Using transformation formulae, we get

$$\begin{align*}
\sin A \cos a &= \sin h \cos \delta \\
\cos A \cos a &= \cos h \cos \delta \sin \phi - \sin \delta \cos \phi \\
\sin a &= \cos h \cos \delta \cos \phi + \sin \delta \sin \phi
\end{align*}$$

Substituting these into the equations for $x$ and $y$, we get

$$ x = \frac{\sin h }{\cos \phi (\cos h + \tan \delta \tan \phi)} $$
$$ y = \frac{\cos h \tan \phi - \tan \delta}{\cos h + \tan \delta \tan \phi} $$

Eliminating the hour angle $h$, we get

$$ \frac{\tan^2 \delta}{\cos^2 \phi} y^2 = x^2 (1 - \tan^2 \phi \tan^2 \delta) - 2 \frac{\tan \phi}{\cos^2 \delta} x + \tan^2 \phi - \tan^2 \delta $$

which is the equation of a conic section. The type of conic section depends on the values of $\phi$ and $\delta$.

- Circle: $\phi = \frac{\pi}{2}$
- Line: $\delta = 0$
- Point: $\delta = \frac{\pi}{2}$
- Ellipse: $\phi + \delta > \frac{\pi}{2}$
- Parabola: $\phi + \delta = \frac{\pi}{2}$
- Hyperbola: $\phi + \delta < \frac{\pi}{2}$

If $\phi = \delta$, the Sun passes through the zenith at noon, and there is no shadow.
