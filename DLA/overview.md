## Diffusion limited aggregation
Coagulated aerosols are aggregates of solid particles, distinguished by their wispy appearance, these structures are unique as the size of these aggregates far exceeds the range of forces that hold them together. Shown to have density correlations of a power-law form, through the use of these power-law correlations, a simulation model can then be generated which demonstrates a discrete version of dendritic growth. This model can then be compared to other low-density object producing models, such as the Eden growth model. While the Eden model is primitive and unsuccessful in discribing the correlation between the aggregate density and distance. The diffusion limited aggregation model is also able to exhibit fractional power law behaviour of the correlation function.  

The generated model is based on the Eden model, whose initial state starts from a seed particle at the origin of a lattice. A second particle is then added randomly at a large distance from the origin. A random walk ensues by the second particle, until it visits a site adjacent to the seed, becoming a cluster. This is then repeated with other particles, consistently growing the aggregate. If a particle comes into contact with the boundaries of the lattce in its random walk, it is removed. 

![image](https://github.com/emaz2718/SM_and_MC_course/assets/151519476/d3693459-8c80-4a64-9697-1262d41b9e20)

Information about the particle distribution is then obtained from the density correlation function. The density is defined to be 1 for occupied sites and 0 otherwise. By measuring the correlation funcion, which would be dependent on the density and the distance between two sites:

$C(r)≡N^{-1}∑ρ(r')ρ(r'+r)$



## The Eden Model
This is the simplest model for the formation of aggregates. It describes how particles are added randomly one at a time to sites adjacent to the occupied sites. This process produces a compact cluster whose density correlations are independent of distance in the limit of large sizes. However, the metal aggregates were reported to have correlations that fall off as a fractional power of distance. 

## The approach of Forrest and Witten
The group of aggregates studied by Forest and Witter were shown to have density correlations of a power-law form. The aggreates were formed when a metal vapour of a heated plated filament was quench condensed.The metal particles condensed near the filament and diffused outwards. The particles coalesced into thin spherical shells which then drifted onto the microscopic slide. The aggregates on the slide were of the order of $10^{5}$ metal particles in a low-density mass. 

The coalescence of the particles into the aggregate structures was noted to be irreversible. Since they were observed to maintain their wispy shapes even after they wouls have moved through the gas.

### Fractals

Simple definition of fractal dimension. Examples Koch curve, Sirpinsky trianlgles etc...
Box counting algorithm and simple example.


## Colab tutorial

