---
title: "NBTI (Negative Bias Temperature Instability)"
type: concept
tags: [reliability, degradation, p-fet, semiconductor, bti]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Impact_of_Material_Variability_on_the_Reliability_of_Nanosheet_FETs.pdf", "raw/sources/Experimental_Study_on_NBTI_Degradation_Behaviors_in_Si_pMOSFETs_Under_Compressive_and_Tensile_Strains.pdf", "raw/sources/Delay_effects_and_frequency_dependence_of_NBTI_with_sub-microsecond_measurements.pdf", "raw/sources/Reliability_analysis_of_CMOS_inverter_subjected_to_AC_amp_DC_NBTI_stresses.pdf"]
related: [["concepts/nanosheet-fet", "Nanosheet FET"], ["concepts/pbti", "PBTI"], ["concepts/strain-engineering", "Strain Engineering"], ["concepts/nbti-frequency-effect", "NBTI Frequency Effect"], ["concepts/ac-nbti", "AC NBTI"], ["concepts/soi-mosfet", "SOI MOSFET"]]
---

# NBTI (Negative Bias Temperature Instability)

## Summary
NBTI 是 p-FET 在**负栅极偏置 + 高温**条件下发生的时变可靠性 degradation 机制，表现为阈值电压 Vth 漂移和亚阈值斜率退化，主要由**栅极氧化层/界面陷阱**引起。

## Mechanism

- **条件**：Vgs < 0（负偏置）+ 高温（T > 300K）
- **过程**：
  1. Si-H 键在电场/热作用下断裂
  2. H 扩散到氧化层，形成界面陷阱（Dit）
  3. 陷阱捕获空穴 → Vth 正向漂移
- **建模**：Reaction-Diffusion (R-D) 模型
- **应力条件**（论文中）：Vgs = -1.4V，T = 300K / 400K

## Effects on Circuit

- Vth 漂移 → circuit timing degradation
- SS (subthreshold slope) 退化 → switch 变慢
- Ring oscillator 频率下降 → chip 性能随时间衰减
- **NBTI 主要影响 p-FET**，PBTI 主要影响 n-FET

## Strain Effect

| 应变类型 | NBTI 效应 |
|----------|-----------|
| **Compressive** (压应变) | 恶化 ↑ |
| **Tensile** (张应变) | 减轻 ↓ |

- **机制**：
  - Compressive strain → Si-Si 键被压缩 → 键长缩短 → Si-H 键能降低 → H 更容易断裂释放 → NBTI 加剧
  - Tensile strain → Si-Si 键被拉伸 → 键长增加 → Si-H 键能增大 → H 难以释放 → NBTI 减轻
- **实际意义**：PMOS 的 compressive strain（提升驱动电流）会**同时加剧 NBTI 退化**，需要权衡可靠性

## Frequency & AC Effect

| 工作条件 | NBTI 效应 |
|----------|-----------|
| **DC stress** | Maximum（worst case，无 recovery）|
| **< 1 MHz AC** | 显著（recovery 时间不足）|
| **> 1 MHz AC** | 可忽略（recovery 时间充足）|

- **机制**：AC stress 的 OFF-phase 提供 recovery 时间，频率越高 recovery 越充分
- **DC = Upper bound**：DC stress 用于 NBTI 加速测试
- **AC stress**：PMOS NBTI + NMOS PBTI 共同作用，VM 向 NMOS 侧漂移

## SOI History Effect

- PD-SOI floating body 导致 NBTI 退化有历史记忆
- **负偏置存储**（Vgs < 0 during interval）→ 加速 NBTI 退化
- **零偏置存储**（Vgs = 0 during interval）→ NBTI 部分恢复

## Related
- [[concepts/nanosheet-fet]] — Nanosheet 架构对此 degradation 的敏感性
- [[concepts/pbti]] — PBTI counterpart
- [[concepts/strain-engineering]] — 应变工程及其对 NBTI/PBTI 的相反影响
- [[concepts/nbti-frequency-effect]] — 频率依赖性详解
- [[concepts/ac-nbti]] — AC NBTI 机制
- [[concepts/soi-mosfet]] — SOI floating-body history effect
