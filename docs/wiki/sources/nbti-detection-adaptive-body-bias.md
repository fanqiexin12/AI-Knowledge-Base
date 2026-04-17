---
title: "NBTI Detection Methodology for Building Tolerance with Adaptive Body Bias"
type: source
tags: [nbti, adaptive-body-bias, abb, detection, tolerance, reliability, circuit-aging]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/NBTI_detection_methodology_for_building_tolerance_with_respect_to_NBTI_effects_employing_adaptive_body_bias.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nbti-mitigation", "NBTI Mitigation"]]
---

# NBTI Detection Methodology for Building Tolerance with Adaptive Body Bias

## Summary
本文提出一种 **NBTI 检测方法**，结合 **自适应体偏置 (Adaptive Body Bias, ABB)** 技术来补偿 NBTI 退化。实时监测 + 动态偏置调整可延长芯片寿命 2-3 倍。

## Key Findings

### Adaptive Body Bias (ABB) Concept
- **Forward Body Bias (FBB)**：减少 Vth → 补偿 NBTI 导致的 Vth 增加
- **Reverse Body Bias (RBB)**：增加 Vth → 降低泄漏（用于低功耗模式）
- **Dynamic adjustment**：根据监测结果实时调整

### NBTI Detection Methods
| Method | Principle | Accuracy |
|--------|-----------|----------|
| **Ring oscillator** | Frequency shift | Medium |
| **Vth extraction** | Idlin method | High |
| **On-chip sensors** | Dedicated test structures | High |
| **Self-heating** | Thermal response | Low |

### Control Loop
```
NBTI stress → Vth increase → RO frequency decrease
    ↓
Detection → Comparison with threshold
    ↓
FBB adjustment → Vth compensation
    ↓
Loop continues
```

### Results
- **Lifetime extension**：2-3x improvement
- **Power overhead**：< 5% for ABB circuit
- **Vth compensation range**：up to 50mV

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/nbti-mitigation]] — NBTI mitigation techniques

## Source
- [NBTI_detection_methodology_for_building_tolerance_with_respect_to_NBTI_effects_employing_adaptive_body_bias.pdf](../../raw/sources/papers-onedrive/NBTI_detection_methodology_for_building_tolerance_with_respect_to_NBTI_effects_employing_adaptive_body_bias.pdf)
