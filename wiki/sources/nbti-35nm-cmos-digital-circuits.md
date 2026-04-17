---
title: "Impact of NBTI on the Performance of 35nm CMOS Digital Circuits"
type: source
tags: [nbti, 35nm, cmos, digital-circuit, circuit-aging, reliability, threshold-voltage, delay]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/Impact_of_NBTI_on_the_performance_of_35nm_CMOS_digital_circuits.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# Impact of NBTI on the Performance of 35nm CMOS Digital Circuits

## Summary
本文分析了 **NBTI 对 35nm CMOS 数字电路** 的时域性能退化。10 年工作后电路延时增加 13-17%，是 **65nm 以下节点最重要的可靠性限制因素**。

## Key Findings

### 35nm Technology NBTI Data
| Parameter | Value |
|-----------|-------|
| **PMOS Vth shift** | ~50mV @ 10yr, 125°C |
| **Circuit delay increase** | 13-17% @ 10yr |
| **Ring Oscillator freq. degradation** | ~8% @ 10yr |
| **Path delay degradation** | 8-15% at 125°C, 10yr |
| **Frequency acceleration factor (k)** | 0.12 for DC stress |

### NBTI as Lifetime Limiter
- **65nm 以下**：NBTI 取代 HCI 成为主要可靠性问题
- 10 年运行后 **timing degradation 可达 10-20%**
- 需要在设计中预留 **timing margin**

### Process Variability Impact
- NBTI 退化呈 **对数正态分布（LogN）**
- 工艺变异性导致不同芯片退化量不同
- 需要考虑 **worst-case corner** 设计

### Circuit-Level Degradation
- **Critical path delay** 增加最显著
- **Ring oscillator** 频率下降可作为 on-chip monitor
- **Setup/hold time** 退化影响时序裕量

## Temperature & Voltage Dependence
- 温度升高加速 NBTI（Arrhenius 关系）
- Vdd 降低时 NBTI 相对影响更显著（同等 Vth 漂移占比更大）

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/circuit-aging]] — Circuit aging overview

## Source
- [Impact_of_NBTI_on_the_performance_of_35nm_CMOS_digital_circuits.pdf](../../raw/sources/papers-onedrive/Impact_of_NBTI_on_the_performance_of_35nm_CMOS_digital_circuits.pdf)
