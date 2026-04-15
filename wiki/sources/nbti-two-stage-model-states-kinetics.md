---
title: "A Study of the States Kinetics in NBTI Degradation by Two-Stage NBTI Model Implementation"
type: source
tags: [nbti, two-stage-model, nbti-model, degradation-mechanism, states-kinetics, interface-traps]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/A_study_of_the_states_kinetics_in_NBTI_degradation_by_two-stage_NBTI_model_implementation.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nbti-model", "NBTI Models"]]
---

# A Study of the States Kinetics in NBTI Degradation by Two-Stage NBTI Model Implementation

## Summary
本文通过 **Two-Stage NBTI 模型** 研究 NBTI 退化中的 **states kinetics（态动力学）**。Two-Stage 模型认为 NBTI 退化分为两个阶段：**(1) Interface trap creation**（界面态产生）和 **(2) Hole trapping**（空穴捕获）。实验数据表明 hole trapping 贡献了大部分初始快速退化，而 interface trap creation 主导长期退化。

## Two-Stage NBTI Model

### Stage 1: Interface Trap Creation (Si-H Bond Breaking)
- **过程**：Si-H 键在电场/热作用下断裂 → H 扩散 → 界面态 Dit 增加
- **时间尺度**：较慢（秒到小时）
- **可恢复性**：部分可恢复（H 可以重新钝化）

### Stage 2: Hole Trapping (Oxide Trap Capture)
- **过程**：空穴被氧化层中的 pre-existing 陷阱捕获
- **时间尺度**：快速（毫秒到秒）
- **可恢复性**：较弱（深陷阱难以释放）

### Combined Effect
- ΔVth = ΔVth_interface + ΔVth_trap
- **初期**：hole trapping 主导（快速）
- **长期**：interface trap creation 主导（累积效应）

## Key Experimental Findings

### Recovery Behavior
- **Initial recovery**：主要是 hole trapping 的反向过程（快速）
- **Long-term recovery**：interface trap 较慢恢复
- Recovery 遵循 **stretched-exponential** 或 **power-law** 模型

### States Kinetics
- **Pre-existing traps**：制造过程中引入，分布不均匀
- **Stress-induced traps**：NBTI stress 产生的新陷阱
- **Dopant effect**：Si 中的 doping 种类影响 NBTI kinetics

## Model Parameters
| 参数 | Interface Traps | Hole Traps |
|------|---------------|------------|
| **Activation energy** | ~0.1 eV | ~0.2-0.3 eV |
| **Time exponent** | n ~ 0.15-0.2 | n ~ 0.3-0.5 |
| **Recovery rate** | 慢 | 快 |

## Implications for NBTI Prediction
- 单一 R-D 模型不足以描述 NBTI 全过程
- Two-Stage 模型更准确预测长期退化
- AC NBTI 需要考虑两种 states 的不同 recovery rates

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/nbti-model]] — NBTI 模型

## Source
[A Study of the States Kinetics in NBTI Degradation by Two-Stage NBTI Model Implementation](raw/sources/A_study_of_the_states_kinetics_in_NBTI_degradation_by_two-stage_NBTI_model_implementation.pdf)
