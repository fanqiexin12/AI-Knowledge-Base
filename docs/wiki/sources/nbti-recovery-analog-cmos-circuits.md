---
title: "Modeling of NBTI-Recovery Effects in Analog CMOS Circuits"
type: source
tags: [nbti, recovery, analog-cmos, modeling, circuit-simulation, transconductance, mismatch]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Modeling_of_NBTI-recovery_effects_in_analog_CMOS_circuits.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/analog-circuit-nbti", "Analog Circuit NBTI"]]
---

# Modeling of NBTI-Recovery Effects in Analog CMOS Circuits

## Summary
本文建立 **NBTI 恢复效应在模拟 CMOS 电路中的模型**。模拟电路（如 **operational amplifier、ADC、DAC**）对 NBTI 退化更敏感——电路性能依赖精确的晶体管匹配，而 NBTI 恢复使 **transconductance (gm) 和阈值电压 (Vth)** 呈现复杂的时间依赖行为。

## Key Findings

### Analog vs Digital NBTI
| Aspect | Digital | Analog |
|--------|---------|--------|
| **Critical parameter** | Vth, timing | gm, Vth, gain, bandwidth |
| **Matching requirement** | Low | High (差分对匹配) |
| **Recovery effect** | 可忽略 | 显著 |
| **Stress pattern** | AC/pulsed | DC or quasi-DC |

### NBTI Recovery in Analog Context
- **Analog 电路常 DC bias**（静态工作点）
- **Recovery during signal swing**：信号负半周期 → 部分恢复
- **Net effect**：取决于 stress/recovery duty cycle
- **Transconductance gm recovery**：gm 是模拟电路核心参数

### Modeling Approaches
1. **Time-dependent Vth model**：
   - ΔVth(t) = ΔVth_max × (1 - exp(-t/τ_r)^β)
   - Recovery time constant τ_r ~ 10-1000 s

2. **Power-law recovery**：
   - ΔVth_recovery ~ t^α (α ≈ 0.1-0.3)
   - 适合描述长期恢复

3. **Compact model integration**：
   - BSIM6 / PSP 模型加入 NBTI recovery
   - 可在 SPICE 中直接仿真

### Impact on Analog Circuits

#### Operational Amplifier
- **Offset voltage V_os**：NBTI 导致 V_os 增加 → 失调
- **Open-loop gain Av**：gm 退化 → Av 下降
- **GBW (Gain-Bandwidth)**：退化

#### Comparator
- **Input offset**：不匹配增加
- **Resolution degradation**：最小可分辨信号增大

#### Data Converter (ADC/DAC)
- **INL/DNL**：积分非线性/差分非线性退化
- **SNDR**：信噪失真比下降

### Recovery Modeling Challenges
- **Multiple time constants**：快/慢恢复叠加
- **Signal dependence**：输入信号 pattern 影响 recovery
- **Mismatch effect**：相邻晶体管的 recovery 不一致 → 失配加剧

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/analog-circuit-nbti]] — 模拟电路 NBTI

## Source
[Modeling of NBTI-Recovery Effects in Analog CMOS Circuits](raw/sources/Modeling_of_NBTI-recovery_effects_in_analog_CMOS_circuits.pdf)
