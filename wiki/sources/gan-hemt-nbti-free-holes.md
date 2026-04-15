---
title: "Role of Free Holes in nBTI Degradation in GaN-on-Si MOS-channel HEMTs"
type: source
tags: [gan, hemt, nbti, wide-bandgap, mos-channel, reliability, free-holes, gallium-nitride]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Role_of_free_holes_in_nBTI_degradation_in_GaN-on-Si_MOS-channel_HEMTs.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/gan-hemt", "GaN HEMT"], ["concepts/wide-bandgap", "Wide Bandgap Semiconductor"]]
---

# Role of Free Holes in nBTI Degradation in GaN-on-Si MOS-channel HEMTs

## Summary
本文研究 **GaN-on-Si MOS 沟道 HEMT（MOS-HEMT）** 中的 **nBTI（negative BTI）退化机制**。核心发现：GaN MOS-HEMT 的 **nBTI 退化与自由空穴（free holes）密切相关**，这与传统 Si MOSFET 的 NBTI 机制显著不同。GaN 材料中 2DEG（二维电子气）沟道下方的空穴积累是 nBTI 的关键驱动力。

## Key Findings

### GaN-on-Si MOS-HEMT Structure
- **GaN HEMT**：GaN/AlGaN 异质结形成 2DEG（高电子迁移率沟道）
- **GaN-on-Si**：Si 衬底上外延 GaN（成本低，但有热膨胀失配）
- **MOS-HEMT**：栅极下有 Gate dielectric (SiN/Al₂O₃) → MOS 结构

### Conventional Si MOSFET NBTI vs GaN nBTI

| | Si MOSFET NBTI | GaN-on-Si MOS-HEMT nBTI |
|---|---|---|
| **应力** | 负栅偏置 | 负栅偏置 |
| **主要载流子** | 空穴（p-MOSFET）| 电子（n-HEMT）|
| **退化机制** | Si-H 键断裂（H 扩散）| 空穴捕获到栅介质 |
| **自由空穴作用** | 间接（激活 H 释放）| **直接参与（被捕获）**|
| **位置** | 界面态/氧化层 | 栅介质陷阱 |

### Free Hole Mechanism in GaN nBTI
- **GaN 极化效应**：自发极化 + 压电极化 → 内建电场
- **2DEG 下方有空穴气（hole gas）**：极化导致价带在沟道下方升高
- **负栅偏置**：吸引空穴到栅介质/GaN 界面
- **空穴捕获**：空穴被栅介质中的陷阱捕获 → 界面势垒变化 → 2DEG 密度降低
- **Result**: Vth 正向漂移，Idsat 下降

### Temperature Dependence
- **更高温度 → 更多自由空穴**（热激发）
- **更高温度 → 更严重的 nBTI**
- 激活能与 GaN 的价带特性一致

## Comparison with Si MOSFET NBTI

| 退化参数 | Si NBTI | GaN nBTI |
|---------|---------|----------|
| ΔVth | ~20-50 mV | ~10-30 mV |
| 恢复 | 显著（功率律）| 较弱 |
| 界面态Dit | 显著增加 | 陷阱捕获主导 |
| 温度加速 | E_a ~ 0.1 eV | E_a ~ 0.2-0.3 eV |

## Implications for GaN Reliability
- GaN-on-Si 的热失配导致 **piezoelectric polarization** 变化
- 偏置和温度协同加速 nBTI
- **GaN 的极化效应是独特的**，与 Si 的 NBTI 机制不同

## Related
- [[concepts/nbti]] — NBTI 基础
- [[concepts/gan-hemt]] — GaN HEMT
- [[concepts/wide-bandgap]] — 宽禁带半导体

## Source
[Role of Free Holes in nBTI Degradation in GaN-on-Si MOS-channel HEMTs](raw/sources/Role_of_free_holes_in_nBTI_degradation_in_GaN-on-Si_MOS-channel_HEMTs.pdf)
