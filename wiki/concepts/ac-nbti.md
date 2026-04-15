---
title: "AC NBTI"
type: concept
tags: [nbti, ac-stress, duty-cycle, pbti, circuit-aging, reliability]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Delay_effects_and_frequency_dependence_of_NBTI_with_sub-microsecond_measurements.pdf", "raw/sources/Reliability_analysis_of_CMOS_inverter_subjected_to_AC_amp_DC_NBTI_stresses.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nbti-frequency-effect", "NBTI Frequency Effect"], ["concepts/pbti", "PBTI"]]
---

# AC NBTI

## Summary
AC NBTI 指电路在**交流信号**（周期性切换）工作条件下的 NBTI 退化。与 DC NBTI 不同，AC NBTI 涉及两种 phase 的交替：**PMOS NBTI**（V_in = high）和 **NMOS PBTI**（V_in = low），两者共同贡献电路老化。

## AC Stress Phases

| Phase | PMOS | NMOS |
|-------|------|------|
| **V_in = high** | NBTI stress | No stress |
| **V_in = low** | No stress | PBTI stress |

## DC vs AC Comparison

| | DC NBTI | AC NBTI |
|---|---|---|
| **主导器件** | PMOS only | PMOS + NMOS |
| **退化量** | Maximum (worst case) | Lower (recovery during opposite phase) |
| **VM shift** | Toward NMOS | Toward NMOS (combined effect) |
| **τpHL impact** | Minimal | Significant (NMOS PBTI) |
| **τpLH impact** | Significant (PMOS NBTI) | Significant |
| **测试方法** | Static stress | Pulsed / AC |

## Duty Cycle Effects

- **50% duty cycle**：PMOS 和 NMOS 各承受 50% 的应力时间
- **High duty cycle (> 50%, V_in 偏向 high)**：PMOS 应力时间更长 → τpLH 退化为主
- **Low duty cycle (< 50%, V_in 偏向 low)**：NMOS 应力时间更长 → τpHL 退化为主

## Recovery Mechanism

- **Opposite phase 提供 recovery 时间**
- Recovery 功率律：ΔVth_recovery ~ t^α
- 频率越高 → recovery 时间比例越高 → 净退化越低

## CMOS Inverter AC NBTI

### Trip Point (VM) Shift
- PMOS NBTI → PMOS Vth ↑（less negative）
- NMOS PBTI → NMOS Vth ↑
- Combined effect: **VM shifts toward NMOS direction**
- VM 偏离 VDD/2 → noise margin 降低

### Delay Asymmetry
- τpLH (low→high): PMOS 主导 → AC NBTI 使其 ↑
- τpHL (high→low): NMOS 主导 → AC NBTI 使其 ↑ (via NMOS PBTI)
- 上升/下降 transition 时间变得不对称

## Practical Implications

1. **实际电路多工作在 AC 模式**，而非 DC
2. **DC stress 给出老化 upper bound**
3. **频率决定 recovery 量**：高频 > 低频 > DC
4. **Analog 电路**：DC 偏置点附近工作 → 更接近 DC NBTI
5. **数字电路**：频繁切换 → NBTI 影响被 recovery 缓解

## Related
- [[concepts/nbti]] — NBTI 基础机制
- [[concepts/nbti-frequency-effect]] — 频率依赖性
- [[concepts/pbti]] — PBTI（AC stress 中 NMOS 承受的机制）
