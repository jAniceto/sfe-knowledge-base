# Peleg model

The Peleg model is an empirical model originally developed for water sorption/desorption kinetics, but it's been adapted for SFE to describe the extraction yield over time. 

The model describes cumulative extraction yield, $m$, as a function of time:

$$
m(t) = \frac{t}{K_1 + K_2 t}
$$

where $m$ is the cumulative yield at time $t$ ($\text{g}_\text{extract} / \text{g}_\text{dry material}$), $t$ is the extraction time, $K_1$ is the Peleg rate constant ($\text{time} \cdot \text{mass}^{-1}$) which governs the initial extraction rate, and $K_2$ is the Peleg capacity constant ($\text{mass}^{-1}$), which governs the equilibrium/asymptotic yield.

The initial extraction rate (as $t \rightarrow 0$) is given by:

$$
\left. \frac{dm}{dt} \right|_{t=0} = \frac{1}{K_1}
$$

A smaller $K_1$ means a faster initial rate, which is useful for comparing solvent power, temperature, or pressure conditions.

The equilibrium (maximum) yield (as $t \rightarrow \infty$) is given by:

$$
m_\infty = \frac{1}{K_2}
$$

and represents the asymptotic plateau, i.e. the theoretical maximum extractable mass under given conditions.

In the context of SFE of plant material the early extraction (steep rise) represents the washing of surface compounds due to fast mass transfer (free oil and surface extractables). The late extraction plateau represents the slow diffusion from cell matrix under pore resistance (bound/cellular oil).

Considering the effect of operating conditions on the model parameters:

- **Increasing pressure**: higher CO2 density $\rightarrow$ better solvent power $\rightarrow$ $K_1$ decreases and $K_2$ increases (faster rate, higher yield).

- **Increasing temperature**: two competing effects (vapor pressure and density) meaning non-monotonic behavior.

- **Particle size decreases**: shorter diffusion paths $\rightarrow$ $K_1$ decreases.

- **CO2 flow rate increases**: reduces external film resistance $\rightarrow$ affects $K_1$ more than $K_2$.