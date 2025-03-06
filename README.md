# Self-Healing RD Simulation

## Introduction
This project simulates the healing process of cracks in a material using a diffusion-reaction model. The focus is on understanding how the concentration of a healing agent (**u_DA**) spreads across a material, the stress distribution (**σ**), and how the concentration influences the crack healing efficiency. The simulation includes factors like diffusion, adsorption, reaction, and stress, aiming to predict the efficiency of crack healing under different conditions.

## Features
- **Model Setup**: The simulation starts with the initialization of material properties such as the length (**L**), grid spacing (**dx**), maximum diffusion coefficient (**D_max**), reaction rate constant (**k_DA**), and temperature (**T**). Initial conditions for the healing agent (**u_DA**) and graphene concentration (**u_Graphene**) are also set.
  
- **Diffusion Coefficient**: The diffusion coefficient is modeled as a function of the concentration of the healing agent (**u**), with a dependency on its value.

- **Reaction Function**: The reaction function represents the decay of the healing agent concentration, with a threshold concentration that determines the healing effect.

- **Concentration Update**: The concentration of the healing agent and graphene is updated iteratively based on the diffusion, reaction, and adsorption processes. The update is governed by a finite difference method.

- **Stress Update**: The material's stress is updated at each time step, with the stress depending on the concentration of the healing agent and graphene. A strain is calculated at each position in the material.

- **Crack Closure Check**: The average concentration and stress in a defined crack region are monitored. If the average concentration exceeds a threshold, the crack is considered to be closed.

- **Simulation Loop**: The simulation runs for a set period (**T**), updating the concentrations and stress distributions at each time step. The progress of the crack healing is tracked by calculating the efficiency based on the concentration of the healing agent.

- **Sensitivity Analysis**: The model performs a sensitivity analysis to examine how varying parameters like the diffusion coefficient (**D**) and the reaction rate constant (**k**) affect the healing efficiency. The analysis is conducted over a range of values for these parameters, with temperature also taken into account.

## Results
After running the simulation, it is found that the healing efficiency reaches 100% when the average concentration exceeds the threshold for crack closure. Sensitivity analysis indicates that both the diffusion coefficient and the reaction rate constant significantly influence the healing efficiency, with higher values leading to faster healing. The simulation provides valuable insights into how the concentration of the healing agent influences crack healing in the material.
