---
title: "On The Interaction of ESD, NBTI, and HCI in 65nm Technology"
type: source
tags: [esd, nbti, hci, interaction, circuit-reliability, electrostatic-discharge, 65nm, compound-failure]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/On_The_Interaction_of_ESD_NBTI_and_HCI_in_65nm_Technology.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/hci", "HCI"], ["concepts/esd", "ESD (Electrostatic Discharge)"]]
---

# On The Interaction of ESD, NBTI, and HCI in 65nm Technology

## Summary
本文研究 **ESD（静电放电）、NBTI 和 HCI 三种可靠性机制之间的相互作用**。三种机制并非独立存在——**ESD stress 会加速后续的 NBTI/HCI 退化**，反之 NBTI/HCI 退化后的器件对 ESD 更敏感。65nm 节点下这种相互作用尤为显著。

## Key Findings

### Three Reliability Mechanisms

| Mechanism | Trigger | Damage Type |
|-----------|---------|-------------|
| **ESD** | 静电放电（ns-μs）| 栅氧化层击穿、金属熔化、结退化 |
| **NBTI** | 负偏置+高温（s-h）| 界面态、阈值电压漂移 |
| **HCI** | 高 Vds 热载流子（s-h）| 氧化层陷阱、热载流子注入 |

### ESD-NBTI Interaction
- **ESD 瞬间高电流**可能在栅氧化层引入 **微缺陷（micro-defects）**
- 这些微缺陷成为 **NBTI 退化的 sites** → NBTI 加速
- **反之**：NBTI 退化后的器件，栅氧化层质量已降低 → ESD 鲁棒性下降

### ESD-HCI Interaction
- **ESD 电流脉冲**产生的 **局部加热（self-heating）** 可能损伤沟道
- HCI 敏感区域（漏端高电场区）在 ESD 期间受额外应力
- **复合效应**：ESD + HCI 协同造成比单独任一机制更严重的退化

### Time Sequence Effects
- **ESD first → then NBTI/HCI**：ESD 造成的初始损伤加速后续退化
- **NBTI/HCI first → then ESD**：预先退化的器件 ESD 阈值降低
- **Real-world scenario**：器件一生经历多次 ESD events + 长期 NBTI/HCI stress

### Compound Failure Mode
- **单一机制**：每种机制本身可能未达失效阈值
- **复合作用**：多种机制叠加 → 总退化超过失效阈值
- **设计挑战**：需要同时考虑所有机制的综合影响

### 65nm Node Specific Issues
- **更薄栅氧化层**：更敏感于 ESD 和 NBTI
- **更高电场**：HCI 和 NBTI 更容易触发
- **Layout 依赖性**：ESD 电流路径和 NBTI stress 分布可能重叠

## Reliability Co-Design Implication
- **ESD protection circuits** 需要考虑长期 aging 的影响
- **Aging-aware ESD design**：在产品生命周期结束时 ESD 仍然有效
- **NBTI/HCI hardening** 同时改善 ESD 鲁棒性

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/hci]] — HCI 机制
- [[concepts/esd]] — ESD 保护

## Source
[On The Interaction of ESD, NBTI and HCI in 65nm Technology](raw/sources/On_The_Interaction_of_ESD_NBTI_and_HCI_in_65nm_Technology.pdf)
