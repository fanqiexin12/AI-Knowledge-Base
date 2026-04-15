---
title: "A NBTI Tolerant Technique for FinFET Based Wide Fan-in Dynamic Logic"
type: source
tags: [finfet, nbti, dynamic-logic, nbti-mitigation, wide-fan-in, circuit-reliability]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/A_NBTI_tolerant_technique_for_FinFET_based_wide_fan-in_dynamic_logic.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/finfet", "FinFET"], ["concepts/nbti-mitigation", "NBTI Mitigation"]]
---

# A NBTI Tolerant Technique for FinFET Based Wide Fan-in Dynamic Logic

## Summary
本文针对 **FinFET 宽扇入动态逻辑（wide fan-in domino logic）** 提出一种 **NBTI tolerant 技术**。核心思路：识别动态逻辑中的 **critical internal node（关键内部节点）**，通过信号编码技术（data encoding）减少这些节点上的 NBTI stress 时间，从而延长电路寿命。

## Key Findings

### Wide Fan-in Dynamic Logic Vulnerability
- Domino logic (动态逻辑) 有 precharge 和 evaluate 阶段
- **Precharge phase**：PMOS pull-up 导通（Vgs < 0）→ NBTI stress on PMOS
- Evaluate phase：无 stress，但 domino 逻辑的 evaluation 直接受 PMOS strength 影响
- **Wide fan-in**：输入越多，评估时间越长，PMOS 承受 stress 时间比例越高

### Critical Internal Nodes
- 动态逻辑中某些内部节点的状态决定了电路的最差情况延迟
- 这些节点在长时间内保持特定状态 → 更严重的 NBTI 累积
- **Gate Merging** 技术将这些关键节点的负载分散，减少单个节点的应力集中

### NBTI Tolerant Encoding
- **Data encoding scheme**：对关键节点使用特定的信号编码
- 目标：平衡节点的正负 state 时间（balance switching activity）
- 减少 PMOS 处于负偏置（stress）状态的时间比例

### FinFET Advantages for NBTI Tolerance
- **更好的静电控制**：3D 栅极环绕 → 更好的亚阈值斜率
- **更低泄漏电流**：关断时泄漏更小
- **更少氧化层电场**：相同 Vcc 下 Tox 更厚（等效）

## FinFET vs Bulk

| 特性 | FinFET | Bulk |
|------|--------|------|
| **NBTI 敏感性** | 较低 | 较高 |
| **栅极控制** | 3 面环绕 | 1 面 |
| **短沟道效应** | 更好抑制 | 较差 |

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/finfet]] — FinFET 架构
- [[concepts/nbti-mitigation]] — NBTI 缓解技术

## Source
[A NBTI Tolerant Technique for FinFET Based Wide Fan-in Dynamic Logic](raw/sources/A_NBTI_tolerant_technique_for_FinIFET_based_wide_fan-in_dynamic_logic.pdf)
