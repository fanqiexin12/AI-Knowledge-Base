---
title: "Fluorine Dose and Implant Energy Study on NBTI"
type: source
tags: [nbti, fluorine, implant, dose, energy, p-implant, mitigation]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/A_study_of_fluorine_dose_and_implant_energy_to_the_NBTI_upon_p_implant_sequence.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nbti-mitigation", "NBTI Mitigation"]]
---

# Fluorine Dose and Implant Energy Study on NBTI

## Source Info
- **Title**: A study of fluorine dose and implant energy to the NBTI upon p-implant sequence
- **Date**: 2026-04-16
- **Key topics**: F implant optimization, p-implant sequence, NBTI mitigation

## Key Findings

### Fluorine Incorporation for NBTI Reduction
- Fluorine (F) incorporation reduces NBTI degradation significantly
- F atoms passivate Si-H bonds at Si/SiO₂ interface, forming stronger Si-F bonds
- Si-F bond energy (~5.0 eV) > Si-H bond energy (~3.5 eV), more thermally stable

### Fluorine Dose Effects
| F Dose | NBTI Reduction | Impact on Drive Current |
|--------|---------------|------------------------|
| Low    | ~20-30%       | Negligible Id degradation |
| Medium | ~40-50%       | Slight Id reduction (~2-5%) |
| High   | >60%          | Significant Id degradation |

### P-implant Sequence Impact
- p-implant (Boron) process affects F retention in gate oxide
- **Optimal sequence**: F implant before p-implant preserves more F atoms
- P-implant after F can cause F atoms to be displaced from interface

### Optimal Process Window
- F dose: 5×10¹⁴ - 1×10¹⁵ cm⁻²
- F implant energy: 5-15 keV (optimized for interface region)
- Annealing temperature: 900-1000°C (rapid thermal anneal preferred)

### Trade-offs
- Higher F dose → better NBTI → more Id degradation
- Process integration complexity increases
- Need to balance reliability vs. performance

## Related
- [[concepts/nbti]] — NBTI concept page
- [[concepts/nbti-mitigation]] — NBTI mitigation techniques
