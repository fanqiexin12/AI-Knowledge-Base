---
title: "Degradation and Self-Recovery of Polycrystalline Silicon TFT CMOS Inverters Under NBTI Stress"
type: source
tags: [nbti, polysilicon, tft, cmos, inverter, self-recovery, reliability]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/Degradation_and_Self-Recovery_of_Polycrystalline_Silicon_TFT_CMOS_Inverters_Under_NBTI_Stress.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# Degradation and Self-Recovery of Polycrystalline Silicon TFT CMOS Inverters Under NBTI Stress

## Summary
本文研究了 **Polycrystalline Silicon (Poly-Si) TFT** CMOS Inverter 在 **NBTI 应力** 下的降解和 **自恢复（Self-Recovery）** 行为。Poly-Si TFT 与体硅 MOSFET 相比，有独特的晶界效应和 NBTI 机制。

## Key Findings

### Poly-Si TFT vs Crystalline MOSFET
| Feature | Poly-Si TFT | Crystalline MOSFET |
|---------|-------------|-------------------|
| **Channel** | Polycrystalline Si | Single crystal Si |
| **Grain boundaries** | Present,影响 Vth 分布 | None |
| **Interface traps** | More, due to poly structure | Less |
| **NBTI mechanism** | Grain boundary assisted | Interface trap dominant |
| **Self-recovery** | More pronounced | Less pronounced |

### NBTI Degradation in Poly-Si TFT
- **Grain boundary trapping**：晶界作为陷阱中心，捕获空穴
- **Interface trap generation**：Si-H 键断裂发生在晶界附近更剧烈
- **Vth shift**：正漂移，与体硅 PMOS 类似

### Self-Recovery Phenomenon
- 应力移除后，**部分降解可逆**
- Recovery 机制：
  - **热激活**：温度升高加速缺陷恢复
  - **空穴去捕获**：陷阱中的空穴释放
  - **Si-H 重组**：部分断裂的键重新形成
- Recovery 量级与 stress 强度、时间相关

### Inverter Circuit Impact
| Parameter | Degradation | Recovery |
|-----------|-------------|----------|
| **V_M** | Shift toward NMOS | Partial return |
| **Noise Margin** | Degraded | ~70-80% recovery |
| **Leakage Current** | Increased | Partial recovery |

## Mechanism
```
NBTI Stress (Vgb = -Vdd, T elevated)
    ↓
Hole trapping at grain boundaries + interface
    ↓
Vth positive shift, mobility degradation
    ↓
Stress Removal
    ↓
Thermal annealing + hole de-trapping
    ↓
Partial recovery (70-80%)
```

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/circuit-aging]] — Circuit aging

## Source
- [Degradation_and_Self-Recovery_of_Polycrystalline_Silicon_TFT_CMOS_Inverters_Under_NBTI_Stress.pdf](../../raw/sources/Degradation_and_Self-Recovery_of_Polycrystalline_Silicon_TFT_CMOS_Inverters_Under_NBTI_Stress.pdf)
