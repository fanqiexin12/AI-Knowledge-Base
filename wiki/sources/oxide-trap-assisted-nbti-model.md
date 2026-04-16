---
title: "New Oxide Trap-Assisted NBTI Degradation Model"
type: source
tags: [nbti, model, oxide-trap, degradation, physics]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/A_new_oxide_trap-assisted_NBTI_degradation_model.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nbti-frequency-effect", "NBTI Frequency Effect"]]
---

# New Oxide Trap-Assisted NBTI Degradation Model

## Source Info
- **Title**: A new oxide trap-assisted NBTI degradation model
- **Date**: 2026-04-16
- **Key topics**: Physical model, oxide trap, trap-assisted degradation

## Key Findings

### Oxide Trap Role in NBTI
- **Traditional view**: NBTI dominated by interface traps (Nit)
- **New finding**: Oxide traps (Not) in gate oxide also contribute significantly
- Oxide traps: pre-existing border traps + generated traps during stress

### Trap-Assisted Degradation Mechanism
1. Hole trapping in oxide traps during stress phase
2. Detrapping during relaxation (recovery)
3. Net degradation = trapping - detrapping balance
4. **Temperature acceleration**: higher T → faster trap generation

### Model Components

#### Oxide Trap Generation
```
ΔNot = A × exp(-Ea/kT) × t^n
```
- A: process-dependent prefactor
- Ea: activation energy (~0.1-0.3 eV)
- n: time exponent (0.1-0.3 for NBTI)

#### Time-Dependent Decay
- Oxide trap charging follows **stretched exponential** behavior
- Recovery time constant τ depends on trap energy depth

### Frequency Dependence Prediction
- Model correctly predicts frequency dependence of NBTI
- At high frequency: insufficient time for trap charging → lower degradation
- At DC: maximum trap occupation → maximum degradation

### Comparison with Two-Stage Model
| Feature | Two-Stage Model | Oxide Trap Model |
|---------|----------------|------------------|
| Interface traps | ✓ | ✓ |
| Oxide traps | ✗ | ✓ |
| Recovery | Exponential | Stretched exponential |
| Frequency effect | Qualitative | Quantitative |

## Related
- [[concepts/nbti]] — NBTI concept page
- [[concepts/nbti-frequency-effect]] — NBTI frequency effect
