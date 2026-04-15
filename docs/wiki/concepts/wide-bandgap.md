---
title: "Wide Bandgap Semiconductor"
type: concept
tags: [wide-bandgap, semiconductor, gan, sic, gan-hemt, power-electronics, breakdown-field]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Role_of_free_holes_in_nBTI_degradation_in_GaN-on-Si_MOS-channel_HEMTs.pdf"]
related: [["concepts/gan-hemt", "GaN HEMT"]]
---

# Wide Bandgap Semiconductor

## Summary
**宽禁带半导体（Wide Bandgap, WBG）** 指禁带宽度显著大于硅（1.1 eV）的半导体材料，主要包括 **SiC（4H-SiC, 3.3 eV）** 和 **GaN（3.4 eV）**。宽禁带带来更高的击穿电场和热导率，使 WBG 器件适合 **高压、高温、高频** 应用。

## Key Materials

| Material | Bandgap | E_br | Mobility | Applications |
|----------|---------|------|---------|-------------|
| **Si** | 1.1 eV | 0.3 MV/cm | 1400 | Logic, Analog |
| **GaAs** | 1.4 eV | 0.4 MV/cm | 8500 | RF, Opto |
| **GaN** | 3.4 eV | 3.3 MV/cm | 2000 | Power, RF |
| **4H-SiC** | 3.3 eV | 2.5 MV/cm | 700 | Power |

## Advantages

### High Breakdown Field
- **GaN E_br ≈ 3.3 MV/cm**（是 Si 的 10 倍）
- 相同耐压下，漂移区（drift region）可以薄 10 倍
- **更小的器件面积**

### High Temperature Operation
- **GaN 可在 400°C+ 工作**（Si 限制在 ~150°C）
- 减少散热系统需求
- 对**汽车、航空**应用重要

### High Frequency
- **GaN 高电子迁移率**：2000 cm²/Vs
- **2DEG** 在 AlGaN/GaN 界面自然形成
- 适合 **5G RF、雷达、卫星通信**

## Applications

| 应用 | SiC | GaN |
|------|-----|-----|
| **EV inverter** | ✓ (1200V+) | ✓ (650V-900V) |
| **PV inverter** | ✓ | ✓ |
| **RF PA** | — | ✓ (5G, radar) |
| **Power supply** | ✓ | ✓ (HF) |

## Reliability Challenges
- [[concepts/gan-hemt]] — GaN HEMT NBTI 机制
- GaN 独特的失效模式：current collapse, dynamic Ron

## Related
- [[concepts/gan-hemt]] — GaN HEMT
