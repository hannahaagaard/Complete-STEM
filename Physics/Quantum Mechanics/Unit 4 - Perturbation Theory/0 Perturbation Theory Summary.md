# Unit Summary
Tags: #Summary #UAG

Relevant files: [[L11_NonDegeneratePeturbationTheory.pdf|Lecture 11 (Perturbation theory intro)]], [[L12_Degenerate PT.pdf|Lecture 12 (Degenerate Perturbation theory)]], [[L13_PerturbationsOfHydrogen.pdf|Lecture 13 (Perturbation of Hydrogen)]],[[L15_TimeDependentPT.pdf|Lecture 15 (Time Dependent PT)]]

## General Idea
The entire idea of perturbation theory it to take a comparison state which you know a solution to and then slowly approximate the actual solution using a series of corrections. 

There are two things which need to be corrected in this case: the energy, and the wavefunction

In order to correct the energy we have the following equations for the corrections
$$
\large\begin{align}
	\text{First Order: } E^{'}_n = \langle \psi_n^0 \vert H^{'} \vert \psi_n^0 \rangle \\
%
	\text{Second Order: } E^2_n = \sum_{m \ne n} \frac{\vert \langle \psi_m^0 \vert \hat{H^{'}} \vert \psi_n^0 \rangle \vert^2}{E^0_n - E^0_m}
\end{align}
$$
We have the following equation for correcting the energy for the first order!
$$
\large \vert \psi_n^{'} \rangle = \sum_{m \ne n} \frac{\langle \psi_m^{0} \vert \hat{H^{'}} \vert \psi_n^{0} \rangle}{E_n^0 - E_m^0} \cdot \vert \psi_m^{0} \rangle
$$

## Degenerate States
Previously with perturbation theory we found that the wave function corrections require that the states aren't degenerate (i.e. each energy is unique). However, there are many situations with degenerate energies! The thing is that the perturbations can split these degeneracies into different levels. If we can find these split states we can continue to use the previous theory! So we just need to find the "good" states. We can do this by solving an **eigenvector problem**. 
$$
\large \hat{H^{'}} \vert\psi^0_{i}\rangle = E^{'}_{i} \vert\psi^0_{i}\rangle
$$
In this case $\large\hat{H^{'}}$ is represented in the basis of the degenerate states such as
$$
\large \langle \phi_a^0 \vert \hat{H^{'}} \vert \phi^0_b \rangle
$$
## Time dependence
If we use previous systems we will find that it's physically impossible for the system to transition to other states!! In order to allow for these transitions we need to figure out how to deal with non-static potentials. In particular a modification to perturbation theory can accomplish this!

We can start with this modification by breaking the hamiltonian into a stable and time dependent portion: $\large \hat{H} = \hat{H^0} + \hat{H^{'}}(t)$ and we can model the coefficients in front of the stable hamiltonian as time dependent. From here the schroedinger equation can be simplified to find equations of motion for the coefficients of each of the valid system states. Initially we have:
$$
\large\begin{align}
i \hbar \frac{\partial}{\partial t} \vert\psi(t)\rangle = \lbrack \hat{H^0} + \hat{H^{'}}(t)\rbrack \vert\psi(t)\rangle
\end{align}
$$
For a two state system this becomes:
$$
\large\begin{align}
{\dot c_1 \choose \dot c_2} = -\frac{i}{\hbar}{ H^{'}_{11}c_1 + H^{'}_{12}c_2e^{-i \omega_0 t}
\choose
 H^{'}_{21}c_1e^{-i \omega_0 t} + H^{'}_{22}c_2
}
\end{align}
$$

Solving these equations then leads to an evolving system which allows for transitions! However solving these can be quite difficult because you know differential equations is hard. In general we can **assume the perturbations are small in order to use a power series**. Like non-degenerate perturbation theory before we can collect this power series according to a parameter. Then we can come to the conclusion that the first term of this power series looks exactly like the above equation.

## Example: Perturbation of Hydrogen
