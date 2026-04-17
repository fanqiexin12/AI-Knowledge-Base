---
title: "FinFET"
type: concept
tags: [finfet, mugfet, mosfet, 3d-gate, multi-gate, semiconductor, advanced-nodes, short-channel-effect, fin-width]
created: 2026-04-14
updated: 2026-04-16
sources: ["raw/sources/A_NBTI_tolerant_technique_for_FinFET_based_wide_fan-in_dynamic_logic.pdf", "raw/sources/A_Guideline_for_the_Optimum_Fin_Width_Considering_Hot-Carrier_and_NBTI_Degradation_in_MuGFETs.pdf", "raw/sources/Assessment_of_NBTI_in_Presence_of_Self-Heating_in_High-_k_SOI_FinFETs.pdf", "raw/sources/FinFET_NBTI_degradation_reduction_and_recovery_enhancement_through_hydrogen_incorporation_and_self-heating.pdf", "raw/sources/papers-onedrive/Study_on_NBTI_improvement_of_HfO2-based_14_nm_P-type_FinFET_with_post_high-k_deposition_thermal_treatment.pdf", "raw/sources/papers-onedrive/Improved_NBTI_reliability_with_sub-1-nanometer_EOT_ZrO2_gate_dielectric_compared_with_HfO2.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/hci", "HCI"], ["concepts/nanosheet-fet", "Nanosheet FET"]]
---

# FinFET

## Summary
**FinFET（鳍式场效应晶体管）** 是一种 **3D 栅极结构** 的 MOSFET，沟道成鳍状突出，栅极从三面包覆沟道。相比 planar MOSFET，FinFET 提供更好的静电控制和更低的泄漏电流，是 **22nm 至 7nm** 节点的主流器件架构。

## Structure

```
        Gate
     =========  ← 栅极（三面包覆）
       ||||
       ||||  ← 鳍（Fin）突出
    ───────────  ← Source/Drain
       ||||
```

- **Fin 宽度**：通常 5-10 nm
- **Fin 高度**：30-60 nm（决定有效沟道宽度）
- **Gate length**：10-20 nm（7nm 节点约 18nm）

## vs Planar MOSFET

| 特性 | Planar | FinFET |
|------|--------|--------|
| **栅极控制** | 1 面 | 3 面 |
| **短沟道效应** | 严重 | 抑制 |
| **亚阈值斜率** | ~60 mV/dec | ~65 mV/dec |
| **泄漏电流** | 较高 | 低 |
| **布局效率** | 高 | 中（fin pitch）|

## Advantages
- **更好的静电控制**：3 面栅极环绕 → 更好的亚阈值斜率
- **更低泄漏**：关断时泄漏电流更低
- **更高驱动电流**：给定占位面积下驱动电流更大

## NBTI in FinFET
- **3D 结构**：fin 侧壁和顶部都受栅极控制
- **NBTI 效应**：fin 侧壁/顶部的 interface quality 可能不同
- **Gate-all-around (GAA)** 是 FinFET 的进化方向 → 4 面栅极控制

## Self-Heating Effect

- **BOX (Buried Oxide)** 热导率低 → 热量积聚在沟道
- 自加热导致温度升高 20-40°C
- 温度升高 **按 Arrhenius 关系加速 NBTI**
- High-k SOI FinFET 中 self-heating + NBTI 交互更复杂

## Hydrogen Incorporation

- **H passivation**：减少 interface traps
- 效果：ΔVth 降低 30-50%
- Self-heating 协同增强 recovery（额外 20-30%）

## High-k Dielectric Optimization

### HfO2 Thermal Treatment
- **Post high-k 热退火** 优化界面质量
- 14nm FinFET：ΔVth 减少 20-30%
- 机制：界面层再结晶、Hf-O键重组、促进H扩散

### ZrO2 vs HfO2
- **ZrO₂** (k~25) 比 **HfO₂** (k~20) NBTI表现更好
- ZrO₂ ΔVth 比 HfO₂ 低 30-50%（氧空位缺陷密度更低）
- 挑战：ZrO₂ 热稳定性需要工艺优化

## Fin Width Optimization (MuGFET)

| Fin Width | NBTI | HCI | Optimal For |
|-----------|------|-----|-------------|
| **< 10nm** | Low | High | HCI-dominated |
| **10-15nm** | Medium | Medium | **Balanced** |
| **> 20nm** | High | Low | NBTI-dominated |

- **最优 Fin Width：10-15nm** — HCI 和 NBTI 最佳平衡
- Narrow fin：peak electric field 高 → HCI 严重
- Wide fin：interface volume fraction 大 → NBTI 严重

## Related
- [[concepts/nbti]] — NBTI
- [[concepts/nanosheet-fet]] — GAA 进化
