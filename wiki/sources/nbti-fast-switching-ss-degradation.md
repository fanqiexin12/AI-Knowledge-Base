---
title: "A New Fast-Switching NBTI Characterization Method That Determines Subthreshold Slope Degradation"
type: source
tags: [nbti, characterization, subthreshold-slope, ss-degradation, fast-measurement, on-the-fly, reliability]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/A_New_Fast-Switching_NBTI_Characterization_Method_That_Determines_Subthreshold_Slope_Degradation.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nbti-characterization", "NBTI Characterization"]]
---

# A New Fast-Switching NBTI Characterization Method That Determines Subthreshold Slope Degradation

## Summary
本文提出一种**快速开关 NBTI 表征方法**，可在 stress 期间直接测量**亚阈值斜率（SS）退化**。传统 NBTI 表征需要中断 stress 后测量，但**中断本身会触发恢复**导致低估退化。该方法在 stress 脉冲之间插入**超快速亚阈值测量（<1 μs）**，捕捉真实的 SS 退化。

## Key Findings

### Conventional NBTI Measurement Issues
- **Stress-then-measure**：stress → 中断 → 测量
- **Recovery during interrupt**：中断期间 NBTI 部分恢复
- **Underestimation**：恢复导致测量结果偏低
- **SS degradation** 通常被低估 20-30%

### On-the-Fly (OTF) Measurement
- **Vth and Idsat** 可 OTF 测量（stress 期间）
- **SS (Subthreshold Slope)** 更难 OTF 测量：
  - SS 测量需要扫描 Vgs → 需要时间
  - 扫描期间 stress 中断 → 恢复发生

### Novel Fast SS Measurement
- **脉冲式 SS 测量**：stress 脉冲之间插入短测量窗口（<1 μs）
- **测量窗口足够短**：恢复来不及发生
- **捕捉真实 SS 退化**：无恢复假象

### Measurement Setup
```
Stress: Vgs_stress = -1.4V (for NBTI)
        ┌──────────────────────────────────────┐
        │    ┌─────┐    ┌─────┐    ┌─────┐    │
        │    │ SS  │    │ SS  │    │ SS  │    │  ...
        │    │measure│   │measure│   │measure│   │
        │    └──┬──┘    └──┬──┘    └──┬──┘    │
        └───────┼──────────┼──────────┼─────────┘
        |<-- T_stress -->|<-- T_stress -->|
              |<-- Δt_meas -->|  (<1 μs)
```

### Key Results
- **SS degradation 比传统方法高 20-40%**
- **Interface trap creation rate** 更准确测量
- **与 DC stress 结果一致**（无 recovery 干扰）

## Method Comparison

| 方法 | SS 测量 | Recovery 误差 | 速度 |
|------|---------|-------------|------|
| **Conventional** | Post-stress | 高（20-40%）| 慢 |
| **OTF Vth/Idsat** | N/A | 极低 | 快 |
| **Fast SS OTF** | During stress | 低（<5%）| 中 |

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/nbti-characterization]] — NBTI 表征技术

## Source
[A New Fast-Switching NBTI Characterization Method That Determines Subthreshold Slope Degradation](raw/sources/A_New_Fast-Switching_NBTI_Characterization_Method_That_Determines_Subthreshold_Slope_Degradation.pdf)
