# Unit Summary
Tags: #Summary #UAG

Relevant files: [[L5_SternGerlach.pdf|Lecture 5 (Stern Gerlach)]], [[L6_SpinOneHalf.pdf|Lecture 6 (Spin one half)]], [[L7_SpinPrecession.pdf|Lecture 7 (Spin Precession)]], [[L8_Addition of Angular Momentum.pdf|Lecture 8 (Angular Addition)]]

## Spin in general
Previously we've talked about angular momentum as it relates between two particles. Now we are dealing with spin which is intrinsic to the particles which we are working with! This type of angular momentum is called "spin" and every particle has spin of some amount.

Just like orbital angular momentum; spin is discrete and has specific values associated with it. However, the odd result is that there are only integer differences between the available spins. This results in odd situations in which the spin of an electron and other particles is found to be a **half integer**.

Using spin we can construct the following operators which are significant
$$
\large\begin{align}
\text{Directional: } \lbrack S_x, S_y \rbrack = i \hbar S_z &&
	\lbrack S_y, S_z \rbrack = i \hbar S_x &&
	\lbrack S_z, S_x \rbrack = i \hbar S_y
\end{align}
$$
$$
\large\begin{align}
\text{Z-basis: } S^2 \vert s \space m \rangle = \hbar^2 s (s+1) \vert s \space m \rangle &&
	S_z \vert s \space m \rangle = \hbar m \vert s \space m \rangle
\end{align}
$$
$$
\large\begin{align}
\text{Ladder: } S_{\pm} \vert s \space m \rangle = \hbar \sqrt{s (s + 1) - m (m \pm 1)} \vert s \space m \rangle
\end{align}
$$
Unless specified these operators can be assumed to be based in the z-axis instead of something else

### Stern-Gerlach Experiment
This experiment is the entire reason why spin is known to be different than orbital momentum.

## Electron Spin
### Ladder Operators
Using the above ladder operator we can find that

### Pauli Matrices
In order to understand how applying each of the directional spin operators affects half spin particles we need to define what the matricies actually are! These are defined using the Pauli matrices which define exactly what each operator does
$$
\large\begin{align}
\sigma_x \equiv {0, 1 \choose 1, 0}
&&
%
\sigma_y \equiv {0, -i \choose i, 0}
&&
%
\sigma_z \equiv {1,0 \choose 0, 1}
\end{align}
$$

### Spin Precession
If we apply a magnetic field unaligned with the spin the particle will precese in a circle. In particular this is the result relative to the z-axis
$$
\large\begin{align}
	\langle S_x \rangle = \frac{\hbar}{2} \sin(\theta)\cos(\omega_0t - \phi) \\
	%
	\langle S_y \rangle = \frac{\hbar}{2} \sin(\theta)\sin(\omega_0t - \phi) \\
	%
	\langle S_z \rangle = \frac{\hbar}{2} \cos(\theta)
\end{align}
$$

## Addition of Angular Momentum
### Two Particle Systems
#### Triplet and Singlet state
### Clebsch-Gordon Table
![[Addition Table.JPG]]
