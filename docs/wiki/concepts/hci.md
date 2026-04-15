---
title: "HCI (Hot Carrier Injection)"
type: concept
tags: [hci, hot-carrier-injection, reliability, mosfet, degradation, soi]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Effect_of_Floating-Body_and_Stress_Bias_on_NBTI_and_HCI_on_65-nm_SOI_pMOSFETs.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/soi-mosfet", "SOI MOSFET"], ["concepts/strain-engineering", "Strain Engineering"]]
---

# HCI (Hot Carrier Injection)

## Summary
**HCI（热载流子注入）** 是 MOSFET 在**高漏极电压**条件下发生的可靠性退化机制。当沟道载流子在高电场下获得足够能量（成为"热载流子"）时，可越过 Si/SiO₂ 界面势垒注入栅氧化层，被陷阱捕获导致器件参数退化。

## Mechanism

- **条件**：高 Vds（漏极电压） + 高 Vgs（栅极电压）
- **过程**：
  1. 漏端附近强电场加速沟道载流子
  2. 载流子获得足够动能（"热载流子"）
  3. 热载流子越过 Si/SiO₂ 势垒（ΔΦ ≈ 3.2 eV）注入氧化层
  4. 被氧化层陷阱捕获 → 形成界面态 Dit ↑、氧化层陷阱 N_ot
- **损伤位置**：主要在**漏端附近**（高电场区域），与 NBTI（整个沟道）不同

## Key Parameters

| 参数 | 描述 |
|------|------|
| **Substrate current I_sub** | 碰撞电离产生的衬底电流，与 HCI 强度相关 |
| **Gate current I_g** | 注入栅氧化层的电流，HCI 退化指标 |
| **Vgs @ max I_sub** | Vgs ≈ Vds/2 时碰撞电离率最高 → HCI 最严重 |
| **I_sub / I_d** | 电离率，常用于 HCI 可靠性监控 |

## Degradation Effects

- **ΔVth**：阈值电压漂移（通常正向）
- **Δgm**：跨导退化
- **ΔIdsat**：饱和驱动电流下降
- **SS 退化**：亚阈值斜率变差

## Comparison with NBTI

| | HCI | NBTI |
|---|---|---|
| **主要应力** | 高 Vds | 高 Vgs (负/正偏置) |
| **温度依赖** | 较弱 | 强（热激活） |
| **损伤分布** | 局部（漏端） | 均匀（全场） |
| **恢复效应** | 很小 | 部分可恢复 |
| **主要节点** | 较老节点（>65nm）更显著 | 先进节点（<28nm）NBTI 更显著 |
| **SOI 影响** | PD-SOI 中更严重 | stress-bias 历史效应 |

## Technology Scaling Impact

- **短沟道效应**：Vds 增加 → 电场增强 → HCI 恶化
- **Newer nodes**：HCI 在先进节点相对减轻（Vdd 降低），但 NBTI 变得更严重
- **Lateral scaling**：沟道长度缩短 → 电场 E 增加 → HCI 风险上升

## Related
- [[concepts/nbti]] — NBTI，另一种主要可靠性机制
- [[concepts/soi-mosfet]] — SOI 架构对 HCI 的影响（PD-SOI 更严重）
