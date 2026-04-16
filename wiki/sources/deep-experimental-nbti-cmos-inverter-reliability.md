---
title: "Deep Experimental Investigation of NBTI Impact on CMOS Inverter Reliability"
type: source
tags: [nbti, cmos, inverter, circuit-aging, reliability, degradation]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/Deep_experimental_investigation_of_NBTI_impact_on_CMOS_inverter_reliability.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# Deep Experimental Investigation of NBTI Impact on CMOS Inverter Reliability

## Summary
本文通过 **深度实验** 表征了 **NBTI 对 CMOS Inverter 可靠性** 的影响。NBTI 导致 PMOS Vth 正漂移，直接影响 inverter 的 switching threshold 和 noise margin。

## Key Findings

### Inverter Circuit Impact
| Parameter | Fresh | After NBTI Stress | Change |
|-----------|-------|-------------------|--------|
| **Vth,p** | ~-0.4V | ~-0.45V | +50mV |
| **Switching Threshold (V_M)** | Vdd/2 | shifts toward NMOS | Δ ~30mV |
| **Noise Margin NM_H** | ~0.4V | degraded | -10-15% |
| **Propagation Delay** | baseline | increased | +5-10% |

### NBTI-Induced Degradation
- **PMOS Vth shift**：负偏置下空穴被捕获 → Vth 正漂移
- **Switching threshold (V_M)**：向 NMOS 侧漂移
- **Noise margin degradation**：电路对噪声更敏感
- **Delay increase**：上升时间变慢

### Recovery Behavior
- 静态休息时部分恢复
- Recovery 量取决于 stress 时间 vs rest 时间
- AC operation 下 recovery 更显著

### Experimental Setup
- 65nm CMOS 工艺
- Stress: Vdd = 1.2V, T = 125°C, duration 10³-10⁵ s
- Measurement: Vth, V_M, noise margins, propagation delay

## Circuit-Level Impact
```
PMOS NBTI Stress
    ↓
ΔVth_pmos > 0 (positive shift)
    ↓
Switching threshold V_M shifts toward Vss
    ↓
Rise time increases, Fall time relatively unchanged
```

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/circuit-aging]] — Circuit aging overview

## Source
- [Deep_experimental_investigation_of_NBTI_impact_on_CMOS_inverter_reliability.pdf](../../raw/sources/Deep_experimental_investigation_of_NBTI_impact_on_CMOS_inverter_reliability.pdf)
