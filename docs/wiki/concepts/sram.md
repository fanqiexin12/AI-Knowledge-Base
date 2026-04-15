---
title: "SRAM (Static Random Access Memory)"
type: concept
tags: [sram, memory, 6t-sram, read-margin, write-margin, snm, sense-amplifier, bti, aging]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/BTI_impact_on_SRAM_sense_amplifier.pdf", "raw/sources/Run_Time_V_th_Extraction_Based_On-Chip_NBTI_Mitigation_Sensor_for_6T_SRAM_Cell.pdf"]
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

### 6T vs 8T SRAM
- **6T**：标准单元，面积小
- **8T**：分离 read port，改善 read stability

## Related
- [[concepts/nbti]] — NBTI 影响
- [[concepts/circuit-aging]] — 电路老化
- [[concepts/sense-amplifier]] — 灵敏放大器
