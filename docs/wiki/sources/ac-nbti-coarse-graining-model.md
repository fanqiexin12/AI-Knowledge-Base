---
title: "A Coarse-Graining Approach to Rate Equations of the Composite AC-NBTI Model"
type: source
tags: [nbti, ac-nbti, model, coarse-graining, reaction-diffusion, multi-timescale, circuit-simulation]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/A_coarse-graining_approach_to_rate_equations_of_the_composite_AC-NBTI_model.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/ac-nbti", "AC NBTI"], ["concepts/nbti-model", "NBTI Models"]]
---

# A Coarse-Graining Approach to Rate Equations of the Composite AC-NBTI Model

## Summary
本文提出一种**粗粒化方法（coarse-graining）** 来简化复合 AC-NBTI 模型的**速率方程**。AC NBTI 涉及多时间尺度（从 ns 到 years），完整模型计算成本高。粗粒化方法通过**聚合快动力学变量**，将模型简化为可集成到电路仿真的形式，同时保持精度。

## Key Findings

### Multi-Timescale Challenge in AC-NBTI
| 时间尺度 | 物理过程 | 挑战 |
|----------|---------|------|
| **ns-μs** | 快速空穴捕获/释放 | 需要超快测量 |
| **μs-ms** | 界面态填充/清空 | AC 效应最显著 |
| **s-hour** | H 扩散 | 长期退化 |
| **years** | 永久界面损伤累积 | 寿命预测 |

### Composite AC-NBTI Model
- **Interface trap (Nit)**：Si-H 键断裂产生，慢速
- ** Oxide trap (Not)**：氧化层空穴捕获，快速
- **两种 states 相互作用**：Not 变化影响 Nit 的 creation/recovery

### Coarse-Graining Method
- **目标**：减少状态变量数量，加速电路仿真
- **方法**：
  1. 识别快慢变量（快：Not；慢：Nit）
  2. 对快变量做 quasi-steady-state 近似
  3. 将快变量的效应合并到慢变量演化方程
- **结果**：N 个微分方程 → M 个（M << N）

### Speed-Accuracy Tradeoff
| 模型 | 变量数 | 仿真时间 | 精度 |
|------|--------|---------|------|
| **Full model** | 10+ | 小时级 | 100% |
| **Coarse-grained** | 3-5 | 秒级 | >95% |
| **Empirical** | 1-2 | ms级 | ~80% |

### Application to Circuit Simulation
- **SPICE/Verilog-AMS 集成**：粗粒化模型可直接嵌入
- **Monte Carlo 仿真**：加速 statistical aging 分析
- **Product qualification**：快速评估 lifetime margin

## Physical Insights
- **Fast states dominate AC response**：空穴捕获/释放在 AC 下反复发生
- **Slow states dominate DC/aging**：H 扩散在长时间尺度累积
- **Interface coupling**：Not 和 Nit 之间的相互作用影响整体 kinetics

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/ac-nbti]] — AC NBTI
- [[concepts/nbti-model]] — NBTI 模型

## Source
[A Coarse-Graining Approach to Rate Equations of the Composite AC-NBTI Model](raw/sources/A_coarse-graining_approach_to_rate_equations_of_the_composite_AC-NBTI_model.pdf)
