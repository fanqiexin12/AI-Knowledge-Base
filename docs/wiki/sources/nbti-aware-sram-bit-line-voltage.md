---
title: "NBTI-Aware Bit Line Voltage Control with Boosted Supply Voltage for 6T SRAM Cell Read Stability"
type: source
tags: [nbti, sram, bit-line, read-stability, voltage-control, reliability]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/NBTI-aware_bit_line_voltage_control_with_boosted_supply_voltage_for_improvement_of_6T_SRAM_cell_read_stability.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/sram", "SRAM"]]
---

# NBTI-Aware Bit Line Voltage Control with Boosted Supply Voltage for 6T SRAM Cell Read Stability

## Summary
本文提出 **NBTI 感知的位线电压控制** 方法，使用 **升压 Vdd** 来补偿 NBTI 导致的 SRAM read stability 退化。

## Key Findings

### NBTI Impact on SRAM Read
- NBTI → PMOS Vth ↑ → pull-up strength ↓
- **Read stability (SNM) 退化**
- 位线电压控制可以补偿这一效应

### Proposed Scheme
| Technique | Description |
|-----------|-------------|
| **Bit-line voltage boosting** | Raise BL/BLB during read |
| **NBTI-aware Vdd** | Dynamically adjust Vdd based on age |
| **Read margin recovery** | SNM improvement ~15-20% |

### Mechanism
```
NBTI degradation detected (via RO sensor)
    ↓
Calculate required Vdd boost
    ↓
Apply boosted Vdd during read operation
    ↓
Compensate for reduced pull-up strength
```

### Trade-offs
- **Power increase**：升压增加动态功耗
- **Read/write conflict**：需要平衡读/写操作
- **Aging monitoring**：需要可靠的 NBTI 传感器

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/sram]] — SRAM cell structure

## Source
- [NBTI-aware_bit_line_voltage_control_with_boosted_supply_voltage_for_improvement_of_6T_SRAM_cell_read_stability.pdf](../../raw/sources/papers-onedrive/NBTI-aware_bit_line_voltage_control_with_boosted_supply_voltage_for_improvement_of_6T_SRAM_cell_read_stability.pdf)
