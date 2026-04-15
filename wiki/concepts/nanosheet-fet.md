---
title: "Nanosheet FET"
type: concept
tags: [semiconductor, gaa, finfet-successor, advanced-nodes, fet-architecture]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Impact_of_Material_Variability_on_the_Reliability_of_Nanosheet_FETs.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/pbti", "PBTI"], ["concepts/variability-sources", "Variability Sources"]]
---

# Nanosheet FET

## Summary
Nanosheet FET（全栅极环绕 FET，Gate-All-Around）是 3nm/2nm 及以下节点取代 FinFET 的主流架构，以**水平堆叠的多层纳米片**环绕沟道四周提供栅极静电控制。

## Overview

### Architecture
- **结构**：水平堆叠 3-5 层纳米带（nanosheet），每层厚度 ~5nm，宽度 ~45nm
- **栅极**：环绕纳米片四周（4 面栅极控制），优于 FinFET 的 3 面控制
- **优势**：
  - 更好的短沟道效应抑制
  - 更高的单位面积驱动电流（通过堆叠多层）
  - 更好的静电控制 → 更低的漏电流

### Node Roadmap
| Node | Architecture |
|------|-------------|
| 7nm | FinFET |
| 5nm | FinFET (optimized) |
| 3nm | **Nanosheet/GAA** |
| 2nm | **Nanosheet/GAA** (堆叠层数更多) |

### vs. FinFET
- FinFET：沟道突出成鳍状，栅极包覆 3 面
- Nanosheet：沟道是水平薄片，栅极包覆 4 面
- Nanosheet 可通过调节**纳米片宽度和堆叠层数**来调整驱动电流，比 FinFET 的鳍数量调节更灵活

## Related
- [[concepts/nbti]] — NBTI degradation mechanism
- [[concepts/pbti]] — PBTI degradation mechanism
- [[concepts/variability-sources]] — Main variability sources affecting nanosheet reliability
