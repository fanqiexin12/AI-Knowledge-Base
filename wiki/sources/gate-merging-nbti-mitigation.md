---
title: "Gate Merging: An NBTI Mitigation Method to Eliminate Critical Internal Nodes in Digital Circuits"
type: source
tags: [nbti, nbti-mitigation, gate-merging, critical-internal-node, circuit-aging, reliability]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Gate_Merging_An_NBTI_Mitigation_Method_to_Eliminate_Critical_Internal_Nodes_in_Digital_Circuits.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nbti-mitigation", "NBTI Mitigation"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# Gate Merging: An NBTI Mitigation Method to Eliminate Critical Internal Nodes in Digital Circuits

## Summary
**Gate Merging** 是一种 NBTI 缓解技术，核心思路：**合并功能相关但原来分离的门电路**，消除 critical internal node（关键内部节点），使内部节点受 NBTI 影响的延迟退化转移到对性能影响更小的路径上。

## Key Findings

### Critical Internal Nodes Problem
- 电路中某些内部节点（internal node）的状态决定最差路径延迟
- 这些节点可能被长期偏置在 stress 状态（PMOS 负偏置）
- 随着 NBTI 退化，这些节点的 Vth 增加 → circuit delay 增加
- **关键节点一旦退化，影响整条路径的 timing**

### Gate Merging Strategy
- **合并功能相近的门**：将原来分离的两个逻辑门合并为一个更大、更简单的门
- **消除中间节点**：原本需要通过中间节点连接的信号，现在可以在单个门内完成
- **内部节点变为内部网络**：不再直接暴露在 NBTI stress 下，或 stress 时间大幅减少

### Quantitative Benefits
- **Timing degradation reduction**: 可减少 30-50% 的 NBTI 导致的时序退化
- **Area overhead**: 适度增加（10-20%），但换来可靠性提升
- **Power impact**: 取决于合并后门的开关 activity

### Gate Level Considerations
- **Which gates to merge?**: 分析 timing critical paths，识别高频 stress 节点
- **Logic simplification**: 合并后逻辑可简化（如去除冗余反相器）
- **Physical layout**: 合并门共享一些晶体管，减少整体面积

## Comparison with Other NBTI Mitigation Techniques

| Technique | 方法 | Pros | Cons |
|-----------|------|------|------|
| **Gate Merging** | 消除关键内部节点 | 减少 critical path 退化 | 增加面积 |
| **Input Vector Control** | 选择低应力输入 | 低开销 | 有限效果 |
| **Body Biasing** | 调节 Vth | 动态可调 | 需要 triple-well |
| **Voltage Guardband** | 预留余量 | 简单 | 性能损失 |

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/nbti-mitigation]] — NBTI 缓解技术总结
- [[concepts/circuit-aging]] — 电路级老化

## Source
[Gate Merging: An NBTI Mitigation Method to Eliminate Critical Internal Nodes in Digital Circuits](raw/sources/Gate_Merging_An_NBTI_Mitigation_Method_to_Eliminate_Critical_Internal_Nodes_in_Digital_Circuits.pdf)
