---
title: "Yield and Reliability Challenges at 7nm and Below"
type: source
tags: [7nm, advanced-nodes, yield, reliability, variability, defects, euv, manufacturing]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Yield_and_Reliability_Challenges_at_7nm_and_Below.pdf"]
related: [["concepts/nanosheet-fet", "Nanosheet FET"], ["concepts/variability-sources", "Variability Sources"], ["concepts/reliability-challenges", "Reliability Challenges at Advanced Nodes"]]
---

# Yield and Reliability Challenges at 7nm and Below

## Summary
本文综述 **7nm 及以下节点**的良率和可靠性挑战。7nm 节点引入 **EUV 光刻 + 多重 patterning**、**新器件架构（FinFET → GAA）**、**新金属化方案**，同时面临 **variability 加剧、new defect 机制、electromigration 挑战**等问题。

## Key Challenges

### 1. Patterning Challenges
- **7nm 需要 EUV + 多重 patterning**（SAQP/LELE）
- **Line-edge roughness (LER)** 和 **line-width roughness (LWR)** 影响器件性能
- **Overlay error** 在多重 patterning 中累积 → 增加 variability

### 2. Variability Challenges
| Source | Impact at 7nm |
|--------|--------------|
| **Random Discrete Doping (RDD)** | 21 nm 沟道只有 ~30 个 doping 原子 |
| **Workfunction Variation (WFV)** | HKMG grain size ~5 nm（与 feature 尺寸相当）|
| **LER** | 原子级粗糙度影响栅极长度 |
| **Thickness Variation** | 纳米片厚度波动（~5 nm）更显著 |

### 3. Device Architecture Transition
- **FinFET at 7nm**：Fin 高度和数量接近物理极限
- **GAA (Nanosheet) at 3nm/2nm**：水平纳米片堆叠
- 新架构带来新的可靠性问题（nanowire/nanosheet 机械稳定性）

### 4. Interconnect Challenges
- **铜阻挡层（Cu barrier）** 在 7nm 节点占互联电阻的 >50%
- **EUV 互联**：新的材料选择（Co、Ru、Mo）引入新的失效模式
- **Electromigration (EM)**：电流密度 >10 MA/cm²，EM 风险大增
- **Via resistance variation**：multiple patterning 导致 via 形状不规则

### 5. New Defect Mechanisms
- **Gate-all-around short**：纳米片间距不均匀导致栅-源/漏短路
- **Stack variation**：纳米片层数/厚度不均匀
- **Bottom oxide breakdown**：纳米片底部的氧化层击穿
- **Parametric yield loss**：Vth、漏电流、亚阈值斜率分布尾部（tail distribution）超出 spec

### 6. Reliability Challenges
| Issue | Description |
|-------|-------------|
| **BTI** | NBTI/PBTI 在更薄氧化层下更严重 |
| **HCI** | 短沟道效应使 HCI 重新成为问题 |
| **TDDB** | Time Dependent Dielectric Breakdown，薄氧化层击穿 |
| **EM** | 电流密度极高，金属迁移加速 |
| **SM** | Stress Migration，应力导致的金属断裂 |

## 7nm vs Previous Nodes

| 参数 | 14nm | 10nm | 7nm |
|------|------|------|-----|
| **光刻** | ArF DPT | ArF DPT + SAQP | EUV + DPT |
| **Fin 间距** | 70 nm | 54 nm | 40 nm |
| **Metal pitch** | 80 nm | 64 nm | 40 nm |
| **电流密度** | ~2 MA/cm² | ~5 MA/cm² | >10 MA/cm² |
| **主要 variability** | LER + RDF | WFV + LER | RDD + WFV |

## Mitigation Strategies
- **Design for Manufacturability (DFM)**：在 design 中考虑工艺窗口
- **Aging-aware design**：预留 BTI 退化余量
- **Redundant via/structure**：增加互联鲁棒性

## Related
- [[concepts/nanosheet-fet]] — GAA 架构
- [[concepts/variability-sources]] — variability 源
- [[concepts/reliability-challenges]] — 先进节点可靠性

## Source
[Yield and Reliability Challenges at 7nm and Below](raw/sources/Yield_and_Reliability_Challenges_at_7nm_and_Below.pdf)
