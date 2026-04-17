---
title: "Circuit Aging"
type: concept
tags: [circuit-aging, nbti, pbti, hci, reliability, timing-degradation, bti, lifetime]
created: 2026-04-14
updated: 2026-04-16
sources: ["raw/sources/Gate_Merging_An_NBTI_Mitigation_Method_to_Eliminate_Critical_Internal_Nodes_in_Digital_Circuits.pdf", "raw/sources/Investigation_of_The_NBTI_and_PBTI_Effects_on_Multiplexer_Circuit_Performances.pdf", "raw/sources/BTI_impact_on_SRAM_sense_amplifier.pdf", "raw/sources/Deep_experimental_investigation_of_NBTI_impact_on_CMOS_inverter_reliability.pdf", "raw/sources/Degradation_and_Self-Recovery_of_Polycrystalline_Silicon_TFT_CMOS_Inverters_Under_NBTI_Stress.pdf", "raw/sources/papers-onedrive/Impact_of_NBTI_on_the_performance_of_35nm_CMOS_digital_circuits.pdf", "raw/sources/papers-onedrive/Impact_of_NBTI_on_the_temporal_performance_degradation_of_digital_circuits.pdf", "raw/sources/papers-onedrive/Modeling_and_minimization_of_PMOS_NBTI_effect_for_robust_nanometer_design.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/pbti", "PBTI"], ["concepts/hci", "HCI"]]
---

# Circuit Aging

## Summary
电路老化（Circuit aging）是指集成电路在长时间工作后，由于 **NBTI、PBTI、HCI、EM** 等可靠性机制导致的性能退化。随着摩尔定律推进，先进节点的电路老化问题日益严峻——10 年运行后 timing degradation 可达 10-20%。

## Aging Mechanisms

| Mechanism | Primary Driver | Dominant Effect |
|-----------|---------------|----------------|
| **NBTI** | Vgs < 0, High T | PMOS Vth ↑ |
| **PBTI** | Vgs > 0, High T | NMOS Vth ↑ |
| **HCI** | High Vds | Id, gm 退化 |
| **EM** | High current density | 互连电阻 ↑ |

## Circuit-Level Aging Impact

### Timing Degradation
- **Path delay** 随 Vth 漂移增加
- Critical path 是 aging limit 的瓶颈
- τpLH (rise) 主要受 NBTI，τpHL (fall) 主要受 PBTI

### SRAM Aging
- **Read margin (SNM)** 退化
- **Sense amplifier offset** 增加
- **Write margin** 退化

### Analog Circuit Aging
- **Offset voltage** 增加
- **Transconductance (gm)** 退化
- **Gain-Bandwidth Product (GBW)** 下降

### CMOS Inverter Aging
- **Vth shift**：PMOS NBTI 导致 Vth 正漂移 ~50mV @ 10yr
- **Switching threshold (V_M)** 向 NMOS 侧漂移 ~30mV
- **Noise margin** 退化 10-15%
- **Propagation delay** 增加 5-10%
- **Poly-Si TFT**：自恢复效应使 70-80% 降解可逆

## Aging Projection

### Acceleration Factors
- **Voltage**：V ↑ → aging 加剧（BTI: V^s, HCI: exp(-E_a/kT)）
- **Temperature**：T ↑ → aging 加剧（热激活）
- **Activity factor**： switching frequency 影响 AC aging

### Lifetime Prediction
```
Aging(t) = A × exp(-E_a/kT) × V^n × (1 - exp(-t/τ))
```
- **10 年 extrapolation**：加速测试后外推
- **Worst-case corner**：高 V, 高 T, high switching activity

### 35nm CMOS Data
- **PMOS Vth shift**：~50mV @ 10yr, 125°C
- **Circuit delay increase**：13-17% over 10 years
- **Ring Oscillator freq. degradation**：~8% @ 10yr
- **Recovery fraction**：25-40%（idle期间可恢复部分）

## Mitigation
- [[concepts/nbti-mitigation]] — NBTI 缓解技术
- Design margins, adaptive techniques

## Related
- [[concepts/nbti]] — NBTI
- [[concepts/pbti]] — PBTI
- [[concepts/hci]] — HCI
