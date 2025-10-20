# Mauve Intrusion: Quantifying Coherence in Coupled Chaotic Systems
**Author:** James Jones
**Affiliation:** Independent Researcher (IEEE Member)
**ORCID:** [0009-0002-6129-2847](https://orcid.org/0009-0002-6129-2847)  
**Paper:** _Mauve Intrusion: Quantifying Coherence in Coupled Chaotic Systems_ (arXiv: [TBD])

---

# Mauve Intrusion Framework

## Overview

This repository contains the rewritten version of the research paper "Mauve Intrusion: Quantifying Coherence in Coupled Chaotic Systems" (dated October 19, 2025), along with accompanying Python simulation and analysis scripts. The Mauve Intrusion (MI) framework introduces a quantitative metric for measuring paradoxical coherence in coupled chaotic systems, such as the Lorenz and Rössler attractors. The rewrite enhances the original framework by deriving local expansion (R), contraction (B), and neutral gradient (G) rates from the sorted real parts of Jacobian matrix eigenvalues, ensuring coordinate invariance and better alignment with rigorous chaos theory principles (e.g., tangent space dynamics and approximations to instantaneous Lyapunov exponents).

The MI metric is defined as:

$$ 
\text{MI}(t) = \frac{R \cdot B}{(R + B)^2} \exp\left(-\frac{G}{\sqrt{R \cdot B}}\right)
$$

Key features demonstrated include stable low-frequency rhythms (~0.16 Hz), weak entropy correlations (Pearson r ≈ 0.12), turbulence ratios (~4.5), partial entrainment (e.g., 25% amplitude variance reduction in the driven Rössler), and system-specific bleed dynamics (e.g., fractions ≈0.30 for Lorenz, ≈0.010 for Rössler).

This work bridges nonlinear dynamics and complexity science, with potential applications in neural networks, secure communications, and other far-from-equilibrium systems.

## Requirements

- Python 3.8+
- Libraries: `numpy`, `scipy`, `matplotlib` (install via `pip install numpy scipy matplotlib`)

No additional installations are needed, as the scripts use standard scientific computing tools.

## File Structure

- `mauve_intrusion.pdf`: Compiled PDF of the rewritten paper (generated from LaTeX).
- `simulation_script.py`: Main Python script for simulations, MI computation, analyses, and figure generation.
- `fig1.png` to `fig9.png`: Generated figures (after running the script).
- `README.md`: This file.

## Usage

1. **Run the Simulation Script**:
   - Execute `python simulation_script.py` to simulate the coupled Lorenz-Rössler systems, compute eigenvalue-based MI, perform analyses (e.g., entropy correlation, power spectrum, bleed metrics), and generate figures (fig1.png to fig9.png).
   - Key outputs in console:
     - Sensitivity analysis results (variances, correlations for varying k).
     - Cross-entrainment metrics (variance reduction, x-correlation).
     - Bleed metrics (mean MI and mixed FTLE fractions).
   - The script discards transients (first 100 units), uses dt=0.01, and simulates for T=1000 units.
   - Customize parameters (e.g., k=0.02 default) or extend to other systems by modifying ODE/Jacobian functions.

3. **Generated Figures**:
   - Fig 1: Lorenz trajectories.
   - Fig 2: MI vs. z phase map (Mauve Loops).
   - Fig 3: MI and Shannon entropy correlation.
   - Fig 4: MI power spectrum with turbulence ratio.
   - Fig 5: Modulated a(t) parameter.
   - Fig 6: Driven vs. uncoupled Rössler dynamics.
   - Fig 7: Phase-space density (Mauve Corridor).
   - Fig 8: Lorenz bleed plots (trajectories and MI).
   - Fig 9: Rössler bleed plots (trajectories and MI).

4. **Extending the Framework**:
   - Adapt `compute_mi` for other chaotic systems by providing custom ODE and Jacobian functions.
   - For neural applications (as suggested in the paper), replace Lorenz/Rössler with models like Hindmarsh-Rose.

## License

This project is licensed under the MIT License. See the LICENSE file for details (if added).

## Acknowledgments

Thanks to open-source communities for tools in nonlinear dynamics simulations. Full code and updates available at: https://github.com/noct-ml/mauve-intrusion

For questions, contact: noct-ml@pm.me

---

