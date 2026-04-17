---
title: "On-Chip Aging Sensor"
type: concept
tags: [on-chip, aging-sensor, ring-oscillator, nbti, reliability-monitor, sensor, icn, bti-sensor]
created: 2026-04-14
updated: 2026-04-16
sources: ["raw/sources/A_Simple_Monitor_for_Tracking_NBTI_in_Integrated_Systems.pdf", "raw/sources/Run_Time_V_th_Extraction_Based_On-Chip_NBTI_Mitigation_Sensor_for_6T_SRAM_Cell.pdf", "raw/sources/papers-onedrive/Reliable_cache_design_with_on-chip_monitoring_of_NBTI_degradation_in_SRAM_cells_using_BIST.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# On-Chip Aging Sensor

## Summary
片上老化传感器是集成在芯片内部、用于实时监测器件/电路老化（主要是 NBTI）的电路模块。相比外部测试设备，片上传感器能够**在真实工作条件下追踪老化**，为 adaptive mitigation（如动态调节 V/f）提供反馈。

## Types of On-Chip Aging Sensors

### 1. Ring Oscillator (RO)-based Sensor
- **原理**：RO 频率 f ∝ 1/td，td ∝ 1/gm ∝ Vth
- **NBTI 效应**：PMOS/NMOS Vth ↑ → td ↑ → f ↓
- **优点**：结构简单，digital readout
- **应用**：NBTI、HCI、EM 监测

### 2. Replica Circuit Sensor
- **原理**：复制关键路径的 transistor stress conditions
- **测量**：stress 后的 Vth 或 delay 变化
- **优点**：更准确反映实际 circuit aging

### 3. Vth Extraction Sensor
- **原理**：在线提取 Vth（无需中断 stress）
- **方法**：电流比较、电压比较
- **优点**：直接测量 Vth

### 4. IDDQ Sensor
- **原理**：监测泄漏电流变化
- **优点**：简单
- **缺点**：对 NBTI 不敏感

## System Integration

| 应用 | 传感器位置 | 响应 |
|------|-----------|------|
| **Per-core** | 每个 CPU/GPU core | DVFS 调节 |
| **NoC** | 互连网络 | 降频保护 |
| **SRAM** | cache 阵列 | ECC/repair 触发 |

## Key Specifications

| 参数 | Ring Oscillator | Vth Extraction |
|------|----------------|----------------|
| **Sensitivity** | ~1 MHz/mV | ±2 mV |
| **Resolution** | ±5 mV | ±2 mV |
| **Area** | < 0.01 mm² | 0.05-0.1 mm² |
| **Power** | < 100 μW | < 1 mW |

## Related
- [[concepts/nbti]] — NBTI
- [[concepts/circuit-aging]] — 电路老化
