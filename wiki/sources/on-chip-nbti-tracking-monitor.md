---
title: "A Simple Monitor for Tracking NBTI in Integrated Systems"
type: source
tags: [nbti, on-chip-monitor, tracking, ring-oscillator, reliability, icn, in-circuit-nbti, aging-sensor]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/A_Simple_Monitor_for_Tracking_NBTI_in_Integrated_Systems.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/on-chip-aging-sensor", "On-Chip Aging Sensor"]]
---

# A Simple Monitor for Tracking NBTI in Integrated Systems

## Summary
本文提出一种**简单的片上 NBTI 监测器（ICN - In-Circuit NBTI monitor）**，用于集成系统中的实时 NBTI tracking。该监测器基于 **ring oscillator** 频率变化，可在产品现场（field）监测 NBTI 退化，无需中断系统运行。

## Key Findings

### Ring Oscillator Based NBTI Monitor
- **Ring oscillator**：奇数个反相器首尾相连 → 振荡
- **Frequency f = 1/(N × td)**：N = 反相器级数，td = 单级延迟
- **NBTI effect**：PMOS Vth ↑ → td ↑ → f ↓
- **Frequency shift Δf/f**：直接反映 NBTI 退化

### Monitor Design
- **Replica circuits**：复制关键路径的 transistor 条件
- **Stress monitoring circuits**：施加 stress 并测量响应
- **Temperature compensation**：内置温度传感器补偿 T 依赖

### Why Ring Oscillator?
- **Simple**：只需反相器和 counter
- **On-chip**：不需外部测量设备
- **Fast readout**：频率变化实时反映 NBTI
- **Technology-portable**：设计原则适用于各种工艺节点

### Measurement Accuracy
| Parameter | Value |
|-----------|-------|
| **Sensitivity** | ~1 MHz shift per 10 mV Vth change |
| **Resolution** | ±2 mV (Vth) |
| **Measurement time** | 1 ms - 1 s |
| **Power consumption** | < 100 μW |

### System Integration
- **Per-core monitors**：每个 CPU/GPU core 一个监测器
- **Network-on-Chip (NoC) monitoring**：监测互连老化
- **PMU (Power Management Unit)** 集成：动态调节 V/f

### NBTI vs Actual Product Aging
- **Monitor 测得 Δf/f** → 推断 PMOS/NMOS Vth 变化
- **Circuit-level aging** → 从 Vth 变化计算 timing margin
- **Lifetime estimation** → 结合加速因子模型外推

## Comparison with Other Approaches
| 方法 | 精度 | 复杂度 | 适用场景 |
|------|------|--------|---------|
| **Ring oscillator** | 中等 | 低 | 大规模现场监测 |
| **Direct Vth extraction** | 高 | 高 | 精确表征 |
| **IDDQ** | 低 | 中 | 快速筛选 |

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/on-chip-aging-sensor]] — 片上老化传感器

## Source
[A Simple Monitor for Tracking NBTI in Integrated Systems](raw/sources/A_Simple_Monitor_for_Tracking_NBTI_in_Integrated_Systems.pdf)
