---
title: "Investigation on NBTI Control Techniques of HKMG Transistors for Low-power DRAM Applications"
type: source
tags: [nbti, hkmg, dram, low-power, reliability, transistor, refresh]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/Investigation_on_NBTI_Control_Techniques_of_HKMG_Transistors_for_Low-power_DRAM_applications.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/dram", "DRAM"]]
---

# Investigation on NBTI Control Techniques of HKMG Transistors for Low-power DRAM Applications

## Summary
本文研究了 **HKMG (High-k/Metal Gate) 晶体管** 的 NBTI 控制技术，针对 **低功耗 DRAM** 应用。提出多种 NBTI 抑制方法以延长 DRAM  retention time。

## Key Findings

### HKMG DRAM NBTI Issues
- HKMG 技术的 **EOT scaling** 使 NBTI 更敏感
- **Retention time** 随 NBTI 退化而缩短
- 低功耗 DRAM 需要 **更严格的 NBTI 控制**

### Control Techniques
| Technique | Effect | Implementation |
|-----------|--------|----------------|
| **Fluorine incorporation** | Reduces ΔVth 30-50% | F implantation |
| **Annealing optimization** | Reduces interface traps | Post-nitridation anneal |
| **Channel doping profile** | Reduces peak field | Halo engineering |
| **Gate workfunction tuning** | Reduces effective Vth shift | Metal gate alloying |

### Key Data
- **ΔVth reduction**：最佳条件下可达 50%
- **Retention time improvement**：从 32ms 恢复至接近 64ms
- **Trade-off**：某些技术可能影响 performance

### Low-Power DRAM Requirements
- **Vdd scaling** 有助于减少 NBTI（但影响 speed）
- **Body bias** 控制可以缓解 degradation
- **Refresh frequency** 需要动态调整

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/dram]] — DRAM structure

## Source
- [Investigation_on_NBTI_Control_Techniques_of_HKMG_Transistors_for_Low-power_DRAM_applications.pdf](../../raw/sources/papers-onedrive/Investigation_on_NBTI_Control_Techniques_of_HKMG_Transistors_for_Low-power_DRAM_applications.pdf)
