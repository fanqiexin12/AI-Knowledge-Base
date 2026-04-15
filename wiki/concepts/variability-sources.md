---
title: "Variability Sources in Advanced FETs"
type: concept
tags: [variability, semiconductor, reliability, manufacturing, advanced-nodes]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Impact_of_Material_Variability_on_the_Reliability_of_Nanosheet_FETs.pdf"]
related: [["concepts/nanosheet-fet", "Nanosheet FET"], ["concepts/nbti", "NBTI"], ["concepts/pbti", "PBTI"]]
---

# Variability Sources in Advanced FETs

## Summary
在先进制程节点（3nm 及以下），**材料变异性（material variability）** 是影响器件可靠性和良率的关键因素。主要来源包括：WFV、LER、MGG、厚度波动等。

## Main Variability Sources

### 1. WFV — Workfunction Variation
- **最显著**的 variability 来源
- HKMG（high-k/metal gate）工艺中，metal gate 的**有效功函数**受 grain 取向影响
- Grain size 越小 → WFV 越大 → σΔVth 越大
- 工艺意义：需要优化 metal gate 退火工艺以增大 grain size

### 2. LER — Line-Edge Roughness
- 栅极边缘的随机粗糙度
- 造成局部栅极长度波动
- 主要影响短沟道效应

### 3. MGG — Metal Grain Granularity
- 栅极金属的晶粒结构不均匀
- 不同 grain 取向有不同的有效功函数
- 与 WFV 紧密相关

### 4. Thickness Variation
- Nanosheet 厚度（~5nm）的随机波动
- 影响栅极氧化层电容和量子限制效应

### 5. Doping Variation
- 源/漏区域掺杂浓度波动
- 影响接触电阻和串联电阻

## Relative Importance

论文发现：**WFV > LER ≈ MGG > 厚度变化**

## Impact on Reliability

- Variability → 器件间 uniformality 差 → 某些器件更快退化
- 在 BTI stress 条件下，variability **加剧** degradation 的分散性
- Multi-sheet Nanosheet 比 single-sheet 对 variability 更 robust

## Related
- [[concepts/nanosheet-fet]] — 变异性对 Nanosheet 架构的影响
- [[concepts/nbti]] / [[concepts/pbti]] — 变异性如何加速 BTI 退化
