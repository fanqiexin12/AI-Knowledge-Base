---
title: "SRAM (Static Random Access Memory)"
type: concept
tags: [sram, memory, 6t-sram, read-margin, write-margin, snm, sense-amplifier, bti, aging]
created: 2026-04-14
updated: 2026-04-16
sources: ["raw/sources/BTI_impact_on_SRAM_sense_amplifier.pdf", "raw/sources/Run_Time_V_th_Extraction_Based_On-Chip_NBTI_Mitigation_Sensor_for_6T_SRAM_Cell.pdf", "raw/sources/papers-onedrive/Impacts_of_NBTI_and_PBTI_on_ultra-thin-body_GeOI_6T_SRAM_cells.pdf", "raw/sources/papers-onedrive/Signal_probability_control_for_relieving_NBTI_in_SRAM_cells.pdf", "raw/sources/papers-onedrive/Reliable_cache_design_with_on-chip_monitoring_of_NBTI_degradation_in_SRAM_cells_using_BIST.pdf", "raw/sources/papers-onedrive/NBTI-aware_bit_line_voltage_control_with_boosted_supply_voltage_for_improvement_of_6T_SRAM_cell_read_stability.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/circuit-aging", "Circuit Aging"], ["concepts/sense-amplifier", "Sense Amplifier"]]
---

# SRAM (Static Random Access Memory)

## Summary
**SRAM** 是六晶体管（6T）结构的静态随机存取存储器，与 DRAM 不同，SRAM 不需要刷新，只要通电就能保持数据。其**单元面积大、功耗高**，但速度最快，用于 CPU cache 等需要高速存取的场景。

## 6T SRAM Cell

```
       WL
        |
   -----|----- M4         M6 ---- VDD
        |      |           |
       M1      M3           M5
        |      |           |
   -----|----- PL ---------|----- BL
        |                    |
       M2      |           M5
        |      |           |
   -----|----- NL ---------|----- BLB
```

- **M1/M2**：pull-down (NMOS)
- **M3/M4**：pull-up (PMOS)
- **M5/M6**：access transistor (NMOS)
- **BL, BLB**：bitline pair
- **WL**：wordline

## SRAM Metrics

### SNM (Static Noise Margin)
- SRAM 抗噪声能力的度量
- **Hold SNM**：保持数据需要的最小噪声
- **Read SNM**：读操作时保持数据的能力
- **Write SNM**：写操作成功需要的最小噪声

### BTI Aging Impact
- **NBTI** 使 M3/M4 Vth ↑（less negative）→ pull-up 变弱 → **read SNM 退化**
- **PBTI** 使 M1/M2/M5/M6 Vth ↑ → pull-down/access 变弱
- **Sense amplifier offset** 增加 → read 可靠性下降

## GeOI SRAM
- **Germanium-on-Insulator** SRAM 有更高迁移率，但界面态密度更高
- NBTI/PBTI 影响更显著：125°C 下 10⁶ 秒后 SNM 失效
- Access transistor 同时受 NBTI + PBTI 影响

## NBTI Mitigation in SRAM

### Signal Probability Control
- 数据模式影响 NBTI 退化：Node "0" probability 越高，stress 时间越长
- **Data inversion** 和 **wear leveling** 可减少退化 20-40%

### Bit-line Voltage Boosting
- NBTI 感知的位线电压控制：检测到退化后升压 Vdd 补偿
- **Read stability** 改善 15-20%

### Cache BIST Monitoring
- BIST 嵌入 ring oscillator 传感器监测 NBTI
- 退化超过阈值时触发数据迁移或 way swapping
- **Lifetime extension** 2-3x

### 6T vs 8T SRAM
- **6T**：标准单元，面积小
- **8T**：分离 read port，改善 read stability

## Related
- [[concepts/nbti]] — NBTI 影响
- [[concepts/circuit-aging]] — 电路老化
- [[concepts/sense-amplifier]] — 灵敏放大器
