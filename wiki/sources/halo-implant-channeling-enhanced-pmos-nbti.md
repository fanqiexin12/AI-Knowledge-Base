---
title: "Enhanced PMOS NBTI Degradation Due to Halo Implant Channeling"
type: source
tags: [nbti, pmos, halo-implant, channeling, strain, reliability]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/Enhanced_PMOS_NBTI_degradation_due_to_halo_implant_channeling.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/strain-engineering", "Strain Engineering"]]
---

# Enhanced PMOS NBTI Degradation Due to Halo Implant Channeling

## Summary
本文揭示了 **Halo Implant Channeling** 导致 **PMOS NBTI 降解加剧** 的机制。晶向沟道效应（Channeling）导致掺杂分布不均匀，形成局部应变场，增强 NBTI 敏感度。

## Key Findings

### Halo Implant Channeling Effect
- **Halo implant**：为了抑制短沟道效应，在沟道两端重度掺杂
- **Channeling**：注入离子沿晶向通道穿透，形成非均匀掺杂分布
- **结果**：沟道内产生局部 **应变场（strain field）**

### Strain-NBTI Coupling
| Strain Type | Effect on NBTI |
|-------------|----------------|
| **Compressive** (on PMOS) | **Worsens** NBTI |
| **Tensile** (on PMOS) | **Alleviates** NBTI |

Halo implant channeling 在 PMOS 沟道中引入 **压应变**，导致：
- Si-H 键能降低
- 界面陷阱更容易生成
- NBTI 降解加速

### Experimental Evidence
- 65nm PMOSFET 测试
- Channeling samples 显示 ΔVth **高出 30-50%**
- TCAD 仿真证实局部应变分布

### Mechanism
```
Halo implant along <110> channel direction
    ↓
Ion channeling through Si lattice
    ↓
Non-uniform doping profile
    ↓
Local compressive strain in channel
    ↓
Si-H bond energy reduction
    ↓
Enhanced interface trap generation under NBTI stress
    ↓
Larger Vth shift
```

## Mitigation Approaches
- **晶向选择**：使用 (100) 晶圆而非 (110)
- **注入角度旋转**：避免沿通道注入
- **Halo 剂量优化**：减少 channeling 效应

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/strain-engineering]] — Strain engineering effects

## Source
- [Enhanced_PMOS_NBTI_degradation_due_to_halo_implant_channeling.pdf](../../raw/sources/Enhanced_PMOS_NBTI_degradation_due_to_halo_implant_channeling.pdf)
