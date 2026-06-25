---
layout: page
permalink: /research/
title: research
description: 
nav: true
nav_order: 1
---

My work spans experimental evaluation of materials in extreme environments,
physics-based modelling of damage and failure, and machine-learning methods for
prediction and inverse characterization. The main areas:

- **Cryogenic and hydrogen materials evaluation** — mechanical and fracture-toughness testing of metals at 20 K and under hydrogen, for liquid-hydrogen service.
- **Measurement accuracy and standardization** — operator-independent property determination and contributions to material test standards.
- **Computational damage mechanics** — stress-state-dependent ductile-damage and fracture models implemented as finite-element subroutines.
- **Machine learning for solid mechanics** — neural networks for inverse material characterization, constitutive modelling, and full-field surrogate simulation.

---

## Cryogenic Material Testing

{% include figure.liquid loading="eager" path="assets/img/research/cryo_machine.png" class="img-fluid rounded z-depth-1" %}

- Built and operated an integrated liquid-hydrogen test capability: a 20 K tensile and fatigue testing machine with a helium re-liquefaction loop, one of the few such capabilities in Korea.
- Addressed the practical measurement issues of 20 K testing: extensometer and clip-on gauge calibration, helium leakage, thermal shrinkage, and specimen sizing.
- Evaluated austenitic stainless steels (304L, 316L), aluminum alloys, and nickel alloys across temperature (room temperature, 110 K, 77 K, 20 K) and hydrogen-charging conditions.

{% include figure.liquid path="assets/img/research/cryo_fracture.png" class="img-fluid rounded z-depth-1" %}

- Measured tensile and J-resistance fracture toughness at 20 K, comparing the unloading-compliance and normalization methods with crack-length correction.

**Open issues being studied**

- Coolant environment: gaseous helium versus liquid hydrogen at 20 K. Serrated yielding seen in helium is largely absent in liquid hydrogen, attributed to the higher specific heat of the liquid; the test environment itself can affect the measured behaviour.
- Indirect toughness assurance from 77 K to 20 K. ASME BPVC permits sub-77 K service from 77 K Charpy data alone, but NASA and NIST studies show poor correlation with the 20 K fracture toughness, so direct 20 K evidence is needed.

---

## Hydrogen-Environment Materials Testing

{% include figure.liquid path="assets/img/research/hydrogen.png" class="img-fluid rounded z-depth-1" %}

- Electrochemical hydrogen charging at elevated temperature (heating mantle with reflux condenser) to reach much higher pre-charged hydrogen than room-temperature charging, with charging conditions set from diffusion theory rather than empirically.
- High-temperature, high-pressure gaseous hydrogen testing for hydrogen-engine components, using an in-situ autoclave with direct-current potential drop crack monitoring (about 10 MPa, 300 °C).
- Related the change in fracture mode from dimple-dominated to quasi-cleavage to the absorbed hydrogen.

{% include figure.liquid path="assets/img/research/hydrogen_design.png" class="img-fluid rounded z-depth-1" %}

- Designed gaseous-charging conditions with a validated hydrogen-diffusion model (San Marchi recommended properties for 304/316, with Abel–Noble and fugacity corrections for real-gas behaviour).
- Computed the time to reach 90 % core saturation as a function of charging temperature and specimen size (for example, about 17 days at 200 °C for a 2 mm radius, and a few days at 300 °C), and the surface saturation concentration from Sieverts' law.
- Predicted the residual hydrogen content and through-thickness profile of tensile and compact-tension specimens after charging and air cooling, accounting for geometry differences between the gauge and grip sections.

---

## Measurement Accuracy and Operator-Independent Evaluation

{% include figure.liquid path="assets/img/research/measurement.png" class="img-fluid rounded z-depth-1" %}

- Automated, operator-independent determination of mechanical properties to remove subjective judgement: elastic-modulus slope determination based on ASTM E3076 and compliance evaluation based on ASTM E1820 Annex X3.
- Custom jig and procedure for calibrating the extensometer and crack-opening-displacement gauge at 20 K.
- Corrected the apparent reduction of crack length in J-resistance testing of high-toughness 316L, identifying under-estimated specimen rotation as the cause through telecentric imaging of the crack front; this matches a current topic at NIST.

---

## Computational Damage Mechanics and Ductile Fracture

{% include figure.liquid path="assets/img/research/damage.png" class="img-fluid rounded z-depth-1" %}

