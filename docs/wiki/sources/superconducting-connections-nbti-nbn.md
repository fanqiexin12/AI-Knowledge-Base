---
title: "Superconducting Connections Between NbTi Thin Films With NbN Paste"
type: source
tags: [superconductor, nbti, nbn, joint-connection, mri-magnets, hts]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Superconducting_Connections_Between_NbTi_Thin_Films_With_NbN_Paste.pdf"]
related: [["entities/nbn", "NbN"], ["entities/nbti", "NbTi"], ["concepts/superconducting-joint", "Superconducting Joint"]]
---

# Superconducting Connections Between NbTi Thin Films With NbN Paste

## Summary
本文研究使用 **NbN  paste（膏体）** 实现 NbTi 超导线材之间的超导连接。传统钎焊（solder）接头存在接触电阻高、热循环稳定性差、机械粘接薄弱等问题。本文证明：通过 **HNA 酸刻蚀（HF/HNO₃/CH₃COOH）** 去除 Ti 表面氧化层后，NbN paste 可实现低阻超导连接，关键电流（Ic）从 ~10A 大幅提升。

## Key Findings

- **背景**：NbTi 是 MRI/NMR 磁体最广泛使用的超导体（40kA 级导体），但传统 solder lap joint 接触电阻高（R_cont = 0.15–0.35 nΩ·cm²），且热循环和机械应力会导致性能退化
- **核心问题**：Ti 表面氧化层（TiOx）+ 有机污染物阻碍电接触；钎焊接头的机械变形来自材料间热膨胀系数差异
- **NbN paste 方案**：
  - NbN 超导涂层 Tc ≈ 17K，Hc2 ≈ 500 kG（@4.2K）
  - 制备：Nd:YAG 激光沉积 NbN 薄膜 → 涂覆 NbN paste → 400°C 氮气氛围烧结
- **HNA 处理是关键**：
  - 未处理：Ic ≈ 10A（几乎不导通）
  - HNA 处理后：超导接头性能显著改善
- **工艺流程**：
  1. Arc-machined NbTi 薄带
  2. HNA 刻蚀（去除 TiOx，暴露新鲜 Ti 表面）
  3. 涂覆 NbN paste
  4. 热压烧结（400°C，15 MPa，10 min，N₂ 氛围）

## Technical Details

- **NbN 薄膜**：厚 2–3 μm，激光烧蚀沉积于 Si 衬底
- **烧结条件**：400°C，N₂ 氛围，10 分钟
- **HNA 配比**：HF : HNO₃ : CH₃COOH = 1:1:1（体积比）
- **NbN paste 成分**：NbN 粉末 + 有机载体 + 粘结剂
- **热膨胀系数不匹配**：NbTi 和 solder/ NbN CTE 不同 → 界面机械应力

## Implications

- **下一代高场磁体**（>25T，使用 Nb₃Sn 或高温超导 HTS）：传统 solder joint 无法承受应力
- **持久模式运行**（persistent-mode）：超导接头可实现零电阻闭合回路，对 MRI/NMR 长期稳定运行至关重要
- **高温超导 (HTS)**：YBCO, Bi-2212, REBCO 带材的连接问题同样需要类似解决方案

## Related Concepts
- [[concepts/superconducting-joint]] — 超导接头技术
- [[entities/nbti]] / [[entities/nbn]] — 相关超导材料

## Source
[Superconducting Connections Between NbTi Thin Films With NbN Paste](raw/sources/Superconducting_Connections_Between_NbTi_Thin_Films_With_NbN_Paste.pdf)
