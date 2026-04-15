---
title: "Reliability Analysis of CMOS Inverter Subjected to AC and DC NBTI Stresses"
type: source
tags: [nbti, cmos-inverter, ac-nbti, dc-nbti, reliability, aging, vth-shift, trip-point]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Reliability_analysis_of_CMOS_inverter_subjected_to_AC_amp_DC_NBTI_stresses.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/ac-nbti", "AC NBTI"], ["concepts/nbti-frequency-effect", "NBTI Frequency Effect"]]
---

# Reliability Analysis of CMOS Inverter Subjected to AC and DC NBTI Stresses

## Summary
本文研究 **CMOS inverter** 在 **AC 和 DC NBTI stress** 下的可靠性退化。关键发现：**DC stress 下 PMOS NBTI 主导**，**AC stress 下 PMOS 和 NMOS PBTI 均贡献退化**；两种 stress 下 **VM（trip point）均向 NMOS 方向漂移**，导致传播延迟 τpHL 和 τLH 增加。

## Key Findings

### DC NBTI Stress
- **PMOS NBTI 主导**（PMOS 在 V_in = high 时受负偏置）
- NMOS 基本不受影响（V_in = high 时 Vgs = 0，无 NBTI 应力）
- PMOS Vth 增加（更正值）→ PMOS 驱动能力下降
- **VM 向 NMOS 方向漂移**（因为 PMOS 变弱）

### AC NBTI Stress
- **两种应力 phase**：
  - V_in = high：PMOS NBTI（负偏置），NMOS 无 stress
  - V_in = low：NMOS PBTI（正偏置），PMOS 无 stress
- **PMOS NBTI + NMOS PBTI 共同作用**
- AC 下退化比 DC 下更复杂（两种机制同时影响 circuit）

### VM (Trip Point) Shift
| Stress Type | VM Shift Direction | 原因 |
|-------------|---------------------|------|
| **DC NBTI** | 向 NMOS 侧 | PMOS Vth ↑（变弱）|
| **AC NBTI** | 向 NMOS 侧 | PMOS NBTI + NMOS PBTI 共同作用 |

- VM 漂移影响 **逻辑裕度（noise margin）**
- VM 偏离 VDD/2 导致 **上升/下降时间不对称**

### Propagation Delay Degradation
- τpHL（高→低）：NMOS 为主，NMOS PBTI 使 τpHL ↑
- τpLH（低→高）：PMOS 为主，PMOS NBTI 使 τpLH ↑
- **DC stress**：τpLH 主要退化（PMOS NBTI）
- **AC stress**：τpHL 和 τpLH 都退化（两种机制叠加）

### AC Stress Duty Cycle Effect
| Duty Cycle | Effect |
|------------|--------|
| **50%** | PMOS 和 NMOS 应力时间相等 |
| **> 50%** | PMOS 应力更多 → τpLH 退化更显著 |
| **< 50%** | NMOS 应力更多 → τpHL 退化更显著 |

## Circuit-Level Implications

- ** Aging-induced delay degradation**：NBTI 使 circuit delay 随时间增加
- **Frequency 影响**：低频 AC（接近 DC）→ 更接近 DC stress 退化
- **实测 DC 退化是 AC 退化的上界**（AC 有恢复时间）
- **不对称退化**：上升/下降 transition 表现不同

## Reliability Projection

- **10 年寿命估计**：需要考虑 NBTI 累积效应
- **加速因子**：温度（T）、电压（V）加速 NBTI
- **Design margin**：电路设计需要预留 NBTI 退化余量

## Related
- [[concepts/nbti]] — NBTI 基础机制
- [[concepts/pbti]] — PBTI（AC stress 中 NMOS 承受）
- [[concepts/nbti-frequency-effect]] — 频率效应

## Source
[Reliability Analysis of CMOS Inverter Subjected to AC and DC NBTI Stresses](raw/sources/Reliability_analysis_of_CMOS_inverter_subjected_to_AC_amp_DC_NBTI_stresses.pdf)
