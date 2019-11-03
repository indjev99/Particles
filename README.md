# Particles
Simulates particles of different randomly generated types.

Each particle type has a mass, radius and colour.

The radius of a particle follows this equation:

`Pi * radius^2 * density = mass` where `density` is some fixed particle density.

Each pair of particle types has an associated randomly generated interaction.

The interaction is a force with magnitude:

`4 * strength * ( (eqDist / r) - (eqDist / r) ^ 2 )` where `r` is their current distance.

The value `eqDist` determines the distance at which the two particles experience no force, while `strength` determines the maximum possible attraction. Notice that at a distance smaller than `eqDist` the particles repel each other and at a higher one they attract each other.

The particles evolve through time by interacting with each other and experiencing drag. The drag is also a force and follows this equation:

`F_D = dragCoeff * 2 * radius * velocity` (it is proportional to the area the particle covers in a unit of time)

Finally, for each particle we get its accelaration by dividing the total force by its mass.

The rules (other than the arbitrary nature of the particle interactions) are physically motivated and thus lead to the typicall 

These rules result in various clusters of particle lattices forming.

This project uses the GLFW library and OpenGL.
