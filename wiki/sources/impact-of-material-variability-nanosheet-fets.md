---
title: "Impact of Material Variability on the Reliability of Nanosheet FETs"
type: source
tags: [nanosheet-fet, reliability, variability, semiconductor, advanced-nodes]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Impact_of_Material_Variability_on_the_Reliability_of_Nanosheet_FETs.pdf"]
related: [["concepts/nanosheet-fet", "Nanosheet FET"], ["concepts/nbti", "NBTI"], ["concepts/pbti", "PBTI"], ["concepts/variability-sources", "Variability Sources"]]
---

# Impact of Material Variability on the Reliability of Nanosheet FETs

## Summary
这是一篇关于 **Nanosheet FET**（GAA 架构的 successor to FinFET）可靠性的仿真研究。研究聚焦于材料变异性（variability）对器件时变 degradation（BTI 效应）的影响，发现：**Nanosheet 堆叠架构在可靠性方面比单 nanosheet 器件表现更优**，但变异性会显著影响器件间的 uniformality，且 WFV（workfunction variation）是最主要的 variability 源。

## Key Findings

- Nanosheet FET 是 3nm/2nm 节点的主流 GAA 架构，以堆叠水平纳米片的形式围绕沟道四周提供栅极控制
- 可靠性两大杀手：**NBTI**（p-FET 的负偏置温度不稳定性）和 **PBTI**（n-FET 的正偏置温度不稳定性）
- 随时间导致 Vth（阈值电压）漂移、亚阈值斜率退化、ring oscillator 频率下降
- 仿真表明：**variability 主要来源是 WFV**（workfunction variation），其次是 LER（line-edge roughness）和 MGG（metal grain granularity）
- **HKMG**（high-k/metal gate）工艺中，metal gate grain size 越小 → WFV 越大 → 器件uniformality 越差
- Nanosheet 堆叠（multi-sheet）比单纳米片表现更好：相同占位面积下提供更多驱动电流，且对 variability 的敏感度更低

## Technical Details

- **器件架构**：Gate-all-around (GAA) Nanosheet FET，水平堆叠 3-5 层纳米带，sheet thickness ~5nm，sheet width ~45nm
- **仿真方法**：TCAD 仿真 + Compact model；测试了 multi-sheet（3-5 层）和 single-sheet 结构
- **关键参数**：Vth variation (σΔVth)、subthreshold slope (SS)、DIBL、Ion/Ioff
- **BTI 建模**：standard R-D model（reaction-diffusion），stress 条件：Vgs = -1.4V (NBTI), +1.2V (PBTI)，T = 300K 和 400K

## Implications

- 在 3nm 及以下节点，**variability management** 是可靠性和良率的关键
- GAA Nanosheet 架构在性能和可靠性之间提供了更好的平衡
- Metal gate 工艺控制（减少 workfunction variability）对 advanced nodes 至关重要

## Source
[Impact of Material Variability on the Reliability of Nanosheet FETs](raw/sources/Impact_of_Material_Variability_on_the_Reliability_of_Nanosheet_FETs.pdf)
