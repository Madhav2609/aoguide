---
title: Bound Orbits
weight: 2
---

Having finished Kepler's laws, you might ask why we need to study the two-body problem any further at all.
Well, the idea is similar to why, after learning Coulomb's law, we still devote a fair amount of time to learning further electrostatics.

The answer is simply practical application. It is much easier to derive some results regarding the system and use them to make our lives easier when solving problems. For instance, you could, theoretically, now that you know $r(\theta)$, figure out $r(t)$ without any of the tools we discuss below, but it would be a much more daunting task.

Anyway, we are still only considering the problem of a two-body system, but we'll primarily work with bound orbits and see what we can do with them.

As we proved in chapter 3.1, *all* bound orbits are elliptical. Therefore, a fair amount of the following discussion is going to rely on some knowledge of ellipses. You should have ideally finished reading the Wikipedia page or used an equivalent resource.

Consider an ellipse with semi-major axis $a$, semi-minor axis $b$, and eccentricity $e$. As you may know, the semi-major axis is half the length of the longest radius of the ellipse, while the semi-minor axis is half the length of the shortest radius. Here, radius refers to the distance from the *center* (not the foci) to the boundary.

I'll just go through some useful results for ellipses that we will need later. I'll urge you to go through this before proceeding, as it's vital to the succeeding discussions.

The semi-minor and semi-major axes are related by

$$ b^2 = a^2 (1 - e^2) $$

The eccentricity of an ellipse is always less than 1, being 0 for a circle. Now, we can use the equation of the ellipse with the origin at one of the foci:
$$
r = \frac{a(1-e^2)}{1 + e\cos\theta}
$$
to find the smallest and largest $r$. This gives the length of the periapsis, which is the point closest to the foci, and apoapsis, the point farthest from the foci:

$$
\begin{align*}
r_p &= a (1 - e)\\
r_a &= a (1 + e)
\end{align*}
$$

From this, we get the relations

$$ a = \frac{r_p + r_a}{2}
\,, \qquad \qquad e = \frac{r_a - r_p}{r_a + r_p} $$

The semi-latus rectum $p$ of an ellipse is defined as the distance from the focus to the ellipse along a line perpendicular to the major axis. It is given by

$$ p = \frac{b^2}{a} = a (1 - e^2) $$

From this, eqns. $(3.1.8)$, $(3.1.10)$; we get that the total energy and angular momentum of the orbit in terms of $a$ and $e$ are:
$$
\begin{align*}
\tag{3.2.1} \varepsilon &= -\frac{\mu}{2a}\\
\tag{3.2.2} h &= \sqrt{\mu a (1 - e^2)}
\end{align*}
$$

From here on, for all subsections except the last one, we consider the case when $m_2 \gg m_1$, which is the case for, for example, our solar system.

## Orbital Velocity

Because we know the value of energy in terms of the parameters now, and the velocity and radius
are related by the energy, we can use eqns. $(3.1.7)$ and $(3.2.1)$ to get the *vis-viva equation*:

$$ \frac{1}{2} v^2 - \frac{\mu}{r} = \varepsilon = -\frac{\mu}{2a} $$

$$\tag{3.2.3} \implies \boxed{v^2 = \mu \left( \frac{2}{r} - \frac{1}{a} \right)} $$

This gives us the velocity of the smaller body at a distance $r$ from the larger body. From here you can see that the velocity is maximum at periapsis and minimum at apoapsis, because it roughly depends on $1/\sqrt{r}$. The velocity at periapsis is then (using the expression for $r_p$ that we found earlier):

$$v_p = \sqrt{\mu \left( \frac{2}{r_p} - \frac{1}{a} \right)} = \sqrt{\frac{\mu}{a} \left( \frac{1+e}{1-e} \right)} $$

And the velocity at apoapsis is:
$$v_a = \sqrt{\mu \left( \frac{2}{r_a} - \frac{1}{a} \right)} = \sqrt{\frac{\mu}{a} \left( \frac{1-e}{1+e} \right)} $$

You can see that they're sort of very symmmetric, if we multiply or divide them, one of the term cancels out! This
gives us some very nice relations:

$$ v_p v_a = \frac{\mu}{a}\,, \qquad \qquad \frac{v_p}{v_a} = \frac{1+e}{1-e} $$

As something you should always do when you have a formula with a parameter you can vary, we can ask what the limiting cases of this are. Since $e$ is bound between $0$ and $1$, let's see what we can do. $e \to 1$ is not really a nice case, for one the orbit becomes unbound, and everything diverges. On the other hand, we can talk about $e = 0$ precisely!

