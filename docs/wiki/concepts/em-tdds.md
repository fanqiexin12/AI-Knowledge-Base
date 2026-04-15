---
title: "EM and TDDB"
type: concept
tags: [electromigration, em, tdds, copper, interconnect, reliability, breakdown, failure-mechanism]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Reliability_on_EUV_Interconnect_Technology_for_7nm_and_beyond.pdf", "raw/sources/Yield_and_Reliability_Challenges_at_7nm_and_Below.pdf"]
related: [["concepts/interconnect-reliability", "Interconnect Reliability"]]
---

# EM and TDDB

## Summary
**EM (Electromigration)** 和 **TDDB (Time Dependent Dielectric Breakdown)** 是先进制程节点互联可靠性的两大主要失效机制。EM 是电流驱动的金属原子迁移，TDDB 是介电层在高电场下的击穿。两者都在高电流密度和高电场下加速。

## Electromigration (EM)

### Mechanism
- **High current density J** → momentum transfer from electrons to metal atoms
- **Atom migration**：沿电子流方向
- **Viod formation**：原子迁移形成空洞
- **Resistance increase** → eventually open circuit

### Black's Equation
```
MTTF = A × J^(-n) × exp(E_a/kT)
```
- **n** ≈ 1.5-2 for Cu
- **E_a** ≈ 0.8-1.0 eV (grain boundary diffusion)

### EM in Advanced Nodes
- **7nm**: J > 10 MA/cm²
- **Via bottom interface** is the weakest point
- **Multiple patterning** creates new diffusion paths

## TDDB

### Mechanism
- **High electric field E** across dielectric
- **Trap generation**：空穴/电子陷阱累积
- **Percolation path** formation
- **Dielectric breakdown** → leakage → short

### E-model vs 1/E-model
| Model | Field dependence | Dominant at |
|-------|-----------------|-------------|
| **E-model** | MTTF ∝ exp(-γE) | High field |
| **1/E-model** | MTTF ∝ exp(+B/E) | Low field |

### EUV Impact
- **EUV resist残留**：碳/氢进入低k介质
- **LWR/LER**：局部电场集中

## Related
- [[concepts/interconnect-reliability]] — 互联可靠性
