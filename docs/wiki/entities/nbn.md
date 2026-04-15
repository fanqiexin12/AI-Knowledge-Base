---
title: "NbN"
type: entity
tags: [superconductor, hts, nbn-paste, high-hc2, film-deposition]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Superconducting_Connections_Between_NbTi_Thin_Films_With_NbN_Paste.pdf"]
related: [["entities/nbti", "NbTi"], ["concepts/superconducting-joint", "Superconducting Joint"]]
---

# NbN

## Summary
**NbN（氮化铌）** 是一种**高临界温度超导体**，Tc ≈ 17K，Hc2 ≈ 500 kG（~50T），远高于 NbTi（Tc ≈ 9.5K，Hc2 ≈ 14T）。本文将其制成 paste 形态用于实现 NbTi 之间的超导连接。

## Properties

| 参数 | 值 |
|------|-----|
| **化学成分** | NbN |
| **Tc（临界温度）** | ~17 K |
| **Hc2（上临界场）** | ~500 kG (50T) @ 4.2K |
| **薄膜制备** | Nd:YAG 激光烧蚀沉积 |
| **膜厚** | 2–3 μm |

## Advantages over NbTi for Joints

- **更高的 Tc**：17K vs 9.5K → 更高的运行温度裕度
- **更高的 Hc2**：50T vs 14T → 更高的磁场容忍度
- **高硬度**：耐磨，适合 arc-machining 表面处理

## In This Paper

NbN 以 **paste（膏体）** 形态使用：
1. **制备**：激光烧蚀 NbN 靶材 → 收集 NbN 纳米颗粒 → 混入有机载体 → 制成 paste
2. **烧结**：400°C，N₂ 氛围，10 分钟
3. **与 NbTi 连接**：热压烧结（15 MPa）实现界面结合

## Why NbN Paste?

- 可填充不规则的接头缝隙
- 烧结温度较低（400°C）低于 NbTi 临界温度（无需冷却）
- 烧结后形成连续的 NbN 通道 → 超导通路

## Related
- [[entities/nbti]] — 主要被连接的基底材料
- [[concepts/superconducting-joint]] — 连接技术
