# Mechanistic models

The governing equations that mathematically describe the supercritical fluid extraction (SFE) process in a packed bed consist of conservation equations for mass, momentum, energy, and species. In general, the energy and species conservation equations are only required when the process involves non-isothermal conditions (i.e., heat transfer effects) or when there is significant multicomponent transport and mixing.[@Banafi2023]


## General SFE mechanism

The mechanism of the supercritical fluid extraction can be described through the following sequential steps: 

1) Transport of supercritical fluid (SCF) molecules from the bulk phase to the solid surface across the external boundary layer surrounding the particle;

2) Diffusion of SCF molecules from the particle surface into the interior pore structure of the solid;

3) Desorption of the solute from the solid matrix and its dissolution into the SCF phase;

4) Transport of the resulting SCF-solute mixture from the particle interior to the particle surface; and 

5) Convective transport of the SCF-solute mixture from the particle surface back into the bulk fluid phase.

In step (3), extraction proceeds in two possible ways:

- via dissolution of the solute into the supercritical fluid (SCF) when no significant solid-solute interactions are present;

- when solid-solute interactions exist, mass transfer is governed primarily by desorption of the solute from the solid matrix prior to its transport into the SCF phase.


## Common model assumptions

The common simplifying assumptions employed in most of the SFE models include: 

- The whole solute is considered as one pseudo-component; 
- Particles are considered regularly shaped and single-sized;
- Constant physical properties of SCF and substrate; 
- Constant bed porosity and consequently, constant interstitial velocity of SCF inside the bed;
- Isothermal operation; and 
- Negligible pressure drop across the column.

With these assumptions, the number of equations required to describe the SFE process reduces to two mass conservation
equations in the form of partial differential equations (PDE): one for the fluid phase and one for the solid phase. Besides these equations, subsidiary thermodynamic and kinetic relations for predicting some parameters and solubility in the SFE
process modelling are also required.


## Mass balance equations

The general form of mass balance equations in both fluid and solid phases is presented below. They relate the solute concentration in solid phase ($C_\text{s}$) and fluid phase ($C_\text{f}$) with the axial position along the column ($z$), radial position in the particle ($r$), and time ($t$).

### Mass balance in fluid phase

$$
\frac{\partial C_\text{f}}{\partial t} + u_\text{i} \frac{\partial C_\text{f}}{\partial z} = D_\text{ax} \frac{\partial^2 C_\text{f}}{\partial z^2} + a_\text{p} \frac{1-\varepsilon}{\varepsilon} J
$$

where:

- $u_\text{i}$ is the interstitial velocity, 
- $D_\text{ax}$ is the is axial dispersion coefficient of solute in the SCF, 
- $a_\text{p}$ is the surface area to volume ratio of the particle (i.e., particle specific surface area), usually considered spherical thus $a_\text{p} = 3 / R_\text{p}$
- $R_\text{p}$ is the particle radius,
- $\varepsilon$ is hte bed porosity, and
- $J$ is the solute mass flux from solid to fluid.

The boundary conditions are:

$$
C_\text{f} = C_\text{f,0}, \quad \text{at } t = 0
$$

$$
D_\text{ax} \frac{\partial C_\text{f}}{\partial z} = u_\text{i} (C_\text{f} - C_\text{f,0}), \quad \text{at } z = 0
$$

$$
\frac{\partial C_\text{f}}{\partial z} = 0, \quad \text{at } z = L
$$

where:

- $C_\text{f,0}$ is the initial solute concentration in the fluid phase, and
- $L$ is the bed length.


### Mass balance in the solid phase

Let's now look at the mechanism of solute extraction and its mass transfer within the solid phase. Some models assume that particles consist of two distinct domains, the solid matrix and the pore space. Here, solute is distributed between the two regions and it is assumed that local equilibrium exists between the corresponding solute fractions. Solute release is driven by desorption from the solid matrix and subsequent dissolution into the supercritical fluid within the pores, after which the solute is transported to the particle surface via intraparticle pore diffusion.

$$
\varepsilon_\text{p} \frac{\partial C_\text{p}}{\partial t} + \left(1 - \varepsilon_\text{p}\right) \frac{\partial C_\text{s}}{\partial t} = \frac{D_\text{eff}}{r^2} \frac{\partial}{\partial r} \left(\varepsilon_\text{p} r^{2} \frac{\partial C_\text{p}}{\partial r}\right)
$$

where:

- $C_\text{p}$ is the solute concentrations in the pores,
- $C_\text{s}$ is the solute concentrations in the solid,
- $\varepsilon_\text{p}$ is the solid particle porosity,
- $D_\text{eff}$ is the effective diffusion coefficient in particle.

The associated initial and boundary conditions are:

$$
C_\text{p} = C_\text{p,0}, \quad \text{at } t = 0
$$

$$
C_\text{s} = C_\text{s,0}, \quad \text{at } t = 0
$$

$$
\frac{\partial C_\text{p}}{\partial r} = 0, \quad \text{at } r = 0
$$

$$
\frac{\partial C_\text{s}}{\partial r} = 0, \quad \text{at } r = 0
$$

$$
\varepsilon_\text{p} D_\text{eff} \frac{\partial C_\text{p}}{\partial r} = -J, \quad \text{at } r = R_\text{p}
$$

where $C_\text{s,0}$ and $C_\text{p,0}$ is the initial solute concentration in the in solid and pores, respectively.

The relation for the solute mass flux from solid to fluid ($J$) is:

$$
J = k_\text{f} \left( C_\text{p}|_{R_\text{p}} - C_\text{f} \right)
$$

where:

- $k_\text{f}$  is the solute mass transfer coefficient in fluid film adjacent to the solid particle, and 
- $C_\text{p}|_{R_\text{p}}$ is the solute concentration on the particle surface.

An equilibrium isotherm is also required:

$$
C_\text{s} = f_\text{isotherm}(C_\text{p})
$$


Different models have different simplifying assumptions as well as differences in the description of phase equilibrium, flow pattern, and the mechanism of solute mass transfer in solid phase.