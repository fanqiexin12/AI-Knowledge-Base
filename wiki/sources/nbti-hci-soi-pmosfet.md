---
title: "NBTI and Concurrent HCI-NBTI Degradation of 65nm SOI pMOSFETs"
type: source
tags: [nbti, hci, soi, pmosfet, 65nm, degradation, reliability, concurrent]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/NBTI_and_Concurrent_HCI-NBTI_Degradation_of_65_nm_SOI_PMOSFETs.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/hci", "HCI"], ["concepts/soi-mosfet", "SOI MOSFET"]]
---

# NBTI and Concurrent HCI-NBTI Degradation of 65nm SOI pMOSFETs

## Summary
本文研究了 **65nm SOI pMOSFET** 中 NBTI 和 **HCI-NBTI 复合退化** 的相互作用。PD-SOI 中 HCI 和 NBTI 同时存在时，退化量大于单独机制之和。

## Key Findings

### Concurrent Degradation
- **Pure NBTI**：Vgs < 0, Vds = 0
- **Concurrent HCI-NBTI**：Vgs < 0, Vds < 0 (high drain bias)
- **复合效应**：总退化 > NBTI + HCI 单独之和

### SOI-Specific Issues
| Effect | Description |
|--------|-------------|
| **Floating body** | Amplifies HCI via body charging |
| **Self-heating** | Accelerates both NBTI and HCI |
| **History effect** | Prior stress state affects current degradation |

### Key Data (65nm PD-SOI)
- **Pure NBTI ΔVth**：~40mV @ 10⁵s
- **Concurrent HCI-NBTI ΔVth**：~60-70mV @ 10⁵s
- **Synergistic factor**：1.3-1.5x

### Mechanism
```
High Vds stress
    ↓
Impact ionization → e-h pair generation
    ↓
Holes collected by body → Body potential ↑
    ↓
Reduced barrier for hole injection → Enhanced NBTI
    ↓
Synergistic degradation
```

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/hci]] — HCI mechanism
- [[concepts/soi-mosfet]] — SOI MOSFET features

## Source
- [NBTI_and_Concurrent_HCI-NBTI_Degradation_of_65_nm_SOI_PMOSFETs.pdf](../../raw/sources/papers-onedrive/NBTI_and_Concurrent_HCI-N