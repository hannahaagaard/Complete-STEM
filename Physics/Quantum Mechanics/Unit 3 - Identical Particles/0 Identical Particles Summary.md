# Unit Summary
Tags: #Summary #UAG

Relevant files: [[L9_IdenticalParticles.pdf|Lecture 9 (Two particle wavefunctions)]], [[L10_IdenticalParticles.pdf|Lecture 10 (Distinguishable, Bosons, Fermions)]]

The solution to the wave function is entirely dependent on the structure of the potential in which the particle is in. It's the structure of this potential that has allowed us to find specific solutions before. However, now we want to introduce multiple particles into this potential which adds additional requirements for the solvability of the system. 
## Two particle wave functions
In general the different aspects of a wave function (position, and spin for example) are independent of one another. This means that we can solve the two problems independently! 

## Identical particles
In order to create identical particles we have to construct the wave function in a specific way such that it obeys a few rules. In order to accomplish this the wave function must exchange the independent variables the form of each wave function depends on. This can be done by using the following form
$$
\large \psi^{Overall}_{n_1 n_2}(x_1, x_2) = A \lbrack \psi_{n_1 n_2}(x_1, x_2) \pm \psi_{n_1 n_2}(x_2, x_1) \rbrack
$$
This permutation of independent variables allow the overall wave function to still be indistinguishable between the two particles while also not restricting their form!

> [!info]- Distinguishable particles
> These particles have no rules associated with them!

>[!info]- Identical fermions
>A fermion is a type of particle which has a half integer spin
>
  The overall wave function **must be anti-symmetric** which means that the spin state and the position function must be opposites of one another.
>
>In addition, fermions must obey the Pauli exlusion principle which means that no two fermions can be in the same state.

> [!info]- Identical Bosons
A boson is a special kind of particle which has a net integer spin
The overall wave function **must be symmetric** which means that the spin state and the position function must be the same parity. Either both are symmetric or both are anti-symmetric

## Exchange Forces
Comes down to the form
$$
\large \langle(x_2-x_1)^2 \rangle = \langle x^2 \rangle_a - 2\langle x \rangle_a \langle x \rangle_b + \langle x^2 \rangle_b \space \mp 2 \vert \int_{-\infty}^{\infty} \psi_a \psi_b^{*}xdx \vert^2
$$