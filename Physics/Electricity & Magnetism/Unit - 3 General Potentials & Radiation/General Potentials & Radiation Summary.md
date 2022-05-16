# General Potentials & Radiation UAG
Tags: #Summary, #UAG

Relevant files: [[EQ Sheet U3.jpg|Reference sheet from Linda]], 

__This unit has some fairly complicated derivations. Please refer to the derivations folder if you get confused__

This unit expanded on previous ones by considering the full maxwell equations. This complicates most things because it adds on a time dependance onto the derivations. This time dependance is not simple due to the speed of light and *time existing*. Let's start by expressing the Maxwell equations

$$
\large\begin{align}
1) \vec\nabla \cdot \vec{E} = {\rho /\epsilon_0} &&
2) \vec\nabla \times \vec{E} = \frac{-\partial \vec{B}}{\partial t} \\\\
3) \vec\nabla \cdot \vec{B} = 0 &&
4) \vec\nabla \times \vec{B} = \mu \vec{J}_0 + \mu_0 \epsilon_0 \frac{\partial \vec{E}}{\partial t}
\end{align}
$$

## Potentials and Fields
Previously we had derivations of the fields and the potentials which did not account for time dependance. We now need to expand these definitions using various means since we are now considering the full equations. In particular this means doing two things

1. Taking into account the amount of time it takes for light to propagate
2. Changing the guage definition to account for the new time dependance!

### Retarded Time
The first is accomplished by defining **retarded time** which is a shifted time according to how far away we are from the signal origin. In a more classical sense it's the amount of time it takes to get to some position assuming that light is traveling at a speed. This quantity naturally follows as

$$
\huge\begin{align}
t_r = t - \mathscr{r}/v
\end{align}
$$
From here we define all of our previous relationships using this variable instead of the normal time. Effectively there is a coordinate system shift being applied!! This coordinate shift allows us to use the Lorentz gauge

### Lorentz Gauge
Previously we applied the Coulomb gauge when deriving the solutions to our equations. However due to the inclusion in time we now require an additional term. Through the application of Maxwell's equations the obvious gauge is the following (aka the Lorentz Gauge)
$$
\large\begin{align}
	\vec\nabla \cdot \vec{A} = -\frac{1}{c^2}\frac{\partial V}{\partial t}
\end{align}
$$
Also allows for the guage transformations which can be useful to shift the potential in some way
$$
\large\begin{align}
	\vec{A'} = \vec{A} + \vec\nabla \lambda &&
	V' = V - \frac{\partial \lambda}{\partial t}
\end{align}
$$


### General Potentials
$$
\large\begin{align}
	V_{ret} = \frac{1}{4 \pi \epsilon_0} \int{\frac{\rho(\vec{r} \space^{'}, t_r)}{\mathscr{r}} d\tau^{'}} \\\\

	\vec{A}_{ret} = \frac{\mu_0}{4 \pi} \int{\frac{\vec{J}(\vec{r} \space^{'}, t_r)}{\mathscr{r}} d\tau^{'}}
\end{align}
$$

## Radiation
### General Waves
This is typically in the far field and also has some assumptions about the construction of the dipole
$$
\large\begin{align}
	r'/r \ll 1 &&
	\lambda / r \ll 1 &&
	d/\lambda \ll 1
\end{align}
$$
The first of these allows for a binomial expansion while the second and third provide for larger simplifications later on. Generally this first approximation results in the following
$$
\large\frac{1}{\mathscr{r}} \approx \frac{1}{r}(1 + \frac{\vec r \cdot \vec r '}{r^2})
$$
This is a super useful result which is used in a lot of diagrams. In addition the general wave equations apply in these situations for the dipole
$$
\large\nabla^2 f - \frac{1}{v^2} \frac{\partial^2 f}{\partial t^2} = 0
$$

### Larmor equations
This equation describes the average power radiated away from a non-relativistic point charge. This equation is super useful
$$
\large\begin{align}
	P = \frac{\mu_0 \space q^2 \space a^2}{6 \pi c}
\end{align}
$$
Here are some typical antenna equations for the average power!
$$
\large\begin{align}
	\text{Electric Dipole} && \text{Oscillating Loop} \\\\
	P = \frac{\mu_0 \space p_0^2 \space \omega^4}{12 \pi c} &&
	P = \frac{\mu_0 \space m_0^2 \space \omega^4}{12 \pi c^3}
\end{align}
$$

### General power
The above equations are common equations which can be used for simple antenna were derived using the Poynting vector and integrating it over a spherical surface. This results in the following general equation
$$
\large\begin{align}
	P = \frac{\mu_0 \ddot\rho^2}{6 \pi c}
\end{align}
$$
The small p in this case is the dipole moment of whatever we are describing

### Relativistic Particles
The general power equation can also be applied to relativistic particles and depending on how the acceleration is oriented to the velocity you get one of the two following equations
$$
\large\begin{align}
	\text{Perp case: } \vec a \perp \vec v && \text{Para case: } \vec a \parallel \vec b \\\\

	P = \frac{\mu_0 \space q^2 \space a^2}{6 \pi c}\gamma^4 &&
	P = \frac{\mu_0 \space q^2 \space a^2}{6 \pi c}\gamma^6
\end{align}
$$
Good luck 🙂