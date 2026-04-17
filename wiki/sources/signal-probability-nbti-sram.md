---
title: "Signal Probability Control for Relieving NBTI in SRAM Cells"
type: source
tags: [nbti, sram, signal-probability, reliability, circuit-aging, duty-cycle]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/Signal_probability_control_for_relieving_NBTI_in_SRAM_cells.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/sram", "SRAM"]]
---

# Signal Probability Control for Relieving NBTI in SRAM Cells

## Summary
本文提出 **信号概率控制 (Signal Probability Control)** 方法来缓解 SRAM 单元的 NBTI 退化。通过优化 SRAM 数据模式降低 NBTI stress duty cycle。

## Key Findings

### Signal Probability Impact
- SRAM 存储的 **数据模式** 影响 NBTI 退化量
- **Node "0" probability** (PN0)：节点保持 0 的时间比例
- **PN0 越高** → NBTI stress 时间越长 → 退化越严重

### NBTI-Aware Data Patterning
| Data Pattern | PMOS NBTI Impact |
|--------------|-----------------|
| **All "0"** | Maximum (always stress) |
| **All "1"** | Minimum (PMOS off) |
| **Random** | Average |
| **NBTI-optimized encoding** | 20-30% reduction |

### Mitigation Techniques
1. **Data inversion**：动态反转数据使 PMOS stress 平衡
2. **Read/write scheduling**：减少"0"节点的持续时间
3. **Error correction**：允许一定错误率换取可靠性
4. **Wear leveling**：将频繁访问的数据分散到不同 cell

### Key Results
- **NBTI degradation reduction**：20-40%
- **Timing margin improvement**：~10%
- **Overhead**：需要额外的 control logic

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/sram]] — SRAM cell structure

## Source
- [Signal_probability_control_for_relieving_NBTI_in_SRAM_cells.pdf](../../raw/sources/papers-onedrive/Signal_probability_control_for_relieving_NBTI_in_SRAM_cells.pdf)
