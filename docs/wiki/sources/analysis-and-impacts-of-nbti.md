---
title: "Analysis and Impacts of NBTI"
type: source
tags: [nbti, circuit-impact, sram, ring-oscillator, sense-amplifier, reliability]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/Analysis_and_impacts_of_Negative_Bias_Temperature_Instability_NBTI.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/circuit-aging", "Circuit Aging"], ["concepts/sram", "SRAM"]]
---

# Analysis and Impacts of NBTI

## Source Info
- **Title**: Analysis and impacts of Negative Bias Temperature Instability (NBTI)
- **Date**: 2026-04-16
- **Key topics**: NBTI mechanism, circuit-level impacts, aging characterization

## Key Findings

### NBTI Mechanism Overview
- NBTI occurs in pMOSFETs under negative gate-to-source voltage (Vgs = Vdd) at elevated temperature
- Dominant degradation: **Vth increase** (positive threshold voltage shift), **mobility degradation**, **subthreshold swing increase**
- Two-stage model: interface trap (Nit) generation + oxide hole trapping
- Recovery effect: during relaxation phase, partial Vth recovery occurs

### Circuit-Level Impacts

#### SRAM
- NBTI causes read/write margin degradation in 6T SRAM cell
- Vth shift leads to **Static Noise Margin (SNM)** reduction
- Long-term reliability concern for cache memories

#### Ring Oscillator (RO)
- RO frequency decreases due to NBTI-induced Vth increase
- Can be used as **on-chip NBTI monitor**
- Frequency degradation ~2-5% after 10 years at operating conditions

#### Sense Amplifier
- **Offset voltage (Voffset)** increases with NBTI stress
- Sense amplifier sensitivity degrades over time
- Impacts read reliability in SRAM/NVM

### Aging Characterization
- NBTI + PBTI combined → overall transistor aging
- Process variability (Vt mismatch) accelerates aging-induced failures
- Circuit lifetime prediction requires comprehensive aging models

## Related
- [[concepts/nbti]] — NBTI concept page
- [[concepts/circuit-aging]] — Circuit aging effects
- [[concepts/sram]] — SRAM reliability
