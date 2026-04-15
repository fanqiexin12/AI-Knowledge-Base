---
title: "Investigation of Nitrogen-Enhanced NBTI Effect Using the Universal Prediction Model"
type: source
tags: [nitrogen, nbti, universal-model, prediction, interface-engineering, si-nitride, hfk]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Investigation_of_nitrogen_enhanced_NBTI_effect_using_the_universal_prediction_model.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nbti-model", "NBTI Models"]]
---

# Investigation of Nitrogen-Enhanced NBTI Effect Using the Universal Prediction Model

## Summary
本文研究**氮化界面（nitrogen-incorporated SiO₂/SiON）对 NBTI 的增强效应**。使用 **universal prediction model** 分析高氮含量界面的 NBTI 退化，发现：**SiON 界面中 N 的积累加速 Si-H 键断裂**，导致更严重的 NBTI 退化；高氮界面还有 **nitrogen clustering** 问题，形成 deep traps。

## Key Findings

### Nitrogen Effect on Si/SiO2 Interface
- **SiON（氮氧化硅）界面**：用 N 替代 SiO₂ 中的部分 O
- **N 的作用**：
  - 改善硼穿透（减少 PMOS 硼扩散）
  - 提高介电常数（允许等效 EOT 缩薄）
  - **副作用：加速 NBTI 退化**

### NBTI Enhancement Mechanism
- **N 破坏 Si-O 网络**：N 引入弱键（N-Si bonds）
- **Si-H 键在 N 附近更不稳定**：N 的电负性改变 Si 键合环境
- **N clustering**：高氮区域形成 N clusters → deep traps → 不可恢复的退化

### Universal Prediction Model
- **模型目标**：用统一的 framework 预测 NBTI（不依赖具体机制参数）
- **输入**：stress 条件（V, T, t）
- **输出**：ΔVth, Δgm, ΔSS 随时间演化
- **适用性**：可用于 Si, SiGe, FinFET, GAA 等不同架构

### Nitrogen Dependence of NBTI
| 界面类型 | N 含量 | NBTI 退化 | 恢复率 |
|----------|--------|----------|--------|
| **SiO₂** | 0% | Baseline | 高 |
| **SiON (low N)** | 1-3% | +20-30% | 略低 |
| **SiON (high N)** | 5-10% | +50-100% | 显著降低 |

### SiON vs HfO2/high-k
- **SiON**：NBTI 增强，但工艺成熟
- **HfO₂/high-k**：NBTI 更严重（更高的 k，但栅介质退化更复杂）
- **HfSiON**：结合两者问题

## Implications
- **N 含量优化**：需要平衡 B-shielding（减少硼穿透）和 NBTI
- **Universal model** 可用于不同节点和架构的 NBTI 预测
- **氮化工艺**在 45nm 及以下节点仍广泛使用（与 high-k 结合）

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/nbti-model]] — NBTI 模型

## Source
[Investigation of Nitrogen-Enhanced NBTI Effect Using the Universal Prediction Model](raw/sources/Investigation_of_nitrogen_enhanced_NBTI_effect_using_the_universal_prediction_model.pdf)
