---
title: "Optimum Fin Width Guideline for HC and NBTI in MuGFETs"
type: source
tags: [nbti, hci, mugfet, finfet, fin-width, reliability, multigate]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/A_Guideline_for_the_Optimum_Fin_Width_Considering_Hot-Carrier_and_NBTI_Degradation_in_MuGFETs.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/hci", "HCI"], ["concepts/finfet", "FinFET"]]
---

# Optimum Fin Width Guideline for HC and NBTI in MuGFETs

## Source Info
- **Title**: A Guideline for the Optimum Fin Width Considering Hot-Carrier and NBTI Degradation in MuGFETs
- **Date**: 2026-04-16
- **Key topics**: Multi-gate FET, Fin width optimization, HC/NBTI tradeoff

## Key Findings

### MuGFET (Multi-Gate FET) Overview
- MuGFET includes FinFET, GAA (Gate-All-Around), nanowire FETs
- 3D structure provides better electrostatics than planar
- Fin width (Wfin) is critical design parameter for reliability

### Fin Width Effects on Reliability

#### Narrow Fin (Wfin < 10nm)
- **HCI is severe**: high lateral electric field at drain edge
- Channel is fully depleted, but velocity overshoot increases hot carrier generation
- Good for short-channel control, bad for HCI

#### Wide Fin (Wfin > 20nm)
- **NBTI dominates**: volume fraction of channel near interface is smaller
- More relaxed electric field → less HCI
- But gate control degrades → worse SCE (short-channel effects)

#### Optimal Fin Width: 10-15nm
- Best tradeoff between HCI and NBTI
- Balances channel volume (NBTI sensitivity) and peak field (HCI)

### HCI vs NBTI Tradeoff

| Fin Width | NBTI | HCI | Dominant |
|-----------|------|-----|----------|
| Narrow (<10nm) | Low | High | HCI |
| Medium (10-15nm) | Medium | Medium | Balanced |
| Wide (>20nm) | High | Low | NBTI |

### MuGFET-specific Considerations
- Multiple fins: device-level variability between fins
- Fin-to-fin uniformity critical for consistent reliability
- Process optimization: uniform fin width across wafer

## Related
- [[concepts/nbti]] — NBTI concept page
- [[concepts/hci]] — Hot carrier injection
- [[concepts/finfet]] — FinFET reliability