In the case of a circular orbit, we have $e = 0$. The body therefore moves with a *constant speed* $v_c$, called the circular velocity, given by
$$\tag{3.2.4} v_c = \sqrt{\frac{\mu}{a}} $$

For the body to escape the gravitational influence of the larger body and become unbound, the total energy of the system must become more than or equal to 0. We can see this through the conservation of energy. Let the initial velocity be $v$. Finally, we need the velocity to
be just non-zero to find the minimum velocity. Note that far away, the potential energy goes to $0$. Pairing this up
with the fact that $K = mv^2/2$ is going to be $0$ for the minimum velocity, we get that the total energy must be $0$.

So the *escape veloctiy* is such that the total energy is $0$. Using the expression for total energy from Kepler's Laws, and since initially the seperation between the bodies is $r$;
$$
0 = \frac{1}{2}mv_e^2 - \mu\frac{m}{r^2} \implies v_e = \sqrt{\frac{2\mu}{r}}
$$

Thus for the smaller body to escape, the minimum velocity needed is:
$$\tag{3.2.5} v_e = \sqrt{\frac{2\mu}{r}} = \sqrt{2} v_c$$

From eqn. $(3.1.13)$, the time period of the circular orbit is:
$$ P = 2 \pi \sqrt{\frac{a^3}{\mu}} $$

## Kepler's Equation

We know what the equation for $r(\theta)$ is, but what about the position as a function of time? It turns out, that's a fairly more difficult task, and the neatest way to do this is using *anomalies*, parameters that describe the motion of our lighter body. As I said when discussing the first law of Kepler, we call the angle between the eccentricity vector and the position vector the *true anomaly*, $\theta$.

Note that because the position vector from the center of mass (which is effectively the larger body here) $r$ is:
$$
r = \frac{h^2/\mu}{1 + e\cos\theta},
$$
the periapsis occurs at $\theta = 0$. So the true anomaly, stated in another manner, measures the angle from the periapsis.
If we can somehow find the true anomaly as a function of time, our job is essentially done because we already know $r(\theta)$.

The idea that we use here is to use a *fictious* circular body (this is closely related to the fact that elliptical motion is a superposition of two independent circular motions). The mean motion $n$ is defined as
$$n \overset{\text{def}}{\equiv} \frac{2 \pi}{P}$$

Let the instant at which the body was at periapsis be $\tau$. We define the mean anomaly $M$ as the *angular distance* from the periapsis which a fictitious body would have if it moved in a circle of radius $a$ (the semi-major axis length). At any instant in time $t$, it is clearly given by:
$$\tag{3.2.6} M = n (t - \tau) $$

{{< callout type="image" >}}
{{< svg "celmech/Mean_anomaly_diagram.svg" "Mean and True Anomaly" "Mean and True Anomaly" >}}
{{< /callout >}}

As it turns out, our equations become much neater if we ignore the true anamoly, and insteard work with the *eccentric anomaly*.
We defined the eccentric anamoly $E$ as the eccentric angle of the smaller body in its elliptical orbit (see the figure). In cartesian coordinates with the center of the ellipse being at origin, the equation of the ellipse becomes

$$ \frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 $$

The eccentric anamoly $E$ in terms of these coordinates is given by

$$ \cos E = \frac{x}{a}\,, \qquad \qquad \sin E = \frac{y}{b} $$

As a consequence, since $r = x^2 + y^2$, and $b^2 = a^2(1-e^2)$ we get that the distance of the smaller body from the larger body (foci of the ellipse) is given by

$$ r = a (1 - \cos E) $$

Now since $\mathbf{r}(\theta) = r(\cos\theta \hat{\mathbf{{i}}} + \sin\theta \hat{\mathbf{j}})$, comparing it with expression for $x$ and $y$ that we have, we get that the eccentric anamoly $E$ and true anamoly are related by
$$ \cos \theta = \frac{a}{r} (\cos E - e) \qquad \qquad \sin \theta = \frac{b}{r} \sin E $$

so that

$$\tag{3.2.7} \tan \frac{\theta}{2} = \sqrt{\frac{1+e}{1-e}} \tan \frac{E}{2}.$$

{{< callout type="image" >}}
{{< svg "celmech/Eccentric_Anomaly.svg" "Eccentric Anomaly" "Eccentric Anomaly, The Point P is at (x,y). Reproduced from Katturnen et al., Fundamental Astronomy" >}}
{{< /callout >}}

