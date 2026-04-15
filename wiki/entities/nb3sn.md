---
title: "Nb3Sn"
type: entity
tags: [superconductor, nb3sn, high-field, sht3-sn, tce, bronze-route, pit, mri-magnets, iter]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Fabrication_and_Test_of_Nb3Sn-NbTi_Superconducting_Joint_for_a_14-T_MRI_Magnet.pdf"]
related: [["entities/nbti", "NbTi"], ["concepts/superconducting-joint", "Superconducting Joint"], ["concepts/superconducting-magnet", "Superconducting Magnet"]]
---

# Nb3Sn (Niobium-Tin)

## Summary
**Nb₃Sn（铌三锡）** 是临界温度最高的低温超导体之一（Tc ≈ 18K），上临界场 Hc2 高达 25-30T。主要用于 **14T 以上的高场 MRI/NMR 磁体**和 **ITER tokamak 超导磁体**。但 Nb₃Sn 工艺难度大（需要 600-700°C 热处理），且应变敏感。

## Properties

| 参数 | 值 |
|------|-----|
| **化学成分** | Nb₃Sn |
| **Tc（临界温度）** | ~18 K |
| **Hc2（上临界场）** | 25-30 T @ 4.2K |
| **Jc（临界电流密度）** | ~3000 A/mm² @ 4.2K, 12T |
| **常用形态** | 多芯线材（bronze route / PIT）|
| **工作温度** | 4.2 K（液氦） |

## Why Nb3Sn vs NbTi?

| 参数 | NbTi | Nb₃Sn |
|------|------|-------|
| **Tc** | 9.5 K | 18 K |
| **Hc2** | 14 T | 25-30 T |
| **最高可用场** | ~10 T | >20 T |
| **工艺** | 挤出（简单）| 扩散反应（复杂）|
| **应变敏感性** | 低 | 高（需<0.2%应变）|
| **成本** | 低 | 高 |

## Manufacturing Methods

### Bronze Route
1. Nb 棒放入 Cu-Sn bronze 基体
2. 多重拉拔成线
3. **Heat treatment (600-700°C)**：Sn 扩散与 Nb 反应形成 Nb₃Sn
4. 缺点：Sn 含量受 bronze 溶解度限制（~15 wt%）

### Powder-in-Tube (PIT)
1. NbSn₂ 粉末装入 Nb 管
2. 拉拔成线
3. **Heat treatment**：NbSn₂ 分解生成 Nb₃Sn + Sn
4. 优点：Sn 含量更高，Jc 更高

## Applications

- **NMR 磁体**：>23T（Nb₃Sn 必须）
- **ITER TF 磁体**：13T 级，18 个线圈
- **14T MRI 磁体**：混合 Nb₃Sn/NbTi 设计
- **高场实验室磁体**：>20T

## Key Challenges

- **Strain sensitivity**：Nb₃Sn 对应变极其敏感，>0.2%应变会导致 Ic 急剧下降
- **Mechanical stress**：热收缩失配 → 线圈制备时预应变控制
- **Brittleness**：Nb₃Sn 脆性，无法像 NbTi 那样弯曲加工
- **Thermal cycling**：每次冷却/升温都产生应力循环

## Related
- [[entities/nbti]] — NbTi 对比
- [[concepts/superconducting-joint]] — Nb₃Sn/NbTi 接头
- [[concepts/superconducting-magnet]] — 超导磁体
