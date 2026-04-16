---
title: "Assessment of NBTI in Presence of Self-Heating in High-k SOI FinFETs"
type: source
tags: [nbti, finfet, soi-mosfet, self-heating, high-k, reliability]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/Assessment_of_NBTI_in_Presence_of_Self-Heating_in_High-_k_SOI_FinFETs.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/finfet", "FinFET"], ["concepts/soi-mosfet", "SOI MOSFET"]]
---

# Assessment of NBTI in Presence of Self-Heating in High-k SOI FinFETs

## Summary
本文评估了 **High-k SOI FinFET** 中 **自加热效应（Self-Heating）** 对 **NBTI** 降解的影响。SOI 结构的热隔离特性导致热量难以散去，与 High-k 栅介质的 NBTI 效应产生相互作用。

## Key Findings

### Self-Heating Effect (SHE)
- SOI FinFET 的 **Buried Oxide (BOX)** 层热导率低
- 器件运行时产生的热量积聚在沟道区域
- 温度升高加速 NBTI 降解动力学

### NBTI + Self-Heating Interaction
| Effect | Mechanism |
|--------|-----------|
| **温度升高** | SHE 提高沟道温度 → NBTI 加速 |
| **热激活** | Arrhenius 关系：温度每升高 10°C，降解速率翻倍 |
| **恢复受限** | 高温同时加速 recovery，但也加剧 stress |

### High-k Dielectric Impact
- High-k (HfO₂) 与 SiO₂ 相比，NBTI 机制不同
- **氧化层陷阱（oxide traps）** 贡献更显著
- 等效氧化层厚度（EOT）缩小时，NBTI 更敏感

### Key Data
- 90nm PD-SOI FinFET 测试
- 自加热导致局部温度升高 20-40°C
- NBTI 降解加速 ~2x at high power states

## Mechanism
```
Power dissipation → Lattice heating → Elevated T
    ↓
NBTI acceleration (Arrhenius: T↑ → k↑)
    ↓
Vth shift increases, recovery complicated
```

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/finfet]] — FinFET structure
- [[concepts/soi-mosfet]] — SOI MOSFET self-heating

## Source
- [Assessment_of_NBTI_in_Presence_of_Self-Heating_in_High-_k_SOI_FinFETs.pdf](../../raw/sources/Assessment_of_NBTI_in_Presence_of_Self-Heating_in_High-_k_SOI_FinFETs.pdf)