- Ductile-failure prediction with a user-defined material (UMAT) subroutine and a three-dimensional fracture locus, taking material fracture as the design criterion for containment structures.
- Workflow from specimens of varying stress state: flow-stress calculation in the necking region, damage-initiation determination against force–displacement data, and calibration of the fracture locus.

{% include figure.liquid path="assets/img/research/damage_evo.png" class="img-fluid rounded z-depth-1" %}

- Stress-state-dependent damage formulated through stress triaxiality and the normalized Lode angle, with the evolution law derived from a dissipation potential.
- Unloading–reloading tensile tests to identify damage evolution, including a single-step method for measuring the elastic modulus.
- Predicts the necking response and crack initiation and direction of 304L stainless steel that commercial codes do not capture.

*Related work: International Journal of Solids and Structures 318, 113439 (2025); Metals (2022); Journal of Constructional Steel Research (2019).*

---

## Machine Learning for Material Characterization and Constitutive Modelling

{% include figure.liquid path="assets/img/research/ml_indentation.png" class="img-fluid rounded z-depth-1" %}

- Neural networks that recover constitutive parameters (elastic modulus, yield strength, and hardening parameters) from a single spherical-indentation load–depth curve together with the residual surface imprint.
- An extension that recovers the in-plane residual stress at the same time, separating two effects that classical indentation analysis cannot tell apart.
- A way to measure properties where standard specimens are not available, such as miniature samples or extreme-environment conditions.

{% include figure.liquid path="assets/img/research/constitutive_nn.png" class="img-fluid rounded z-depth-1" %}

- A neural-network-integrated elastoplastic constitutive model for J2 plasticity that predicts the updated stress, trial yield function, and plastic multiplier from the trial-state stress and the current equivalent plastic strain.
- The stress state is expressed in Haigh–Westergaard coordinates, which reduces the number of inputs and eases the out-of-distribution problem.
- This gives 39 to 48 percent better accuracy than a principal-stress formulation, with stronger extrapolation; training data are generated in Python from stress invariants without commercial finite-element software.

*Related work: Journal of Applied Mechanics 93(3), 031008 (2026); International Journal of Pressure Vessels and Piping, under review (2026); Engineering Science and Technology, an International Journal 69, 102104 (2025).*

---

## Graph-Neural-Network Surrogates for Transient Multi-Physics

{% include figure.liquid path="assets/img/research/gnn.png" class="img-fluid rounded z-depth-1" %}

- A label-free graph-neural-network surrogate for moving-heat-source problems, supervised by the weak form of the governing heat equation and trained by rollout, so that pre-computed simulation datasets are not required.
- Online sampling of randomized conditions through Gaussian-random-field augmentation, covering moving heat sources representative of welding, line heating, and additive manufacturing.
- On a domain ten times larger than the training domain, the surrogate predicted about 11,000 time steps with under 1 percent relative error while running roughly 200 times faster than the finite-element solver.
- The longer-term aim is to invert these physics-constrained surrogates, recovering material properties or process parameters from limited full-field measurements such as infrared or digital-image-correlation data.

*Related work: manuscript in preparation (2026).*

---

## Standards and Regulation Contributions

{% include figure.liquid path="assets/img/research/standards.png" class="img-fluid rounded z-depth-1" %}

- Material-compatibility input to Korea's interim guidelines for ship hydrogen fuel-cell systems and to the IMO review of high-manganese-steel ammonia compatibility testing.
- Material selection and test-procedure guidelines for hydrogen-fuelled and liquid-hydrogen ships, developed with the Korean Register.
- Technical guidebooks for the shipbuilding industry on metallic-material selection, liquid-hydrogen compatibility, and cryogenic insulation evaluation.

---

## Cryogenic Insulation and Autonomous Ship Systems

{% include figure.liquid path="assets/img/research/insulation_mass.png" class="img-fluid rounded z-depth-1" %}

- Advanced polyurethane-foam insulation with improved mechanical strength and thermal performance, evaluated against manufacturing conditions such as additive type, weight ratio, and density.
- Impact-resistance evaluation of LNG insulation panels under repetitive loading and cryogenic-to-ambient temperature gradients, including a registered patent and guidance for reinforced-foam assessment under sloshing loads.
- Maritime autonomous surface ship systems, including an automated mooring system (rubber-seal selection and vacuum suction-pad design) and an automated hull-inspection robot.
