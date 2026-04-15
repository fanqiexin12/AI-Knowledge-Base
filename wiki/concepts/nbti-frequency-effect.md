---
title: "NBTI Frequency Effect"
type: concept
tags: [nbti, frequency-dependence, ac-nbti, recovery, high-frequency, circuit-delay]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Delay_effects_and_frequency_dependence_of_NBTI_with_sub-microsecond_measurements.pdf", "raw/sources/Reliability_analysis_of_CMOS_inverter_subjected_to_AC_amp_DC_NBTI_stresses.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/ac-nbti", "AC NBTI"]]
---

# NBTI Frequency Effect

## Summary
NBTI 退化具有**强烈的频率依赖性**：频率越高，NBTI 效应越弱。在 f > 1 MHz 时恢复时间充足，NBTI 退化可忽略。DC stress 是 worst case，AC stress 下 NBTI 效果受 duty cycle 和频率调制。

## Frequency Dependence Summary

| Frequency | NBTI Impact | Recovery |
|-----------|-------------|----------|
| **DC** | Maximum | None |
| **< 1 MHz** | Significant | Insufficient |
| **> 1 MHz** | Negligible | Sufficient |
| **> 10 MHz** | Minimal | Near-complete |

## Mechanism

### Recovery During OFF-Phase
- AC stress 下，stress-free intervals 提供恢复时间
- Recovery ~ t^α（功率律，α ≈ 0.1–0.3）
- 脉冲宽度（pulse width）和占空比（duty cycle）共同决定 recovery 量

### Frequency Tradeoff
```
Higher frequency → Shorter stress pulses → Less cumulative damage
                 → Longer recovery intervals → More complete recovery
```

## AC NBTI Characteristics

### Phase-Dependent Stress
- **V_in = high**：PMOS NBTI（Vgs < 0），NMOS no stress
- **V_in = low**：NMOS PBTI（Vgs > 0），PMOS no stress

### Duty Cycle Impact
- **50% duty cycle**：两种应力时间相等
- **> 50%**：PMOS 应力更多 → τpLH 主要退化
- **< 50%**：NMOS 应力更多 → τpHL 主要退化

## Circuit Implications

### Delay Degradation
- NBTI → ΔVth ↑ → τp (propagation delay) ↑
- Delay degradation 也表现出频率依赖性
- 高频电路 → less delay degradation

### DC = Worst Case
- DC stress 用于 NBTI 加速测试（提供 upper bound）
- 实际 AC 使用场景的退化 <= DC stress 结果

## Key References
- DC NBTI → PMOS dominates (VM shifts toward NMOS)
- AC NBTI → PMOS NBTI + NMOS PBTI both contribute
- Frequency > 1 MHz → NBTI effect becomes negligible

## Related
- [[concepts/nbti]] — NBTI 基础机制
- [[concepts/ac-nbti]] — AC NBTI 详细讨论
- [[concepts/circuit-aging]] — 电路级老化效应
