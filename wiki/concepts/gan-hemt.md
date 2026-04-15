---
title: "GaN HEMT"
type: concept
tags: [gan, hemt, wide-bandgap, 2deg, algan/gan-heterostructure, reliability, nbti, power-electronics]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Role_of_free_holes_in_nBTI_degradation_in_GaN-on-Si_MOS-channel_HEMTs.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/wide-bandgap", "Wide Bandgap Semiconductor"]]
---

# GaN HEMT

## Summary
**GaN HEMT（氮化镓高电子迁移率晶体管）** 是一种基于 **AlGaN/GaN 异质结** 的宽禁带功率半导体器件，利用 **2DEG（二维电子气）** 作为导电沟道。GaN HEMT 具有 **高电子迁移率、高击穿电压、低损耗** 的特点，是 **功率电子、射频(RF)、汽车电子** 的新兴候选技术。

## Structure

```
     Gate
       |
   AlGaN barrier (20-30 nm)
       |
    GaN channel (2DEG at interface)
       |
    GaN buffer
       |
     Si/sapphire substrate
```

## Key Properties

| Parameter | GaN | Si | GaAs |
|-----------|-----|-----|------|
| **Bandgap** | 3.4 eV | 1.1 eV | 1.4 eV |
| **Breakdown field** | 3.3 MV/cm | 0.3 MV/cm | 0.4 MV/cm |
| **Electron mobility** | 2000 cm²/Vs | 1400 | 8500 |
| **Max temperature** | 400°C | 150°C | 200°C |

## 2DEG Formation
- **Spontaneous polarization** + **piezoelectric polarization**
- AlGaN/GaN 界面电场 → 三角形势阱 → 2DEG
- **无需 doping** 就有高浓度 2DEG（~10¹³ cm⁻²）

## GaN-on-Si vs GaN-on-SiC
| | GaN-on-Si | GaN-on-SiC |
|---|----------|------------|
| **成本** | 低 | 高 |
| **热导率** | 低（Si）| 高（SiC）|
| **晶格失配** | ~17%（大）| ~3%（小）|
| **最高电压** | 650V | 1200V+ |

## Reliability Issues

### NBTI in GaN
- **GaN nBTI**：负栅偏置下的退化，机制与 Si 不同
- **Free holes** 关键作用：2DEG 下方有空穴气
- 极化效应使 GaN NBTI 复杂化

### Other Reliability
- **Current collapse**：陷阱捕获导致电流下降
- **Dynamic Ron**：开关时导通电阻增加
- **Breakdown**：栅介质击穿

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/wide-bandgap]] — 宽禁带半导体
