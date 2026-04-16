---
title: "SOI MOSFET"
type: concept
tags: [soi, mosfet, floating-body, pd-soi, fd-soi, semiconductor, reliability]
created: 2026-04-14
updated: 2026-04-16
sources: ["raw/sources/Effect_of_Floating-Body_and_Stress_Bias_on_NBTI_and_HCI_on_65-nm_SOI_pMOSFETs.pdf", "raw/sources/Assessment_of_NBTI_in_Presence_of_Self-Heating_in_High-_k_SOI_FinFETs.pdf"]
related: [["concepts/hci", "HCI"], ["concepts/nbti", "NBTI"], ["concepts/nanosheet-fet", "Nanosheet FET"]]
---

# SOI MOSFET

## Summary
**SOI（Silicon-on-Insulator）MOSFET** 是一种在绝缘衬底（如 SiO₂）上形成 Si 薄膜沟道的器件架构。相比传统 Bulk MOSFET，SOI 通过 **BOX（Buried Oxide）** 实现沟道与衬底的介质隔离，消除闩锁效应、降低泄漏电流，但引入 **floating-body（体区悬空）** 效应。

## Types of SOI

### PD-SOI (Partially Depleted SOI)
- Si 膜厚度较厚（50-90nm）→ 耗尽层未充满整个 Si 膜
- **Body 区悬空（floating body）** → 电压随偏置变化
- **优点**：工艺与 bulk 兼容性好
- **缺点**：floating-body 效应（kink effect, history effect）

### FD-SOI (Fully Depleted SOI)
- Si 膜极薄（<10-20nm）→ 沟道完全耗尽
- Body 区可通过 **back-gate/bias** 控制（**RBB/RGB**）
- **优点**：更好的静电控制，无 floating-body 问题
- **缺点**：工艺难度高，薄 Si 膜控制困难

## Structure

```
     Gate
       |
   ----|---- ----
  |    |      |
  S    |      D   ← Si 薄膜沟道（thin Si film）
  |    |      |
   ----|---- ----
       | BOX (Buried Oxide)
   ----|---- ----
       |       Si 衬底
```

## Key Features

### Advantages over Bulk
| 特性 | SOI | Bulk |
|------|-----|------|
| **Junction leakage** | 极低（BOX 阻断） | 较高 |
| **Latch-up** | 无（介质隔离） | 可能发生 |
| **Subthreshold slope** | 更陡 | 一般 |
| **Short channel effect** | 更好抑制 | 较差 |
| **寄生电容** | 更低 | 较高 |

### Floating-Body Effects (PD-SOI)
1. **Kink effect**：浮体充电导致沟道电流异常突增
2. **History effect**：之前应力状态影响当前 I-V 特性
3. **Self-heating**：BOX 热阻高，散热差

## Reliability: NBTI & HCI in SOI

### NBTI in SOI
- **History effect**：stress-bias 历史影响退化量
  - 负偏置存储（Vgs < 0）→ NBTI 加重
  - 零偏置存储 → NBTI 部分恢复
- **与 Bulk 不同**：Bulk 的 NBTI 测量结果更稳定，不依赖历史

### Self-Heating in SOI
- **BOX 层热阻高**：热量难以散去
- **温度升高 20-40°C** at high power states
- 温度升高加速 NBTI 动力学（Arrhenius 关系）
- High-k 介质 + SOI 结构使 NBTI 更敏感
- Self-heating 同时影响 recovery 动力学

### HCI in SOI (PD-SOI)
- **比 Bulk 更严重**：
  - Body 区充电（正向 Vbody）使源端注入更多载流子
  - 体-p-n结反偏 → 碰撞电离率提高
  - 碰撞电离产生的电子-空穴对中，电子进入 body → 正向充电 → 进一步增强碰撞电离（正反馈）

## Technology Node Relevance

- **65nm-45nm**：PD-SOI 被广泛使用（IBM, AMD 等）
- **28nm 及以下**：FD-SOI 兴起（STMicroelectronics 等）
- **先进节点**：FD-SOI + 后端偏置（back-bias）用于功耗/性能调节
- **最新**：GAA Nanosheet 继承了 SOI 的思路（环绕栅极全介质隔离）

## Related
- [[concepts/hci]] — HCI 在 PD-SOI 中更严重
- [[concepts/nbti]] — NBTI 的 history effect
- [[concepts/nanosheet-fet]] — GAA 架构与 SOI 的思想传承
