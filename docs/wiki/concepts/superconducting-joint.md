---
title: "Superconducting Joint"
type: concept
tags: [superconductor, joint-connection, mri-magnets, persistent-mode, reliability]
created: 2026-04-14
updated: 2026-04-16
sources: ["raw/sources/Superconducting_Connections_Between_NbTi_Thin_Films_With_NbN_Paste.pdf", "raw/sources/papers-onedrive/Novel_Pb-Free_Superconducting_Joint_Between_NbTi_and_Nb3Sn_Wires_Using_High-Temperature-Tolerable_Superconducting_Nb3Hf_Intermedia.pdf"]
related: [["entities/nbti", "NbTi"], ["entities/nbn", "NbN"], ["concepts/hta-hts", "HTS Materials"]]
---

# Superconducting Joint

## Summary
超导接头（Superconducting Joint）是指两块超导体之间实现**零电阻**连接的技术，是 MRI/NMR 磁体持久模式运行的关键。传统 solder joint 有接触电阻，而真超导接头（SC joint）通过超导材料直接连接，实现无电阻闭合回路。

## Types of Joints

### 1. Solder Joint (Conventional)
- **材料**：InSnPb 或类似软钎料
- **问题**：
  - 接触电阻 R_cont = 0.15–0.35 nΩ·cm²（对 10kA 级导体不理想）
  - 热循环后性能退化
  - 机械强度低，无法承受高场磁体的 Lorentz 力
- **应用**：目前工业主流，用于 10kA 以下导体

### 2. Superconducting Joint (本文研究)
- **目标**：零电阻连接（真超导）
- **方法**：NbN paste 烧结连接 NbTi
- **挑战**：Ti 表面氧化层阻碍电接触，需要表面处理（HNA 刻蚀）
- **优势**：无接触电阻，可持久模式运行

### 3. Diffusion Bonding
- 高温高压下原子扩散形成连接
- 用于 Nb₃Sn 线材连接（需在 600–700°C 烧结）

## Applications

| 应用 | 需求 |
|------|------|
| MRI 磁体 | 持久模式运行，低年衰减率 (<0.1%/年) |
| NMR 磁体 | 高场稳定性 (>23T) |
| 高能物理 | 大型磁体，低交流损耗 |

## Key Challenges

1. **表面氧化**：TiOx 层阻断电接触
2. **热膨胀系数 (CTE) 不匹配**：NbTi / solder / NbN 三者 CTE 不同 → 界面应力
3. **机械稳定性**：高场 Lorentz 力可破坏接头
4. **长期稳定性**：热循环、机械振动

## Nb₃Hf Joint Technology

- **Nb₃Hf 中间层**：高 Hc2 (~20-25T)，优于 NbTi
- **无铅设计**：环境友好，避免 Sn-Pb 焊料
- **工艺**：热等静压 (HIP) + 扩散退火
- **性能**：接头电阻 < 0.5 nΩ，可工作于 >12T 磁场

## Related
- [[entities/nbti]] — 最重要的 LTS 材料
- [[entities/nbn]] — 高 Tc 超导材料，用于接头膏体
- [[concepts/hta-hts]] — 高温超导材料
