---
title: "Separation of NBTI Component from Channel Hot Carrier Degradation in pMOSFETs"
type: source
tags: [nbti, hci, pmosfet, separation, recovery, degradation, reliability]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/papers-onedrive/Separation_of_NBTI_component_from_channel_hot_carrier_degradation_in_pMOSFETs_focusing_on_recovery_phenomenon.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/hci", "HCI"]]
---

# Separation of NBTI Component from Channel Hot Carrier Degradation in pMOSFETs

## Summary
本文提出了从 pMOSFET 的 **HCI 退化中分离 NBTI 贡献** 的方法，并关注 **recovery 现象**。NBTI 和 HCI 机制重叠，但可通过时间域和温度域分离。

## Key Findings

### NBTI vs HCI Separation
- **NBTI**：负栅偏置下的慢速退化，时间常数大
- **HCI**：高 Vds 下的快速退化，时间常数小
- **Recovery 行为不同**：NBTI 可恢复，HCI 基本不可恢复

### Separation Methods
| Method | Principle |
|--------|-----------|
| **Temperature dependence** | NBTI 激活能 ~0.12 eV, HCI ~0.3 eV |
| **Time-resolved measurement** | NBTI 有 long-tail recovery |
| **Vds switching** | HCI 主要在高 Vds 时发生 |
| ** substrate current** | HCI 伴随碰撞电离，NBTI 无 |

### Recovery Phenomenon
- **NBTI recovery**：stress 移除后 25-40% 可恢复
- **HCI recovery**：几乎无 recovery（永久性损伤）
- **Recovery 时间常数**：从 ms 到 ks 不等

### Quantitative Analysis
- **pMOSFET 中 NBTI 贡献** 随工艺节点减小而增加
- **65nm 及以下**：NBTI 成为主要退化机制
- **HCI 相对重要性** 下降

## Related
- [[concepts/nbti]] — NBTI mechanism
- [[concepts/hci]] — HCI mechanism

## Source
- [Separation_of_NBTI_component_from_channel_hot_carrier_degradation_in_pMOSFETs_focusing_on_recovery_phenomenon.pdf](../../raw/sources/papers-onedrive/Separation_of_NBTI_component_from_channel_hot_carrier_degradation_in_pMOSFETs_focusing_on_recovery_phenomenon.pdf)
