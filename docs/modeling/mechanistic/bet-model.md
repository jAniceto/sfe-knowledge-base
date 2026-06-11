# BET model

The BET model was proposed by Pardo-Castaño et al. and is based on the Brunauer-Emmett-Teller (BET) theory of adsorption.[@PardoCastano2015]


## Derivation

The BET model neglects the axial dispersion and solute accumulation in fluid phase compared to the amount of solute in solid phase, and the mass balance equation in fluid phase and association relations are:

$$
u_\text{i}  \frac{\partial y_\text{f}}{\partial z} = a_\text{p} \frac{1-\varepsilon}{\varepsilon} J
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
- $y_\text{f}$ and $y_\text{f}^*$ are solute mass fractions in fluid phase and in fluid film adjacent to the particle surface which is in equilibrium with solid surface, respectively, 
- $y_\text{f,L}$ is also solute mass fraction in fluid phase at the outlet of the extractor, and 
- $J$ is the solute mass flux from solid to fluid.

The equation can be integrated analytically to find the solute mass fraction in fluid phase at the extractor exit:

$$
y_\text{f,L} = y_\text{f}^* \left[ 1 - \exp \left( - \frac{(1-\varepsilon) a_\text{p} k_\text{f} L}{\varepsilon u} \right) \right]
$$


To obtain the solute mass balance in solid phase, it is assumed that the mass of extracted solute in fluid phase at the extractor outlet is negligible in comparison with the total mass of solute and SCF. Thus, the solute mass balance in solid phase can be written as:

$$
\frac{d x_\text{s}}{d t} = - \frac{\dot{m}_\text{f}}{m_{0}} y_{\text{f,L}} = - \frac{\dot{m}_\text{f}}{m_{0}} y_\text{f}^* \left[ 1 - \exp \left( - \frac{(1-\varepsilon) a_\text{p} k_\text{f} L}{\varepsilon u} \right) \right]
$$

where $x_{s}$ is solute mass fraction in solid phase. $\dot{m}_{f}$ and $m_{0}$ denote the supercritical solvent flow rate and initial mass of extractable solute, respectively.

The solute interaction with solid matrix is given by the BET-type equilibrium equation:

$$
\frac{x_{s}}{x_{m}} = \frac{K \mathcal{X}}{[1-\mathcal{X}] [1+(K-1) \mathcal{X}]}
$$

$$
\mathcal{X} = \frac{y_\text{f}}{y_\text{sat}}
$$

where $K$ represent the sorption equilibrium coefficient, $y_\text{sat}$ and and $x_{m}$ are the mass fractions of solute in the saturated fluid phase and the first monolayer, respectively. 

$y_\text{f}^*$ is solved analytically and substituted into the $\frac{d x_{s}}{d t}$ equation above to calculate the extraction yield as a function of time with three adjustable parameters, through analytical integration using the initial condition at $t = 0$, $x_{s} = 1$.  


## Integrated final model

The model can be analytically integrated using the initial condition: $t = 0, $x_{s} = 1$:

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