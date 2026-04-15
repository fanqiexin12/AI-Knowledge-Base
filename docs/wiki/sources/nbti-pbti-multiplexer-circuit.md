---
title: "Investigation of The NBTI and PBTI Effects on Multiplexer Circuit Performances"
type: source
tags: [nbti, pbti, multiplexer, circuit-aging, timing-degradation, reliability, circuit-reliability]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Investigation_of_The_NBTI_and_PBTI_Effects_on_Multiplexer_Circuit_Performances.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/pbti", "PBTI"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# Investigation of The NBTI and PBTI Effects on Multiplexer Circuit Performances

## Summary
本文实验研究 **NBTI 和 PBTI 对 multiplexer（多路复用器）电路性能的影响**。关键发现：NBTI 主要导致 **上升时间（rise time）退化**，PBTI 主要导致 **下降时间（fall time）退化**；传输延迟（propagation delay）退化随时间累积，严重时导致 timing failure。

## Key Findings

### MUX Circuit Structure
- **2:1 MUX**：基本单元，由传输门（TG）或 CMOS 逻辑实现
- **关键路径**：sel → out 路径决定 MUX 的切换速度
- **PMOS** 控制 pull-up（上升边），**NMOS** 控制 pull-down（下降边）

### NBTI vs PBTI Impact on MUX

| BTI Type | 主要影响器件 | 退化参数 |
|----------|------------|---------|
| **NBTI** | PMOS pull-up | Rise time ↑（上升变慢），τpLH ↑ |
| **PBTI** | NMOS pull-down | Fall time ↓（下降变慢），τpHL ↑ |

### Propagation Delay Degradation
- **τpLH**（低→高）：PMOS 主导 → NBTI 使其 ↑
- **τpHL**（高→低）：NMOS 主导 → PBTI 使其 ↑
- **总传输延迟** τp = max(τpLH, τpHL) → 随着 aging 增加

### Input Pattern Dependence
- MUX 输入信号 pattern 影响 PMOS/NMOS 的 stress 时间
- **Sel 信号频率**也影响 stress duty cycle
- 高频切换 → NBTI/PBTI 效应降低（recovery 机制）

### Lifetime Prediction
- **10 年运行**：在 DC stress 下，MUX 的 τp 退化可达 15-25%
- **实际 AC 使用**：退化约 10-15%（recovery 效果）
- **Design margin** 需要预留 20-30% 以保证 10 年寿命

### MUX in Larger Systems
- MUX 常用于 **data routing、address selection、clock multiplexing**
- 在 **SoC** 中，MUX 的 timing degradation 影响系统性能
- **Critical path** 中的 MUX 需要特别关注 aging

## Comparison with Inverter
- MUX 比 inverter 更复杂：两种 transition (τpLH, τpHL)
- Inverter 的 NBTI/PBTI 效应相对对称
- MUX 的退化分布依赖于 sel 信号 duty cycle

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/pbti]] — PBTI 机制
- [[concepts/circuit-aging]] — 电路老化

## Source
[Investigation of The NBTI and PBTI Effects on Multiplexer Circuit Performances](raw/sources/Investigation_of_The_NBTI_and_PBTI_Effects_on_Multiplexer_Circuit_Performances.pdf)
