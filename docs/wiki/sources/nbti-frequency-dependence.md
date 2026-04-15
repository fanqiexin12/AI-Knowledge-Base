---
title: "Delay Effects and Frequency Dependence of NBTI with Sub-microsecond Measurements"
type: source
tags: [nbti, frequency-dependence, high-frequency, circuit-delay, ac-nbti, recovery, pulse-measurement]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Delay_effects_and_frequency_dependence_of_NBTI_with_sub-microsecond_measurements.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nbti-frequency-effect", "NBTI Frequency Effect"]]
---

# Delay Effects and Frequency Dependence of NBTI with Sub-microsecond Measurements

## Summary
本文研究 **高频工作条件下（sub-μs 脉冲，上限 10 MHz）NBTI 退化**及其对电路 **propagation delay** 的影响。核心发现：**NBTI 效应随频率增加而减弱**，在 f > 1 MHz 时基本消失；DC stress 是 worst case；AC stress 下恢复时间（recovery time）是关键因素。

## Key Findings

### Frequency Dependence
| Frequency | NBTI Effect | 原因 |
|-----------|-------------|------|
| **DC** | 最大 | 无恢复时间 |
| **< 1 MHz** | 显著 | 恢复时间不足 |
| **> 1 MHz** | 可忽略 | 脉冲间隔足够恢复 |
| **> 10 MHz** | 最小 | 极短应力时间 |

### Recovery Mechanism
- **功率律恢复**：恢复 ~ t^α（α ≈ 0.1–0.3）
- Recovery occurs during OFF-phase（stress-free intervals）
- 脉冲宽度（pulse width）和占空比（duty cycle）都影响 recovery 量

### Delay (τp) Degradation
- NBTI → ΔVth ↑ → circuit delay ↑
- Propagation delay τp 增加与 NBTI 退化量成正比
- **Delay degradation 也表现出频率依赖性**：高频 → 延迟退化小

### Measurement Setup
- Pulse measurement: Vgs 脉冲宽度 100 ns – 1 μs
- Frequency range: DC – 10 MHz
- 测量参数：ΔVth, ΔIdsat, Δgm, Δτp

### AC vs DC NBTI
- **DC (static stress)**: 持续负偏置，worst case degradation
- **AC (pulsed stress)**:
  - 高电平 phase：施加 NBTI stress
  - 低电平 phase：stress-free → recovery 发生
  - 50% duty cycle：stress 和 recovery 各占一半
  - 实际电路通常工作在 AC 模式

## Implications

- **高频数字电路**受 NBTI 影响较小（recovery 充分）
- **静态偏置**（如 analog 电路 reference、DC 偏置）需要更保守的 NBTI 估计
- **加速测试**：DC stress 可用于快速评估 NBTI 敏感性
- **电路设计**：考虑工作频率对 NBTI 寿命的影响

## Related
- [[concepts/nbti]] — NBTI 基础机制
- [[concepts/nbti-frequency-effect]] — NBTI 频率效应

## Source
[Delay Effects and Frequency Dependence of NBTI with Sub-microsecond Measurements](raw/sources/Delay_effects_and_frequency_dependence_of_NBTI_with_sub-microsecond_measurements.pdf)
