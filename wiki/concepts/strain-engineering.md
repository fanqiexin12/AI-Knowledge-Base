---
title: "Strain Engineering in Semiconductor Devices"
type: concept
tags: [strain-engineering, semiconductor, performance, reliability, finfet, nanosheet, nbti, pbti]
created: 2026-04-14
updated: 2026-04-16
sources: ["raw/sources/Experimental_Study_on_NBTI_Degradation_Behaviors_in_Si_pMOSFETs_Under_Compressive_and_Tensile_Strains.pdf", "raw/sources/Enhanced_PMOS_NBTI_degradation_due_to_halo_implant_channeling.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/pbti", "PBTI"], ["concepts/nanosheet-fet", "Nanosheet FET"]]
---

# Strain Engineering in Semiconductor Devices

## Summary
应变工程是提升 CMOS 器件驱动电流的核心技术，通过在沟道中引入**机械应变**调节晶格常数，影响载流子迁移率和器件性能。但应变同时影响可靠性机制——**compressive strain 恶化 NBTI、tensile strain 恶化 PBTI**，制造中需要在性能与可靠性之间做权衡。

## Strain Types & Effects

| 应变类型 | 效果 | 对 NBTI | 对 PBTI |
|----------|------|---------|---------|
| **Compressive** (压应变) | 提升 PMOS 驱动电流 | 恶化 ↑ | 减轻 ↓ |
| **Tensile** (张应变) | 提升 NMOS 驱动电流 | 减轻 ↓ | 恶化 ↑ |

## Mechanisms

### Performance Effect
- **Si-Si 键长变化**影响载流子散射率
- Compressive strain → 降低空穴有效质量 → 提高 PMOS 迁移率
- Tensile strain → 降低电子有效质量 → 提高 NMOS 迁移率

### Reliability Effect (NBTI/PBTI)
- **关键：Si-H 键能**
  - Compressive strain → Si-H 键能降低 → H 更容易释放 → NBTI 恶化
  - Tensile strain → Si-H 键能增大 → H 更难释放 → NBTI 减轻
- **NBTI 和 PBTI 对应变的响应相反**

### Halo Implant Channeling Effect
- **Halo implant** 注入时沿晶向产生 channeling
- Channeling 导致非均匀掺杂分布
- 局部 compressive strain 增强 NBTI 30-50%
-  Mitigation：使用 (100) 晶圆、注入角旋转、剂量优化

## Technology Node Evolution

### Planar Era
- **NMOS**：tensile SiN CESL（接触停止层应力）
- **PMOS**：compressive SiGe 衬底 or CESL

### FinFET Era
- **PMOS**：SiGe source/drain → intrinsic compressive strain
- **NMOS**： tensile contact liners
- **权衡**：compressive strain 提升 PMOS 性能，但同时加剧 NBTI

### Nanosheet/GAA Era
- 纳米片结构天然提供一定的应变调制
- 纳米片宽度/厚度设计影响应变分布
- 多层堆叠提供额外的性能提升路径

## Reliability-Performance Tradeoff

```
Performance ↑  ←  Compressive strain  →  NBTI Reliability ↓
Performance ↑  ←  Tensile strain       →  PBTI Reliability ↓
```

这意味着：
- 不能一味增大应变来提升性能
- 需要在 circuit lifetime 和 performance target 之间找平衡
- 对可靠性敏感的应用（analog、RF）需要更保守的应变设计

## Related
- [[concepts/nbti]] — NBTI 机制及应变对其的影响
- [[concepts/pbti]] — PBTI 机制及应变对其的影响
- [[concepts/nanosheet-fet]] — nanosheet 架构中的应变考虑
