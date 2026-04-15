---
title: "FinFET"
type: concept
tags: [finfet, mosfet, 3d-gate, multi-gate, semiconductor, advanced-nodes, short-channel-effect]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/A_NBTI_tolerant_technique_for_FinFET_based_wide_fan-in_dynamic_logic.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nanosheet-fet", "Nanosheet FET"]]
---

# FinFET

## Summary
**FinFET（鳍式场效应晶体管）** 是一种 **3D 栅极结构** 的 MOSFET，沟道成鳍状突出，栅极从三面包覆沟道。相比 planar MOSFET，FinFET 提供更好的静电控制和更低的泄漏电流，是 **22nm 至 7nm** 节点的主流器件架构。

## Structure

```
        Gate
     =========  ← 栅极（三面包覆）
       ||||
       ||||  ← 鳍（Fin）突出
    ───────────  ← Source/Drain
       ||||
```

- **Fin 宽度**：通常 5-10 nm
- **Fin 高度**：30-60 nm（决定有效沟道宽度）
- **Gate length**：10-20 nm（7nm 节点约 18nm）

## vs Planar MOSFET

| 特性 | Planar | FinFET |
|------|--------|--------|
| **栅极控制** | 1 面 | 3 面 |
| **短沟道效应** | 严重 | 抑制 |
| **亚阈值斜率** | ~60 mV/dec | ~65 mV/dec |
| **泄漏电流** | 较高 | 低 |
| **布局效率** | 高 | 中（fin pitch）|

## Advantages
- **更好的静电控制**：3 面栅极环绕 → 更好的亚阈值斜率
- **更低泄漏**：关断时泄漏电流更低
- **更高驱动电流**：给定占位面积下驱动电流更大

## NBTI in FinFET
- **3D 结构**：fin 侧壁和顶部都受栅极控制
- **NBTI 效应**：fin 侧壁/顶部的 interface quality 可能不同
- **Gate-all-around (GAA)** 是 FinFET 的进化方向 → 4 面栅极控制

## Related
- [[concepts/nbti]] — NBTI
- [[concepts/nanosheet-fet]] — GAA 进化
