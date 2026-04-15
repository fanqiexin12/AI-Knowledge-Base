---
title: "PBTI (Positive Bias Temperature Instability)"
type: concept
tags: [reliability, degradation, n-fet, semiconductor, bti]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Impact_of_Material_Variability_on_the_Reliability_of_Nanosheet_FETs.pdf"]
related: [["concepts/nanosheet-fet", "Nanosheet FET"], ["concepts/nbti", "NBTI"]]
---

# PBTI (Positive Bias Temperature Instability)

## Summary
PBTI 是 n-FET 在**正栅极偏置 + 高温**条件下发生的时变可靠性 degradation 机制，表现为阈值电压 Vth 漂移，主要与**high-k 栅极氧化层中的电子捕获**有关。

## Mechanism

- **条件**：Vgs > 0（正偏置）+ 高温（T > 300K）
- **过程**：
  1. 电子注入 high-k 栅极氧化层
  2. 被氧化层陷阱捕获
  3. 导致 Vth 正向漂移（对 n-FET）
- **建模**：Reaction-Diffusion (R-D) 模型
- **应力条件**（论文中）：Vgs = +1.2V，T = 300K / 400K

## Comparison with NBTI

| | NBTI | PBTI |
|---|---|---|
| **靶器件** | p-FET | n-FET |
| **主要机制** | 界面陷阱（H 扩散） | 电子捕获（high-k） |
| **严重程度** | 通常更严重 | 在 HKMG 节点较显著 |
| **恢复效应** | 部分可恢复 | 恢复效应较弱 |

## Strain Effect

| 应变类型 | PBTI 效应 |
|----------|-----------|
| **Compressive** (压应变) | 减轻 ↓ |
| **Tensile** (张应变) | 恶化 ↑ |

- **机制**：PBTI 与 NBTI 对应变的响应**相反**
  - Compressive strain → Si-H 键能增大 → H 难以释放 → PBTI 减轻
  - Tensile strain → Si-H 键能降低 → H 更容易释放 → PBTI 恶化
- **实际意义**：对 NMOS 用 tensile strain 提升性能，但会**加剧 PBTI**

## Related
- [[concepts/nanosheet-fet]] — Nanosheet 架构下的 PBTI 特性
- [[concepts/nbti]] — NBTI counterpart
- [[concepts/strain-engineering]] — 应变工程及其对 NBTI/PBTI 的相反影响
