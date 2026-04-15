---
title: "ESD (Electrostatic Discharge) Protection"
type: concept
tags: [esd, electrostatic-discharge, protection, reliability, diode, scr, tvs, clamping]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/On_The_Interaction_of_ESD_NBTI_and_HCI_in_65nm_Technology.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/hci", "HCI"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# ESD (Electrostatic Discharge) Protection

## Summary
**ESD（静电放电）** 是集成电路的主要可靠性威胁之一——人体或设备积累的静电可在 ns-μs 内对芯片造成毁灭性损伤。ESD 保护电路通过提供**低阻抗放电路径**，将 ESD 电流导向地或 VDD，保护核心电路免受损坏。

## ESD Threat

| 模型 | 电压 | 电流 | 时间常数 |
|------|------|------|---------|
| **HBM** | ±1-15 kV | 0.5-10 A | ~150 ns |
| **MM** | ±100-1000 V | 1-10 A | ~30 ns |
| **CDM** | ±1-2 kV | 10-50 A | <1 ns |

## Protection Structures

### Diode-based Protection
- **Forward-biased diode**：低阻抗通路
- **Dual-diode**：I/O 到 VDD 和 VSS 双向
- **Snapback diode**：用于高速应用

### SCR (Silicon Controlled Rectifier)
- **最高鲁棒性**的 ESD 保护
- **低触发电压**，高电流处理能力
- **Lateral/Vertical SCR** design

### TVS (Transient Voltage Suppressor)
- **Clamping** 机制限制过压
- 用于 board-level 保护

## ESD-NBTI/HCI Interaction
- ESD 造成的微损伤会 **加速 NBTI/HCI 退化**
- 相反，NBTI/HCI 退化后的器件 ESD 阈值**降低**
- **复合失效**：多机制协同导致失效

## Related
- [[concepts/nbti]] — NBTI
- [[concepts/hci]] — HCI
- [[concepts/circuit-aging]] — 电路老化
