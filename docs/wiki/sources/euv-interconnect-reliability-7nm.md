---
title: "Reliability on EUV Interconnect Technology for 7nm and Beyond"
type: source
tags: [euv, interconnect, reliability, 7nm, electromigration, tddb, copper, cobalt, ruthenium]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Reliability_on_EUV_Interconnect_Technology_for_7nm_and_beyond.pdf"]
related: [["concepts/interconnect-reliability", "Interconnect Reliability"], ["concepts/em-tdds", "EM and TDDB"], ["concepts/euv-lithography", "EUV Lithography"]]
---

# Reliability on EUV Interconnect Technology for 7nm and Beyond

## Summary
本文研究 **EUV 光刻技术实现的 7nm 及以下节点互联可靠性**。核心发现：EUV 的高能量光子（13.5nm）引入新的材料/工艺挑战；铜互联在 7nm 节点的电流密度 >10 MA/cm²，**electromigration (EM)** 和 **TDDB** 成为主要失效机制；新材料（Co、Ru、Mo）提供替代方案但也有各自挑战。

## Key Findings

### EUV Interconnect Challenges
- **Metal pitch 缩至 40 nm**（7nm 节点）
- **Via 尺寸 < 20 nm**：via resistance 和 yield 对工艺极度敏感
- **EUV mask defect**：即使单个 EUV mask 缺陷也可导致 chip 失效

### Material Evolution at 7nm

| 节点 | 金属化 | 阻挡层 |
|------|--------|--------|
| **14nm** | Cu | TaN/Ta |
| **7nm** | Cu/Co混合 | Ru/Co 替代 |
| **5nm** | Co 或 Ru 直接镀覆 | 无阻挡层 |

### Electromigration (EM) Challenges
- **电流密度 J > 10 MA/cm²**（7nm 节点）
- **EM lifetime τ ~ (A/j^n) exp(E_a/kT)**，n ≈ 1.5-2
- **铜的 EM**：原子沿晶界/界面扩散
- **新问题**：
  - **Via bottom interface**（金属/阻挡层）是 EM 失效热点
  - **multiple patterning** 导致的缺陷成为 EM 扩散路径

### TDDB (Time Dependent Dielectric Breakdown)
- **栅氧化层 / ILD** 在高电场下的击穿
- **EUV 引入的污染**：光刻胶残留碳/氢可能进入介电层
- **Low-k 介质**：k < 2.5，多孔结构 → mechanical weakness

### New Materials

#### Cobalt (Co)
- **优势**：比 Cu 更抗 EM（更高熔点）
- **挑战**： vias 中的 Co 电镀难度大，电阻率略高

#### Ruthenium (Ru)
- **优势**：可直接镀覆（无阻挡层），与 Cu 兼容
- **挑战**：沉积工艺控制困难，界面 adhesion 问题

#### Molybdenum (Mo)
- **优势**：高熔点，低电阻
- **挑战**：工艺生态不成熟

### EUV-Specific Reliability Issues
- **Patterning defects**：EUV 光刻的随机性（光子散粒噪声）→ local CD variation
- **LWR/LER**：影响 line 边缘粗糙度 → current crowding → EM 局部热点
- **Via landing**：EUV overlay 误差 → via 偏移 → current crowding at via edge

## Reliability Comparison

| Material | EM Lifetime | TDDB | Challenge |
|----------|------------|------|--------|
| **Cu/TaN** | Baseline | Baseline | 阻挡层占电阻 >50% |
| **Cu/Ru** | 改善 | OK | Ru 工艺控制 |
| **Co** | 显著改善 | 需验证 | 电镀难度 |
| **Ru** | 最佳潜力 | OK | adhesion |

## Related
- [[concepts/interconnect-reliability]] — 互联可靠性
- [[concepts/em-tdds]] — EM 和 TDDB 机制
- [[concepts/euv-lithography]] — EUV 光刻

## Source
[Reliability on EUV Interconnect Technology for 7nm and Beyond](raw/sources/Reliability_on_EUV_Interconnect_Technology_for_7nm_and_beyond.pdf)
