---
title: "Reliable Cache Design with On-Chip Monitoring of NBTI Degradation in SRAM Cells Using BIST"
type: source
tags: [nbti, sram, cache, bist, on-chip-monitor, reliability, aging-sensor]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/Reliable_cache_design_with_on-chip_monitoring_of_NBTI_degradation_in_SRAM_cells_using_BIST.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/sram", "SRAM"], ["concepts/on-chip-aging-sensor", "On-chip Aging Sensor"]]
---

# Reliable Cache Design with On-Chip Monitoring of NBTI Degradation in SRAM Cells Using BIST

## Summary
本文提出了一种 **可靠的 Cache 设计**，使用 **BIST (Built-In Self-Test)** 片上监测 NBTI 退化。当检测到 NBTI 退化超过阈值时，触发预警或数据迁移。

## Key Findings

### BIST Architecture for NBTI Monitoring
- **Ring oscillator sensors** 嵌入在 cache 周围
- **定期测量** 频率漂移来估算 NBTI 退化
- **阈值报警** 当 degradation 超过预设值

### Monitoring Scheme
| Component | Function |
|-----------|----------|
| **RO sensors** | Frequency measurement |
| **Comparator** | Compare with fresh reference |
| **Counter/Logic** | Accumulate degradation |
| **Alert signal** | Trigger when threshold exceeded |

### Key Data
- **Detection resolution**：~1mV Vth shift
- **Update interval**：可配置 (ms to hours)
- **Power overhead**：< 1% of cache power

### Reliability Management
- **Data migration**：当 NBTI 严重时迁移到 fresher cache line
- **Way swapping**：将高退化 way 替换为低退化 way
- **Predictive maintenance**：预测剩余寿命

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/sram]] — SRAM cell structure
- [[concepts/on-chip-aging-sensor]] — On-chip aging sensors

## Source
- [Reliable_cache_design_with_on-chip_monitoring_of_NBTI_degradation_in_SRAM_cells_using_BIST.pdf](../../raw/sources/papers-onedrive/Reliable_cache_design_with_on-chip_monitoring_of_NBTI_degradation_in_SRAM_cells_using_BIST.pdf)
