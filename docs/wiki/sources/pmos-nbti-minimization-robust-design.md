---
title: "Modeling and Minimization of PMOS NBTI Effect for Robust Nanometer Design"
type: source
tags: [nbti, pmos, modeling, robust-design, circuit-aging, reliability, lifetime]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/Modeling_and_minimization_of_PMOS_NBTI_effect_for_robust_nanometer_design.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# Modeling and Minimization of PMOS NBTI Effect for Robust Nanometer Design

## Summary
本文建立了 **PMOS NBTI 退化模型**，并提出 **纳米尺度设计的 NBTI 最小化方法**。模型包含温度、电压、时间依赖性，可用于 circuit aging 仿真。

## Key Findings

### NBTI Model
- **ΔVth(t) = A × t^n** (power-law time dependence)
- **n** ~ 0.15-0.25 (stress-dependent)
- **A** depends on Vg, T, process

### Model Parameters
| Parameter | Expression | Typical Value |
|-----------|------------|---------------|
| **Time exponent (n)** | Process-dependent | 0.15-0.25 |
| **Voltage factor** | exp(β×Vg) | β ~ 1-2 V⁻¹ |
| **Temperature (Ea)** | exp(-Ea/kT) | Ea ~ 0.12 eV |
| **Process factor** | exp(σ×P) | σ ~ doping |

### Minimization Strategies
1. **Input vector control**：选择 Vth 漂移最小的输入
2. **Body biasing**：Forward body bias 减少 NBTI impact
3. **Gate sizing**：增加关键路径晶体管尺寸
4. **Voltage scaling**：降低 Vdd（trade-off with performance）

### Lifetime Projection
- **10 年 @ 125°C**：ΔVth ~ 50-80mV
- **Circuit timing margin**：需要预留 10-15%

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/circuit-aging]] — Circuit aging

## Source
- [Modeling_and_minimization_of_PMOS_NBTI_effect_for_robust_nanometer_design.pdf](../../raw/sources/papers-onedrive/Modeling_and_minimization_of_PMOS_NBTI_effect_for_robust_nanometer_design.pdf)
