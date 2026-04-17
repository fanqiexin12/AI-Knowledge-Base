---
title: "Impact of NBTI on the Temporal Performance Degradation of Digital Circuits"
type: source
tags: [nbti, temporal-degradation, digital-circuit, circuit-aging, recovery, reliability]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/Impact_of_NBTI_on_the_temporal_performance_degradation_of_digital_circuits.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# Impact of NBTI on the Temporal Performance Degradation of Digital Circuits

## Summary
本文研究了 **NBTI 导致数字电路时域性能退化** 的定量分析。10 年运行后电路速度退化 15-20%，且存在 **25-40% 的恢复效应**。

## Key Findings

### Temporal Degradation Data
| Parameter | Value |
|-----------|-------|
| **Circuit speed degradation** | 15-20% over 10 years |
| **PMOS Vth shift** | 30-100mV over 10 years |
| **Recovery fraction** | 25-40% (during idle periods) |
| **Activation energy** | 0.12 eV |
| **Worst-case degradation** | ~20% @ 10yr |

### Recovery Effect
- **idle 期间可恢复 25-40%** 的性能退化
- Recovery 时间常数与 stress 时间相关
- 设计意义：间歇性工作比连续工作寿命更长

### Voltage Dependence
- **低 Vdd 下 NBTI 影响更显著**
- 原因：同等 Vth 漂移在低电压下占 Ir drop 比例更大
- 低功耗设计中 NBTI 需要特别关注

### Temperature Dependence
- **激活能 0.12 eV**
- 高温加速 NBTI 退化
- 芯片散热设计影响可靠性寿命

## Lifetime Projection
```
Fresh → 5yr → 10yr → 15yr → 20yr
 0%   5-8%  15-20%  20-25%  25-30%  (delay increase)
```

## Mitigation Considerations
- 设计时预留 **15-20% timing margin**
- 散热优化延长使用寿命
- 低功耗模式减少 NBTI 累积

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/circuit-aging]] — Circuit aging overview

## Source
- [Impact_of_NBTI_on_the_temporal_performance_degradation_of_digital_circuits.pdf](../../raw/sources/papers-onedrive/Impact_of_NBTI_on_the_temporal_performance_degradation_of_digital_circuits.pdf)
