---
title: "Run Time Vth Extraction Based On-Chip NBTI Mitigation Sensor for 6T SRAM Cell"
type: source
tags: [nbti, on-chip-monitor, sram, vth-extraction, sensor, aging-sensor, reliability-monitoring]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Run_Time_V_th_Extraction_Based_On-Chip_NBTI_Mitigation_Sensor_for_6T_SRAM_Cell.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/sram", "SRAM"], ["concepts/on-chip-aging-sensor", "On-Chip Aging Sensor"]]
---

# Run Time Vth Extraction Based On-Chip NBTI Mitigation Sensor for 6T SRAM Cell

## Summary
本文提出一种**基于在线 Vth 提取的片上 NBTI 缓解传感器**，用于 6T SRAM 单元。传感器在运行期间实时监测 SRAM 晶体管的 Vth 漂移，当检测到 NBTI 退化超过阈值时，触发**自适应偏置（adaptive body bias）** 补偿 Vth 变化，延长 SRAM 寿命。

## Key Findings

### On-Chip NBTI Sensor Architecture
1. **Ring oscillator-based sensor**：振荡频率随 Vth 变化
2. **Replica circuit**：复制 SRAM 单元的应力条件
3. **Vth extraction circuit**：实时提取 Vth 值

### 6T SRAM Cell Aging
- **6T SRAM**：6 个晶体管（2 个 access + 4 个 storage）
- **Read/Write 操作都对 PMOS 和 NMOS 施加 NBTI/PBTI stress**
- **Aging asymmetry**：PMOS 主要受 NBTI，NMOS 主要受 PBTI
- **SNM (Static Noise Margin) 退化**：随 Vth 漂移而减小

### NBTI Mitigation via Adaptive Body Bias
- **Forward Body Bias (FBB)**：降低 PMOS Vth，补偿 NBTI 引起的 Vth 增加
- **Reverse Body Bias (RBB)**：增加 NMOS Vth，补偿 PBTI 引起的 Vth 增加
- **Monitoring → Decision → Compensation 闭环控制**

### Sensor Specifications
| 参数 | 值 |
|------|-----|
| **Vth 检测精度** | ±5 mV |
| **更新频率** | 可配置（ms 到 s 级）|
| **功耗 overhead** | < 5% of SRAM array |
| **检测时间** | < 1 μs per cell |

### Lifetime Extension
- **Without mitigation**：10 年后 SNM 退化 20-30%
- **With adaptive body bias**：SNM 退化 < 10%
- **Power cost**：额外功耗 ~3-8% （用于 body bias 控制电路）

## System Integration
- **Per-column or per-bank monitoring**：不监测每个 cell，监测代表性 sample
- **Calibration**：初始 Vth 建立 baseline，定期 re-calibration
- **Temperature compensation**：NBTI 有温度依赖，传感器需补偿

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/sram]] — SRAM 电路
- [[concepts/on-chip-aging-sensor]] — 片上老化传感器

## Source
[Run Time Vth Extraction Based On-Chip NBTI Mitigation Sensor for 6T SRAM Cell](raw/sources/Run_Time_V_th_Extraction_Based_On-Chip_NBTI_Mitigation_Sensor_for_6T_SRAM_Cell.pdf)
