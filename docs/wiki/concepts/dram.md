---
title: "DRAM"
type: concept
tags: [dram, memory, nbti, retention, refresh, reliability]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/A_Comprehensive_Review_of_DRAM_NBTI_Issues_and_Solutions.pdf", "raw/sources/papers-onedrive/Investigation_on_NBTI_Control_Techniques_of_HKMG_Transistors_for_Low-power_DRAM_applications.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/sram", "SRAM"]]
---

# DRAM (Dynamic Random Access Memory)

## Summary
**DRAM** 使用 1T1C（一个晶体管 + 一个电容）结构存储每一位数据。由于 DRAM cell 中的 pMOS access transistor 受 NBTI 影响，其 retention time 会随时钟累积而退化，需要通过更频繁的 refresh 来补偿。

## DRAM Cell Structure

```
Word Line ──┬── Gate of Access FET
            │
            ├──→  Source/Drain  ──→ Bit Line
            │
            └──→  Drain/Source
                  │
              Capacitor ──→ Storage Node (1 or 0)
```

## NBTI Impact on DRAM

### Primary Degradation
- pMOS access transistor Vth increases (positive shift) due to NBTI
- Cell discharge rate increases → retention time decreases

### Symptoms
| Degradation | Impact |
|-------------|--------|
| Retention time ↓ | Refresh interval must decrease |
| Write margin ↓ | Write failures at low Vdd |
| Read disturb ↑ | Half-selected cells may flip |

### Timeline
- Fresh: retention time ~64ms
- After 10yr NBTI: retention time ~32ms or less
- Requires **adaptive refresh** to maintain data integrity

## DRAM Types

| Type | Structure | NBTI Severity |
|------|----------|---------------|
| **1T1C** | 1 transistor + 1 capacitor | High |
| **3T** | 3 transistors, no capacitor | Medium |
| **Gain Cell** | Read transistor separated | Medium |
| **eDRAM** | Embedded DRAM (similar to 1T1C) | High |

## Mitigation Strategies

- **Adaptive refresh**: increase refresh frequency as NBTI accumulates
- **ECC**: error correction codes for occasional read errors
- **Word-line boosting**: increase write voltage
- **Fluorine incorporation**: process-level NBTI reduction
- **Wear leveling** in memory controller

## HKMG DRAM NBTI Control

- **EOT scaling** 使 HKMG DRAM 的 NBTI 更敏感
- **Fluorine注入** 可减少 ΔVth 30-50%，retention time 恢复接近 64ms
- **Annealing优化**：减少界面态密度
- **Channel掺杂profile**：Halo工程减少峰值电场
- **Body bias控制**：动态调整补偿退化

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/sram]] — SRAM (related but different memory)
