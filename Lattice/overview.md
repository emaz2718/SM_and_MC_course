# Lattice models

## lattice

In three dimensions, a lattice can be defined as a regular arrangement of points in three-dimensional space, where each point has identical surroundings and the arrangement repeats itself periodically in all directions. More formally, a lattice in three dimensions can be defined as a set of points of the form $\vec{r} = n_1\vec{a}_1 + n_2\vec{a}_2 + n_3\vec{a}_3$, where $\vec{a}_1$, $\vec{a}_2$, and $\vec{a}_3$ are three linearly independent vectors called the lattice vectors, and $n_1$, $n_2$, and $n_3$ are integers.

The lattice vectors $\vec{a}_1$, $\vec{a}_2$, and $\vec{a}_3$ are chosen such that they form a parallelepiped that contains all the lattice points. This parallelepiped is called the unit cell of the lattice, and it represents the repeating pattern of the lattice.


![Lattice](lattice.png)

The figure illustrates a 2d lattice with the unit cell marked out.

There are many types of lattices in three dimensions, each with different symmetry properties. Some common examples include the simple cubic lattice, the face-centered cubic lattice, and the body-centered cubic lattice. The simple cubic lattice is the most basic type of lattice, where each lattice point is at the corner of a cube. The face-centered cubic lattice has additional lattice points at the center of each face of the cube, while the body-centered cubic lattice has an additional lattice point at the center of the cube.


IMPORTANT #1: For systems with disorder (e.g gas and liquids) we make use of a "super lattice" contaning a large number of sites. The repeating unit can be threrfore be very large!

IMPORTANT #2: Neighbors (especially nearest neieghbors = NN ) are important in lattice models. We should explain the concept of periodic boundary conditions here and illustrate this concept in terms of which lattice site are connected (NN).


## Ideal Lattice Gas

The ideal lattice gas model is a simplified representation of a gas system in statistical mechanics. It provides a theoretical framework for studying the behavior of non-interacting particles in a lattice structure. This model serves as a fundamental reference for understanding the properties of real gases under certain conditions.

During the process of adsorption, the gas binds to the surface of the solid through various intermolecular interractions. If these are weak van der waals then physical adsorption is present, if these are strong covalent bonds then we have chemical adsorption. When building the adsorption model of an ideal lattice gas, we are gonna consider the surface of the lattice as having M sites, which will be occupied by N molecules. There are two assumptions that we are going to keep in mind:
(i) The sites M are equivalent and independent 
(ii) There is a maximum of one molecule bonded per site 

So, the partition function for an adsorbed molecule would then be:

$q(T) = q_{x} q_{y} q_{z} e^{-(U_{00}/kT)}$

where q_{X}, q_{y}, and q_{z} are the 1-dimenional harmonic oscillator-type partition functions. Considering that during the process of adsorption the free gas is in equilibrium with the adsorbed molecules. The same zero-level energy for the molecules in the gas and adsorbed state must be present. Hence, let U=0 correspond to the gas molecule at rest for z→∞, then U_{OO} would be the energy at the minimum of U_{O}(x,y). Which would therefore be the potential energy of the adsorbed molecules at 0K, meaning that U_{OO}<0.

Therefore for the two possible situations of :

N = M
$Q(N,M,T) = q(T)^{N}$                                                        ...equation (i)

N ≤ M 
$Q(N,M,T) = (M    N) q(T)^{N}$                                                ...equation(ii)

Where (M N) is a 2*1 matrix representing the number of possible ways that the N indistinguishable molecules can be distributed on the M distinguishable sites. Therefore taking the logarithmic function of the equation (ii) we can have:

$lnQ = MlnM - M - (NlnN - N) - [(M - N)ln(M - N)-(M - N)] + Nlnq$
$lnQ = MlnM - NlnN - (M - N)ln(M - N) + Nlnq$                               ...equation(iii)


### Configurational entropy of an ideal lattice gas

The total entropy has two contributions: $S = S_{config} + S_{vib}$. Which can be seen by combining the general entropy equation $S = U/T = klnQ$ to the previously derived equation (iii). 
Hence, the combinatorial term will be: 

$S_{config} = kln(M   N)$

$S_{config} = k(MlnM - M - (NlnN - N) - [(M - N)ln(M - N) - (M - N)])$
$S_{config} = l(MlnM - NlnN - (M - N)ln(M - N))$

The interaction term will be:

$S_{vib} = Nk(lnq + T(dlnq/dT)$

### Chemical potential


## Interacting Lattice Gas with Nearest-Neighbor Interactions

In the context of statistical mechanics, an interacting lattice gas refers to a model where N particles adhered to M sites of a lattice experience interactions, specifically nearest-neighbor interactions. The energy associated with these interactions is denoted as $w$. The model is once again a one-dimensional lattice gas, so the criteria of equation (ii) can be applied, whereby N≤M. So, denoting the filled sites of the lattice as "1" and the empty sites as "0", for the following exemplary lattice surface adsorption:

1 1 1 0 0 1 0 1 0 0 1 1 0 

We would have a total of 13 sites, M=13, occupied by 7 molecules, N=7. Additionally, we have the following nearest-neighbour interractions:

![image](https://github.com/emaz2718/SM_and_MC_course/assets/151519476/c7ebbc20-d615-448f-a583-08fbaeda6626)

Therefore, ignoring boundary effects in general we would then have:

$2N = 2N_{11} + N_{01}$

$2(M-N) = 2N_{00} + N_{01}$

As can be noted, we have three unknown variables N_{11}, N_{00} and N_{01}. Therefore, making N_{01} an independent variable, we can derive the total interaction energy;

$2N = 2N_{11} + N_{01}$

$2N_{11} = 2N - N_{01}$

$N_{11} = N - (N_{01}/2)$

$(N_{11})w = (N - (N_{01}/2))w$

If g(N,M,N_{01}) is the number of configurations with N_{01} pairs for a given (N,M), the Canonical partition function for the one dimensional lattice gas can be written as:

$Q(N,M,T) = q^{N}Σg(N,M,N_{01})e^{-(N-N_{01}/2)w/kT}$
$Q(N,M,T) = (qe^{-w/kT})^{N}Σg(N,M,N_{01})(e^{w/2kT)^{N_{01}$

where the Σ is over all possible values of N_{01} for given (N,M). 

### Mixture

A lattice fully populated with two types os species A and B. 

### Bragg-Williams approximation (Mean-field approximation)
The Bragg-Williams approximation is a mean-field theory approach. It arises by randomly distributing the molecules over the sites (as if w=0) and then counting the average number of interaction, therefore the N_{11} terms. 

$Q(N,M,T) = (M  N) q^{N} e^{-N_{11-average}w/kT}                                 ....equation (iv)

Where N_{11-average} is the average number of 11 interractions and N_{11-average}w is the average interaction energy.
For a lattice with c neighbour sites, the average occupied sites of a molecule would be $cθ = cN/M$. (Considering that $θ = N/M$). The average number of 11 interractions would then be:

$N_{11-average} = c(N/M)(N/2) = cN^{2}/2M$                                     ...equation(v)

Taking logarithyms of equation (iv) and substituting in equation (v):

$lnQ = MlnM - NlnN - (M - N)ln(M - N) + Nlnq - cN^{2}w/2MkT$




