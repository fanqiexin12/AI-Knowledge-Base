---
title: "NBTI Mitigation Techniques"
type: concept
tags: [nbti, mitigation, reliability, circuit-design, process-engineering, fluorine, gate-merging]
created: 2026-04-14
updated: 2026-04-16
sources: ["raw/sources/Gate_Merging_An_NBTI_Mitigation_Method_to_Eliminate_Critical_Internal_Nodes_in_Digital_Circuits.pdf", "raw/sources/NBTI_performance_enhancement_with_process_integration_of_High_Current_Fluorine_incorporation_and_O2_gas_asher_process_in_45nm_CMOS_technology.pdf", "raw/sources/A_NBTI_tolerant_technique_for_FinFET_based_wide_fan-in_dynamic_logic.pdf", "raw/sources/papers-onedrive/NBTI_detection_methodology_for_building_tolerance_with_respect_to_NBTI_effects_employing_adaptive_body_bias.pdf", "raw/sources/papers-onedrive/Signal_probability_control_for_relieving_NBTI_in_SRAM_cells.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/circuit-aging", "Circuit Aging"], ["concepts/on-chip-aging-sensor", "On-Chip Aging Sensor"]]
---

# NBTI Mitigation Techniques

## Summary
NBTI 缓解技术分为**电路设计层面**和**工艺工程层面**两大类。电路层面包括 input vector control、gate merging、adaptive body bias 等；工艺层面包括 fluorine 注入、界面工程等。

## Circuit-Level Techniques

### 1. Gate Merging
- **方法**：合并功能相关的门电路，消除 critical internal nodes
- **效果**：减少关键节点的正偏置时间比例
- **代价**：面积增加 10-20%

### 2. Input Vector Control (IVC)
- **方法**：选择使关键 PMOS 处于低应力状态的输入向量
- **效果**：NBTI 退化减少 10-30%
- **限制**：需要 circuit 空闲时主动控制输入

### 3. Adaptive Body Bias (ABB)
- **方法**：NBTI 退化后通过 body bias 补偿 Vth 漂移
- **FBB (Forward BB)**：补偿 NBTI 引起的正向 Vth 漂移
- **代价**：功耗增加

### 4. Voltage/Frequency Scaling
- **方法**：降低 Vcc 或频率，减少 NBTI 应力
- **Tradeoff**：性能下降

## Process-Level Techniques

### 5. Fluorine Incorporation
- **方法**：高电流 F 注入到 Si/SiO₂ 界面
- **机制**：Si-F 键（5.5 eV）比 Si-H 键（3.5 eV）更强 → 更难断裂
- **效果**：ΔVth 减少 30-50%

### 6. Interface Engineering
- **O₂ plasma asher**：界面清洁，去除污染
- **Nitridation control**：适当 N 含量（但过多会加重 NBTI）

## Architecture-Level

### 7. NBTI-Aware Design Margins
- **方法**：设计时预留更多 timing margin
- **代价**：性能/功耗损失

## Comparison

| Technique | Effectiveness | Cost | Maturity |
|-----------|---------------|------|----------|
| Gate Merging | 中等 | 中等面积 | 高 |
| IVC | 低-中 | 极低 | 高 |
| ABB | 高 | 中等功耗 | 中 |
| F Injection | 高 | 工艺复杂 | 中 |
| Interface Eng. | 中 | 工艺集成 | 高 |

## Related
- [[concepts/nbti]] — NBTI 基础机制
- [[concepts/circuit-aging]] — 电路老化
