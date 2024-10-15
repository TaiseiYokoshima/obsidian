To attempt at addressing the dynamic nature of LEO, we propose an approach utilizing the repetitive patterns: if the topology is restricted such that each satellite's local view is the same as that of any other. Then one can limit topology design to the space of all possible local views at just one satellite. This is called **motif**.

This motif is then repeated across all satellites, with each connected to its neighbors in the same way. Even for the densest proposed constellations, the space of possible motifs, while non-trivial, is small enough to search exhaustively and identify the optimal motif for a target traffic matrix. 

While this approach provides ~2x efficiency improvement over the neighbor-grid baseline, satellites are closer to each other at higher latitudes than at the Equator, implying a larger set of possibilities for ISLs. Therefore, motif limits the possible solutions to this problem by reducing the complexities.

Thus, motifs can be customized at different latitudes, providing improvements in network capacity. This enables efficiency improvements even when we make worst-case assumptions about the range of power-limited ISLs - for StarLink, with our approach, network performance would improve over the neighbor-grid by 37 percent even in the most pessimistic scenario. 

We show that our approach tackles the temporal variations inherent to LEO: ISLs based on motifs are maintained for long time, avoiding frequent, expensive link changes.

## Satellite Orbits and Constellations
Fully describing orbits requires 7 parameters, but all the constellations being proposed use fewer degrees of freedom, e.g. with only circular orbits (with the same apogee and perigee), so we offer the below simplified description:

Inclination is the angle between an orbit and the Equator as the satellite travels northward. For polar orbits, the inclination is 90 degrees. Orbits with lower inclinations do not travel over the poles, spending more time at lower latitudes. For both polar and non-polar orbits, the density of satellites increases away from the equator, simply due to the involved geometry. This has important consequences for our design. 

Altitude of a satellite is measured over sea level, and determines its orbital velocity. LEO completes orbit in less than 100 minutes. 

Phase shifts capture the relative placement of satellites in a constellation. Successive orbital planes cross the Equator at different points; see e.g., the orbits in Fig. 1. if phase shifted uniformly, 30 orbital planes would have separation of 12 between successive planes. Each orbital plane can carry many satellites, e.g., the. 

## System Dynamics


