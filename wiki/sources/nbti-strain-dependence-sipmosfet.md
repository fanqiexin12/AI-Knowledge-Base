---
title: "Experimental Study on NBTI Degradation Behaviors in Si pMOSFETs Under Compressive and Tensile Strains"
type: source
tags: [nbti, strain-engineering, pmosfet, reliability, strain-silicon, finfet, nanosheet]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Experimental_Study_on_NBTI_Degradation_Behaviors_in_Si_pMOSFETs_Under_Compressive_and_Tensile_Strains.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/pbti", "PBTI"], ["concepts/strain-engineering", "Strain Engineering"]]
---

# Experimental Study on NBTI Degradation Behaviors in Si pMOSFETs Under Compressive and Tensile Strains

## Summary
本文通过**实验研究**揭示了**机械应变（strain）对 Si pMOSFET 的 NBTI 退化**的影响规律：** compressive strain（压应变）加剧 NBTI，tensile strain（张应变）减轻 NBTI**。机制在于应变调节 Si-H 键的键能——压应变削弱键合使 H 更易释放，张应变增强键合使 H 难以释放。

## Key Findings

### Strain Effect on NBTI
| Strain Type | NBTI Severity | ΔVth | Δgm |
|-------------|---------------|------|-----|
| **Compressive** (压应变) | 恶化 ↑ | 更大 | 更大退化 |
| **Tensile** (张应变) | 减轻 ↓ | 更小 | 更小退化 |

### Mechanism
- **压应变**：压缩 Si-Si 键 → 键长缩短、键能降低 → Si-H 更容易断裂 → H 扩散进入氧化层 → NBTI 加剧
- **张应变**：拉伸 Si-Si 键 → 键长增加、键能增大 → Si-H 难以断裂 → NBTI 减轻

### Opposite Effect on PBTI
- **PBTI 规律与 NBTI 相反**：
  - Compressive strain → PBTI 减轻
  - Tensile strain → PBTI 加剧
- 意味着：应变工程在改善一种器件可靠性的同时，可能恶化另一种

## Technology Node Implications

### Planar Bulk → Strain Si
- **NMOS**：tensile CESL (contact etch stop layer) → 提高驱动电流
- **PMOS**：compressive SiGe substrate or CESL → 提高驱动电流
- **Tradeoff**：对 PMOS 用 compressive strain 提升性能，但会**加剧 NBTI**

### FinFET Era
- **PMOS**：SiGe source/drain 形成 intrinsic compressive strain → 提升驱动电流
- **代价**：compressive strain 加剧 NBTI 退化 → 可靠性降低
- 制造工艺需要在**性能提升**和**可靠性退化**之间做权衡

### Nanosheet (GAA)
- 纳米片堆叠结构中应变工程依然重要
- 需要考虑 nanosheet 堆叠层数/宽度与应变效应的交互

## Key Experimental Observations

1. **应变效应随应力电压增强**：Vgs 越大 → 应变对 NBTI 的影响越显著
2. **亚阈值摆幅 (SS) 退化**：NBTI 期间 SS 退化与 ΔVth 成正相关
3. **gm (跨导) 退化**：与界面陷阱密度 Dit 增长一致
4. **恢复特性**：去除应力后，张应变器件恢复更慢（更强的键 = 更难恢复）

## Practical Implications

- **可靠性-性能权衡**： compressive strain 提升 PMOS 性能，但 NBTI 可靠性下降
- **电路设计**：对 NBTI 敏感的 circuit（如 analog、RF）需要考虑 strain 效应
- **加速测试**：应变可用于加速 NBTI 退化测试

## Related
- [[concepts/nbti]] — NBTI 基础机制
- [[concepts/pbti]] — PBTI 及与 NBTI 的对比
- [[concepts/strain-engineering]] — 应变工程技术

## Source
[Experimental Study on NBTI Degradation Behaviors in Si pMOSFETs Under Compressive and Tensile Strains](raw/sources/Experimental_Study_on_NBTI_Degradation_Behaviors_in_Si_pMOSFETs_Under_Compressive_and_Tensile_Strains.pdf)
