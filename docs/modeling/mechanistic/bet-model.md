# BET model

The BET model was proposed by Pardo-Castaño et al. and is based on the Brunauer-Emmett-Teller (BET) theory of adsorption.[@PardoCastano2015]


## Mass balance in the fluid

The BET model starts from the mass balance to the fluid phase shown in [Mechanistic models](index.md) but makes two simplifications:

- Neglects axial dispersion. This approximation is valid when $L > 50 R_\text{p}$ and $\text{Re} > 10$;

- Considers that solute accumulation in fluid phase can be neglected when compared to the amount of solute in solid. 

Hence, the mass balance to the fluid phase becomes:

$$
u_\text{i} \frac{\partial C_\text{f}}{\partial z} =  a_\text{p} \frac{1-\varepsilon}{\varepsilon} J
$$


$$
J = k_\text{f} (y_\text{f}^* - y_\text{f})
$$

$$
y_\text{f} = 0 \quad \text{at} \quad z = 0
$$

$$
y_\text{f} = y_\text{f,L} \quad \text{at} \quad z = L
$$

where 

- $u_\text{i}$ is interstitial velocity, 
- $\varepsilon$ is the bed porosity, 
- $a_\text{p}$ denotes the surface area to volume ratio (i.e., particle specific surface area); in most cases solid particles are considered as spheres and thus $a_\text{p} = 3 / R_\text{p}$, where $R_\text{p}$ is the radius of the particle,
- $y_\text{f}$ is the solute mass fraction in the fluid phase,
- $y_\text{f}^*$ is the solute mass fraction in the fluid film adjacent to the particle surface which is in equilibrium with solid surface, respectively, 
- $y_\text{f,L}$ is also solute mass fraction in fluid phase at the outlet of the extractor, and 
- $J$ is the solute mass flux from solid to fluid.

The equation can be integrated analytically from: 

$$
z = 0: \quad y_\text{f} = 0
$$

$$
z = L: \quad y_\text{f} = y_\text{f,L} 
$$

to find the solute mass fraction in fluid phase at the extractor exit:

$$
y_\text{f,L} = y_\text{f}^* \left[ 1 - \exp \left( - \frac{(1-\varepsilon) a_\text{p} k_\text{f} L}{\varepsilon u} \right) \right]
$$

## Mass balance in the solid

To obtain the solute mass balance in solid phase, it is assumed that the mass of extracted solute in fluid phase at the extractor outlet is negligible in comparison with the total mass of solute and SCF. Thus, the solute mass balance in solid phase can be written as:

$$
\frac{d x_\text{s}}{d t} = - \frac{\dot{m}_\text{f}}{m_{0}} y_{\text{f,L}} \Rightarrow
$$

$$
\Rightarrow \frac{d x_\text{s}}{d t} = - \frac{\dot{m}_\text{f}}{m_{0}} y_\text{f}^* \left[ 1 - \exp \left( - \frac{(1-\varepsilon) a_\text{p} k_\text{f} L}{\varepsilon u} \right) \right]
$$

where 

- $x_{s}$ is solute mass fraction in solid phase,  
- $\dot{m}_{f}$ is the supercritical solvent flow rate, and 
- $m_{0}$ is the initial mass of extractable solute.


## BET equilibrium

The solute interaction with solid matrix is given by the BET-type equilibrium equation:

$$
\frac{x_{s}}{x_{m}} = \frac{K \mathcal{X}}{[1-\mathcal{X}] [1+(K-1) \mathcal{X}]}
$$

$$
\mathcal{X} = \frac{y_\text{f}}{y_\text{sat}}
$$

where 

- $K$ is the sorption equilibrium coefficient, 
- $y_\text{sat}$ is the mass fractions of solute in the saturated fluid phase, and 
- $x_{m}$ is the mass fractions of solute in the first monolayer. 

$y_\text{f}^*$ is solved analytically and substituted into the solid mass balance equation above to calculate the extraction yield as a function of time with three adjustable parameters.  


## Integrated final model

The model can be analytically integrated using the initial condition: $t = 0$, $x_{s} = 1$

$$
t = \frac{m_0}{2 \ \dot{m}_\text{f} \ y^*} \left( x_0' - x' + (2 - K) \left[ x - x_\text{m} \ln \left( \frac{\alpha}{\beta} \right) \right] + K x_\text{m} \ln \left[ \frac{\alpha'}{\beta' (1-x)^2} \right] \right)
$$

$$
x_0' = \sqrt{a + b + c}
$$

$$
x' = \sqrt{a (1-x)^2 + b (1-x) + c}
$$

$$
a = K^2
$$

$$
b = 2 (2-K) K x_\text{m}
$$

$$
c = (K x_\text{m})^2
$$

$$
\alpha = x' + K (1 - x) + (2-K) x_\text{m}
$$

$$
\alpha' = x' + (2-K)(1-x) + K x_\text{m}
$$

$$
\beta = x_0' + K + (2-K) x_\text{m}
$$

$$
\beta' = x_0' + (2-K) + K x_\text{m}
$$

$$
y^* = y_\text{sat} \left[ 1 - \exp \left( -\frac{k L}{u_\text{i} \varepsilon} \right) \right]
$$

where $x$ is the extraction yield (ratio between the mass of solute extracted at time $t$, and the mass of solute initially present in the packed bed that can be extracted).

This equation expresses a relationship between time and extraction yield, and has three adjustable parameters: $y^*$, $K$, and $x_\text{m}$ which have physical meaning: 

- $y^*$ is related to the solubility of the solute in the SCF corrected by diffusional limitations; 
- $K$ is the ratio between the adsorption equilibrium constant of the solute in the first monolayer and that in subsequent layers (when the solute-solid interactions are strong, $K \rightarrow \infty$, and when they are weak, $K \rightarrow 0$); and 
- $x_\text{m}$ is the ratio between the mass of solute present in the first monolayer and the initial mass of solute that can be extracted.