Using Kepler's second law, the total area covered by the smaller body in the shaded region (see the previous figure) is:
$$
A = \pi ab \frac{t - \tau}{P} = \frac{1}{2}ab M
$$
when it is present at the eccentric angle $E$. Also, since an ellipse is a rescaling of a circle, the area is $b/a$ times the area of $FP'X$. Thus one obtains from someone geometry that the area of $FPX$ is:
$$
A = \frac{1}{2}ab(E - e\sin E)
$$

We then equate these to find the relation between the mean anamoly $M$ and the eccentric anamoly $E$ as

$$\tag{3.2.8} M = E - e \sin E $$

This is called Kepler's equation. It is a *transcendental equation*, and we can solve it using numerical methods.

Using an infinite series expansion, we can solve it exactly:

$$ E = M + e \sin M + \frac{e^2}{2} \sin 2M + \frac{e^3}{6} \sin 3M + \ldots $$

Using this and the relations we found, the true anamoly (if you so want) and distance from focus too can be obtained in terms of infinite series expansion, given by

$$
\begin{align*}
\theta &= M + {2e \sin M} + \frac{5e^2}{4} \sin 2M + \frac{e^3}{12} (12 \sin 3M - 3 \sin M) + \cdots\\
\frac{r}{a} &= 1 - e\cos M + \frac{e^2}{2} (1 - \cos 2M) + \frac{3e^3}{8} (\cos M - \cos 3M) + \cdots
\end{align*}
$$

And thus we *have* found $r(t)$.

## Radial Elliptic trajectory

A radial elliptic trajectory is a degenerate case of an elliptical trajectory, where the eccentricity $e$ is equal to 1 and the angular momentum of the system is zero. The trajectory is a straight line, and the two bodies collide with each other at some point in the trajectory. It is still classified as an elliptic trajectory since the total energy of the system is negative.

## Binary Systems

Consider a binary system having two bodies of masses $m_1$ and $m_2$ moving in bound orbits. Both the bodies move in ellipses of equal eccentricities but oriented opposite to each other. Properties of orbits of individual bodies will be labelled with a subscript (e.g. $x_1$ and $x_2$), and properties of the trajectory of the separation vector, or the orbit of one of the bodies relative to the other will be written without a subscript (e.g. $x$).

The semi-major axes $a$ are related by the center of mass relation,

$$\tag{3.2.9} m_1 a_1 = m_2 a_2 = ma \implies a = a_1 + a_2 $$

Similarily, in the center of mass frame, the speeds $v$ are related by

$$\tag{3.2.10} m_1 v_1 = m_2 v_2 = m v \implies v = v_1 + v_2$$

When an elliptical orbit is projected onto a plane, it produces another ellipse. However, the foci of the original ellipse does not project onto the foci of the observed ellipse.

Consider a binary system at a distance $r$ from us, inclined at an angle $i$, which is the angle between the plane of the orbit and plane of the sky. $\alpha$ and $\tilde{\alpha}$ be the true and observed angular semi-major axes. They are related by the equations

$$ m_1 \alpha_1 = m_2 \alpha_2 = m \alpha \implies \alpha = \alpha_1 + \alpha_2$$
$$ m_1 \tilde{\alpha}_1 = m_2 \tilde{\alpha}_2 = m \tilde{\alpha} \implies \tilde{\alpha} = \tilde{\alpha_1} + \tilde{\alpha_2} $$
$$\tag{3.2.11} \tilde{\alpha} = \alpha \cos i $$

The true semi-major axis $a$ is given by

$$a = r \alpha = r \tilde{\alpha} \cos i$$

Hence Kepler's third law can be written as

$$\tag{3.2.12} m_1 + m_2 = \frac{4\pi^2}{G} \frac{a^3}{P^2} = \frac{4\pi^2}{G} \left( \frac{r}{\cos i} \right)^3 \frac{\tilde{\alpha}^3}{P^2}$$

Usually, for a binary system, only the radial velocity of the bodies can be measured. If the trajectory of the binary system is circular, the radial velocity is given by $v = \frac{2 \pi a}{T}$. The maximum radial velocity observed is $v_r = v \sin i$

