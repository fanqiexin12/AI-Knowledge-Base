---
title: "NBTI (Negative Bias Temperature Instability)"
type: concept
tags: [reliability, degradation, p-fet, semiconductor, bti]
created: 2026-04-14
updated: 2026-04-16
sources: ["raw/sources/Impact_of_Material_Variability_on_the_Reliability_of_Nanosheet_FETs.pdf", "raw/sources/Experimental_Study_on_NBTI_Degradation_Behaviors_in_Si_pMOSFETs_Under_Compressive_and_Tensile_Strains.pdf", "raw/sources/Delay_effects_and_frequency_dependence_of_NBTI_with_sub-microsecond_measurements.pdf", "raw/sources/Reliability_analysis_of_CMOS_inverter_subjected_to_AC_amp_DC_NBTI_stresses.pdf", "raw/sources/Analysis_and_impacts_of_Negative_Bias_Temperature_Instability_NBTI.pdf", "raw/sources/A_new_oxide_trap-assisted_NBTI_degradation_model.pdf", "raw/sources/A_study_of_fluorine_dose_and_implant_energy_to_the_NBTI_upon_p_implant_sequence.pdf", "raw/sources/A_Comprehensive_Review_of_DRAM_NBTI_Issues_and_Solutions.pdf", "raw/sources/Assessment_of_NBTI_in_Presence_of_Self-Heating_in_High-_k_SOI_FinFETs.pdf", "raw/sources/Deep_experimental_investigation_of_NBTI_impact_on_CMOS_inverter_reliability.pdf", "raw/sources/Degradation_and_Self-Recovery_of_Polycrystalline_Silicon_TFT_CMOS_Inverters_Under_NBTI_Stress.pdf", "raw/sources/Enhanced_PMOS_NBTI_degradation_due_to_halo_implant_channeling.pdf", "raw/sources/FinFET_NBTI_degradation_reduction_and_recovery_enhancement_through_hydrogen_incorporation_and_self-heating.pdf", "raw/sources/papers-onedrive/Impact_of_NBTI_on_the_performance_of_35nm_CMOS_digital_circuits.pdf", "raw/sources/papers-onedrive/Impact_of_NBTI_on_the_temporal_performance_degradation_of_digital_circuits.pdf", "raw/sources/papers-onedrive/Impacts_of_NBTI_and_PBTI_on_ultra-thin-body_GeOI_6T_SRAM_cells.pdf", "raw/sources/papers-onedrive/Improved_NBTI_reliability_with_sub-1-nanometer_EOT_ZrO2_gate_dielectric_compared_with_HfO2.pdf", "raw/sources/papers-onedrive/Investigation_on_NBTI_Control_Techniques_of_HKMG_Transistors_for_Low-power_DRAM_applications.pdf", "raw/sources/papers-onedrive/Separation_of_NBTI_component_from_channel_hot_carrier_degradation_in_pMOSFETs_focusing_on_recovery_phenomenon.pdf", "raw/sources/papers-onedrive/Signal_probability_control_for_relieving_NBTI_in_SRAM_cells.pdf", "raw/sources/papers-onedrive/Reliable_cache_design_with_on-chip_monitoring_of_NBTI_degradation_in_SRAM_cells_using_BIST.pdf", "raw/sources/papers-onedrive/NBTI_and_Concurrent_HCI-NBTI_Degradation_of_65_nm_SOI_PMOSFETs.pdf", "raw/sources/papers-onedrive/Modeling_and_minimization_of_PMOS_NBTI_effect_for_robust_nanometer_design.pdf", "raw/sources/papers-onedrive/NBTI_detection_methodology_for_building_tolerance_with_respect_to_NBTI_effects_employing_adaptive_body_bias.pdf", "raw/sources/papers-onedrive/Study_on_NBTI_improvement_of_HfO2-based_14_nm_P-type_FinFET_with_post_high-k_deposition_thermal_treatment.pdf", "raw/sources/papers-onedrive/NBTI-aware_bit_line_voltage_control_with_boosted_supply_voltage_for_improvement_of_6T_SRAM_cell_read_stability.pdf"]
related: [["concepts/nanosheet-fet", "Nanosheet FET"], ["concepts/pbti", "PBTI"], ["concepts/strain-engineering", "Strain Engineering"], ["concepts/nbti-frequency-effect", "NBTI Frequency Effect"], ["concepts/ac-nbti", "AC NBTI"], ["concepts/soi-mosfet", "SOI MOSFET"], ["concepts/dram", "DRAM"], ["concepts/sram", "SRAM"], ["concepts/finfet", "FinFET"], ["concepts/hci", "HCI"]]
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

## Oxide Trap-Assisted Degradation Model

- 传统观点：NBTI 主要由界面态（Nit）主导
- 新发现：**氧化层陷阱（Not）**也显著贡献退化
- 陷阱协助机制：空穴在应力阶段被氧化层陷阱捕获，弛豫阶段去捕获
- **Time-dependent decay**：遵循 stretched exponential 行为
- 该模型能**定量预测频率效应**

## Circuit-Level Impacts

| Circuit | NBTI Impact |
|---------|-------------|
| **SRAM** | SNM 退化，读取/写入裕量下降 |
| **Ring Oscillator** | 频率下降 2-5%（10年），可用作 on-chip monitor |
| **Sense Amplifier** | Voffset 增加，读取灵敏度退化 |
| **DRAM** | retention time 缩短，需要更频繁 refresh |

## DRAM NBTI

- DRAM cell 使用 pMOS access transistor，NBTI 导致 Vth 正漂移
- **Retention time degradation**：64ms → 32ms 或更短
- Write margin 和 read disturb 也会退化
- 缓解方法：adaptive refresh、ECC、wear leveling

## Self-Heating Effect on NBTI

- **SOI/FinFET 结构**的热阻较高，自加热效应显著
- 功率耗散导致沟道温度升高 20-40°C
- 温度升高按 **Arrhenius 关系**加速 NBTI（每升高 10°C，速率翻倍）
- High-k 介质与 SOI 结构结合时 NBTI 更敏感
- 自加热与 NBTI recovery 产生复杂交互：高温加速降解但也加速恢复

## CMOS Inverter Reliability

- NBTI 导致 **PMOS Vth 正漂移**（~50mV @ 10yr）
- **Switching threshold (V_M)** 向 NMOS 侧漂移（~30mV）
- **Noise margin** 退化 10-15%
- **Propagation delay** 增加 5-10%
- Poly-Si TFT 呈现部分自恢复（70-80% 恢复率）

## Halo Implant Channeling Effect

- **Halo implant** 沿晶向通道注入时产生 **channeling 效应**
- 非均匀掺杂分布引入局部 **compressive strain**
- Compressive strain 降低 Si-H 键能 → NBTI 加剧
- PMOS ΔVth **增加 30-50%** compared to non-channeling samples

## Hydrogen Incorporation for NBTI Reduction

- **H 钝化**：氢与硅悬挂键形成 Si-H 键，减少界面态
- 效果：**ΔVth 降低 30-50%**
- 与自加热协同：高温增强缺陷退火和空穴去捕获
- Recovery 增强额外 **20-30%**

## Related
- [[concepts/nanosheet-fet]] — Nanosheet 架构对此 degradation 的敏感性
- [[concepts/pbti]] — PBTI counterpart
- [[concepts/strain-engineering]] — 应变工程及其对 NBTI/PBTI 的相反影响
- [[concepts/nbti-frequency-effect]] — 频率依赖性详解
- [[concepts/ac-nbti]] — AC NBTI 机制
- [[concepts/soi-mosfet]] — SOI floating-body history effect
