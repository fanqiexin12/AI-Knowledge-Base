---
title: "FinFET NBTI Degradation Reduction and Recovery Enhancement Through Hydrogen Incorporation and Self-Heating"
type: source
tags: [nbti, finfet, hydrogen, self-heating, recovery, reliability]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/FinFET_NBTI_degradation_reduction_and_recovery_enhancement_through_hydrogen_incorporation_and_self-heating.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/finfet", "FinFET"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# FinFET NBTI Degradation Reduction and Recovery Enhancement Through Hydrogen Incorporation and Self-Heating

## Summary
本文研究 **氢离子注入（Hydrogen Incorporation）** 对 **FinFET NBTI** 的改善作用。氢钝化界面态，减少降解；同时自加热效应（Self-Heating）增强恢复效应。

## Key Findings

### Hydrogen Incorporation Mechanism
- **H passivation**：氢与硅悬挂键（dangling bonds）形成 Si-H 键
- **界面态密度（Dit）降低**：减少 NBTI 相关的陷阱生成
- **效果**：ΔVth 减少 **30-50%**

### NBTI Reduction Effect
| Condition | ΔVth (10yr stress) | Reduction |
|-----------|---------------------|----------|
| **Without H** | ~80mV | baseline |
| **With H incorporation** | ~40-50mV | **30-50%** |

### Self-Heating Effect on Recovery
- FinFET 的 **自加热** 在高功率运行时显著
- 温度升高（ΔT ~ 20-30°C）促进：
  - **缺陷退火（defect annealing）**
  - **空穴去捕获（hole de-trapping）**
- Recovery 增强量：**20-30%** additional recovery

### Combined Effect
```
Hydrogen Incorporation (during processing)
    ↓
Interface passivation, reduced Dit
    ↓
Less trap generation under NBTI stress
    ↓
Reduced degradation (30-50% lower ΔVth)

Self-Heating during operation
    ↓
Elevated temperature
    ↓
Enhanced recovery (annealing + de-trapping)
    ↓
Additional 20-30% recovery
```

### FinFET-Specific Considerations
- Fin 结构的热阻较高 → 自加热效应更明显
- 3D 结构：热量从 fin 侧壁散发
- 氢钝化主要在沟道interface/侧壁

## Process Integration
- **H plasma treatment** 或 **H ion implantation**
- 需要优化剂量和能量，避免引入 new defects
- 与现有 CMOS 工艺兼容

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/finfet]] — FinFET structure
- [[concepts/circuit-aging]] — Circuit aging

## Source
- [FinFET_NBTI_degradation_reduction_and_recovery_enhancement_through_hydrogen_incorporation_and_self-heating.pdf](../../raw/sources/FinFET_NBTI_degradation_reduction_and_recovery_enhancement_through_hydrogen_incorporation_and_self-heating.pdf)