$$ a = a_1 + a_2 = \frac{P}{2 \pi} (v_1 + v_2) = \frac{P}{2 \pi \sin i} (v_{1r} + v_{2r}) $$
$$\tag{3.2.13} \implies m_1 + m_2 = \frac{P}{2 \pi G} \frac{(v_{1r} + v_{2r})^3}{\sin^3 i} $$

If only one velocity ($v_{1r}$) is observable, $v_{2r}$ can be obtained using $m_1 v_{1r} = m_2 v_{2r}$. Putting this into the equation above, we get

$$\tag{3.2.14} \boxed{ \frac{m_2^3}{(m_1 + m_2)^2} \sin^3 i = \frac{P}{2 \pi G} v_{1r}^3 } $$

This is the mass function of the binary system. The mass function can be used to determine the mass of the secondary body if the mass of the primary body is known. The mass function can also be used to determine the inclination of the orbit if the masses of both bodies are known. It also sets a lower limit on the mass of $m_2$:

$$\tag{3.2.15} m_2 \geq \frac{P}{2 \pi G} v_{1r}^3 $$

## Problems

{{< tabs >}}
    {{< tab name="P1" >}}
    A Sun-orbiting periodic comet is the farthest at $31.5 \mathrm{\,AU}$ and the closest at $0.5 \mathrm{\,AU}$. What is the orbital period of this comet? What is the area (in $\mathrm{AU^2/yr}$) swept by the line joining the comet and the Sun?
    {{< /tab >}}

    {{< tab name="Solution" >}}
    The semi-major axis of the orbit is

    $$a = \frac{r_p + r_a}{2} = 16 \mathrm{\,AU}$$

    Using Kepler's third law, we have

    $$P^2 = a^3 = 16^3 = 4096 \implies \boxed{P = 64 \mathrm{\,years}}$$

    The eccentricity and semi-latus rectum can be found using

    $$e = \frac{r_a - r_p}{r_a + r_p} = \frac{31.5 - 0.5}{31.5 + 0.5} = \frac{31}{32}$$

    $$p = a(1 - e^2) = 16 \left( 1 - \frac{31^2}{32^2} \right) = 16 \left( \frac{63}{1024} \right) = 0.98 \mathrm{\,AU}$$

    Therefore the rate of area swept is

    $$\frac{dA}{dt} = \frac{h}{2} = \frac{\sqrt{\mu p}}{2} = \frac{\sqrt{4 \pi^2 p}}{2} = \pi \sqrt{p} = \pi \cdot \sqrt{0.98} = \boxed{3.1 \mathrm{\, AU^2/yr}}$$
    {{< /tab >}}
{{< /tabs >}}

{{< tabs >}}
    {{< tab name="P2" >}}
    Estimate the radius of a planet that a man can escape its gravitation by jumping vertically. Assume density of the planet and the Earth are the same.
    {{< /tab >}}

    {{< tab name="Solution" >}}
    A man can jump to a height $h \approx 50 \mathrm{\,cm}$ on Earth. This gives the man's jump velocity to be $v_\text{jump} = \sqrt{2g_\oplus h}$. Equating it to the escape velocity of the planet, we get

    $$\sqrt{2g_\oplus h} = \sqrt{\frac{2GM}{R}} \implies \sqrt{2\frac{G}{R_\oplus^2} \frac{4 \pi \rho_\oplus R_\oplus^3}{3} h} = \sqrt{\frac{2G}{R} \frac{4 \pi \rho R^3}{3}}$$

    Since $\rho = \rho_\oplus$, we have

    $$ R = \sqrt{R_\oplus h} \approx \boxed{1.79 \times 10^3 \mathrm{\,m}}  $$
    {{< /tab >}}
{{< /tabs >}}

{{< tabs >}}
    {{< tab name="P3" >}}
    A projectile which starts from the surface of the Earth at the sea level is launched with the initial speed of $v_0 < \sqrt{\frac{2GM_\oplus}{R_\oplus}}$ and the projecting angle (with respect to the local horizon) of $\theta$. Ignore the air resistance.
    1. The orbit of the projectile is an ellipse. Find its semi-major axis $a$ in units of $R_\oplus$.
    2. Calculate the highest altitude of the projectile with respect to the Earth surface (in units of $R_\oplus$)
    3. Find the time of filght for the projectile.
    4. What is the range of the projectile (surface distance between launching point and falling point) in the units of $R_\oplus$?
    5. What is the eccentricity $e$ of this elliptical orbit?
    {{< /tab >}}

    {{< tab name="Solution" >}}
    Coming Soon
    {{< /tab >}}
{{< /tabs >}}
