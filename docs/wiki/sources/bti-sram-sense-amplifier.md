---
title: "BTI Impact on SRAM Sense Amplifier"
type: source
tags: [sram, sense-amplifier, bti, nbti, pbti, read-margin, circuit-reliability, aging]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/BTI_impact_on_SRAM_sense_amplifier.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/pbti", "PBTI"], ["concepts/sram", "SRAM"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# BTI Impact on SRAM Sense Amplifier

## Summary
本文研究 **BTI（NBTI 和 PBTI）对 SRAM sense amplifier（灵敏放大器）** 的影响。关键发现：BTI 退化导致 **SRAM read margin 下降**，sense amplifier 的失调电压（offset voltage）随时间增加，严重时导致 read failure。

## Key Findings

### SRAM Sense Amplifier Overview
- **Sense amplifier**：检测 bitline 差分电压，快速放大到 full-swing 信号
- **SRAM read 过程**：
  1. Wordline 选通 → bitline 充电/放电
  2. Bitline 差分电压 ΔV_BL 很小（~100 mV）
  3. Sense amplifier 检测 ΔV_BL 并放大
- **Read margin**：保证正确 read 的最小 ΔV_BL

### BTI Impact on Sense Amplifier
| BTI Type | Affected Transistor | Effect |
|----------|-------------------|--------|
| **NBTI** | PMOS load | Vth 增加（less negative）→ 驱动能力下降 |
| **PBTI** | NMOS access / drive | Vth 增加 → 驱动能力下降 |

### Offset Voltage (Voffset) Degradation
- Sense amplifier 的 **Voffset** 由晶体管匹配的差异决定
- BTI 退化 **不均匀**（不同晶体管退化量不同）
- **Voffset 增加** → sense amplifier 区分 ΔV_BL 的能力下降
- 当 Voffset > ΔV_BL 时 → **read failure**

### Read Current Degradation
- **Bitcell read current I_READ** 退化（access transistor NBTI/PBTI）
- **Sense amplifier pull-up/pull-down** 退化（NBTI/PBTI）
- I_READ 退化 → ΔV_BL 变小 → read margin 下降

### SNM (Static Noise Margin) Impact
- SRAM 的 **SNM** 是衡量 read stability 的关键指标
- BTI 退化使 **SNM 减小**（worst case 退化可达 20-30%）
- **Hold margin** 和 **read margin** 都受影响

## Aging vs. Fresh Circuit

| 参数 | Fresh | After BTI Aging |
|------|-------|-----------------|
| **Voffset** | ~10-20 mV | ~30-50 mV |
| **Read margin** | 100% | 70-80% |
| **SNM** | 100% | 70-80% |
| **Failure time** | — | 数年（取决于 stress）|

## Mitigation Techniques
- **Read-assist techniques**：辅助 read 电路
- **BTI-aware design**：预留更多 margin
- **Body biasing**：调节 Vth 补偿 BTI 退化

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/pbti]] — PBTI 机制
- [[concepts/sram]] — SRAM 电路
- [[concepts/circuit-aging]] — 电路老化

## Source
[BTI Impact on SRAM Sense Amplifier](raw/sources/BTI_impact_on_SRAM_sense_amplifier.pdf)
