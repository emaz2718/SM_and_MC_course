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

Partion function and ln(Q)


### Configurational entropy of an ideal lattice gas

Can we find an expression in terms of the fraction of occupied sites? 

### Chemical potential


## Interacting Lattice Gas with Nearest-Neighbor Interactions

In the context of statistical mechanics, an interacting lattice gas refers to a model where particles on a lattice experience interactions, specifically nearest-neighbor interactions. The energy associated with these interactions is denoted as $w$.



### Mixture

A lattice fully populated with two types os species A and B. 

### Bragg-Williams approximation (Mean-field approximation)

Can we derive the partion function using Christer Elvingssons notes and compute some thermodynamical quantity that we can later compare to an explicit Monte-Carlo simulation? Can we make a supersimple python tutorial? 
