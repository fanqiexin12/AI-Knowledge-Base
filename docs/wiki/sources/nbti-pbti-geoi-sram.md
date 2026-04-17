---
title: "Impacts of NBTI and PBTI on Ultra-Thin-Body GeOI 6T SRAM Cells"
type: source
tags: [nbti, pbti, geoi, sram, germanium, ultra-thin-body, reliability]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/Impacts_of_NBTI_and_PBTI_on_ultra-thin-body_GeOI_6T_SRAM_cells.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/pbti", "PBTI"], ["concepts/sram", "SRAM"]]
---

# Impacts of NBTI and PBTI on Ultra-Thin-Body GeOI 6T SRAM Cells

## Summary
本文研究了 **NBTI/PBTI 对 ultra-thin-body GeOI (Germanium-on-Insulator) 6T SRAM** 的影响。GeOI 的高载流子迁移率使其适合高性能应用，但其界面态密度高于 Si，BTI 效应更显著。

## Key Findings

### GeOI vs Si SRAM Comparison
| Parameter | GeOI | Si |
|-----------|------|-----|
| **Mobility (holes)** | ~4x higher | baseline |
| **Interface trap density (Dit)** | Higher | Lower |
| **NBTI sensitivity** | **More severe** | Less |
| **PBTI sensitivity** | **More severe** | Less |

### NBTI/PBTI Impact on 6T SRAM
- **NBTI** affects pull-up pMOSFETs (MP1, MP2)
- **PBTI** affects pull-down nMOSFETs (MN1, MN2)
- **Access transistor (MN3)** suffers from both NBTI + PBTI
- Result: **SNM (Static Noise Margin) degradation leads to failure at 10⁶s @ 125°C**

### Failure Mechanism
- NBTI → PMOS Vth ↑ → pull-up strength ↓ → SNM ↓
- PBTI → NMOS Vth ↑ → pull-down strength ↓ → SNM ↓
- Combined effect: SRAM cell fails faster than expected

### GeOI-Specific Concerns
- **Higher Dit** → more trap states at Ge/GeO₂ interface
- **Lower thermal budget** needed for GeOI process
- **Germanium oxide** is less stable than SiO₂

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/pbti]] — PBTI mechanism
- [[concepts/sram]] — SRAM cell structure

## Source
- [Impacts_of_NBTI_and_PBTI_on_ultra-thin-body_GeOI_6T_SRAM_cells.pdf](../../raw/sources/papers-onedrive/Impacts_of_NBTI_and_PBTI_on_ultra-thin-body_GeOI_6T_SRAM_cells.pdf)
