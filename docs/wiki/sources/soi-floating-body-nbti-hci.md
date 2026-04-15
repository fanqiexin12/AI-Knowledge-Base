---
title: "Effect of Floating-Body and Stress Bias on NBTI and HCI on 65-nm SOI pMOSFETs"
type: source
tags: [soi, floating-body, nbti, hci, pmosfet, reliability, stress-bias, pd-soi]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Effect_of_Floating-Body_and_Stress_Bias_on_NBTI_and_HCI_on_65-nm_SOI_pMOSFETs.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/hci", "HCI (Hot Carrier Injection)"], ["concepts/soi-mosfet", "SOI MOSFET"]]
---

# Effect of Floating-Body and Stress Bias on NBTI and HCI on 65-nm SOI pMOSFETs

## Summary
本文研究 **65nm PD-SOI (Partially Depleted Silicon-on-Insulator) pMOSFET** 中 **floating-body 效应** 和 **stress bias 条件** 对 **NBTI** 和 **HCI (Hot Carrier Injection)** 退化的影响。关键发现：SOI 的 floating body（体区悬空）导致 NBTI 退化表现出**历史记忆效应**，且 HCI 退化比 bulk MOSFET 更严重。

## Key Findings

### 1. PD-SOI Floating-Body Effect
- PD-SOI 中 body 区（Si薄膜）被 **BOX (Buried Oxide)** 与衬底隔离 → **floating body**（体区悬空）
- Body 电压 Vbody 受源/漏/栅偏置调制，不固定为地电位
- **影响**：
  - History effect：之前应力状态影响当前器件特性
  - Kink effect：浮体导致 kink 效应（沟道电流突变）
  - 更低的泄漏电流（junction leakage 路径被 BOX 阻断）

### 2. Stress Bias 对 NBTI 的影响
- **stress-measure-stress 序列**很重要：测量间隔期间施加的偏置状态影响退化量
- **Negative Vgs during interval**（负栅偏置存储）→ 加速 NBTI 退化 → 更大 ΔVth
- **Zero Vgs during interval**（零偏置存储）→ NBTI 部分恢复 → 更小 ΔVth
- **原因**：负偏置维持 Si-H 键断裂的界面态；零偏置允许 H 回迁

### 3. Stress Bias 对 HCI 的影响
- HCI 发生在高电场区域（漏端附近）
- **Stress 时 Vds 越大** → 退化越严重（沟道热载流子能量更高）
- **Stress 时 Vgs 位置影响退化分布**：Vgs = Vds/2 时 HCI 最严重（此时碰撞电离率最高）

### 4. HCI vs. NBTI in PD-SOI
| 特性 | NBTI | HCI |
|------|------|-----|
| **退化位置** | 整个沟道区域 | 漏端附近（高电场区） |
| **失效机制** | Si-H 键断裂，H 扩散 | 热载流子注入氧化层 |
| **应力依赖** | Vgs 主导 | Vds + Vgs 共同决定 |
| **SOI 特殊性** | 历史记忆效应 | 比 bulk 更严重（body 充电效应） |

### 5. PD-SOI 对 HCI 更敏感的原因
- Body 区充电（正向 body 电压）→ body-p-n结反偏 → **碰撞电离率提高** → 产生更多热载流子
- 体区充电使源端注入更多空穴到沟道 → HCI 退化加剧

## Comparison: Bulk vs. SOI

| 特性 | Bulk MOSFET | PD-SOI MOSFET |
|------|-------------|---------------|
| **Body** | 接地 | Floating（悬空） |
| **Junction leakage** | 较高 | 低（BOX 阻断） |
| **NBTI 历史效应** | 无 | 有（stress bias 依赖） |
| **HCI 敏感性** | 较低 | 较高（body 充电） |
| **闩锁效应** | 可能 | 无（完全介质隔离） |

## Implications

- **SOI 可靠性测试**必须考虑 stress-bias 历史和 floating-body 效应
- **HCI 在 SOI 中比 bulk 更严重**，设计时需要特别关注
- NBTI 测试协议必须标准化（stress/measurement 序列），否则结果不可比

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/hci]] — HCI 机制
- [[concepts/soi-mosfet]] — SOI MOSFET 架构

## Source
[Effect of Floating-Body and Stress Bias on NBTI and HCI on 65-nm SOI pMOSFETs](raw/sources/Effect_of_Floating-Body_and_Stress_Bias_on_NBTI_and_HCI_on_65-nm_SOI_pMOSFETs.pdf)
