---
title: "NbTi"
type: entity
tags: [superconductor, lts, mri-magnets, nbti-nbn-joint, low-temperature-superconductor]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Superconducting_Connections_Between_NbTi_Thin_Films_With_NbN_Paste.pdf"]
related: [["entities/nbn", "NbN"], ["concepts/superconducting-joint", "Superconducting Joint"], ["concepts/hta-hts", "HTS Materials"]]
---

# NbTi

## Summary
**NbTi（铌钛合金）** 是目前工业应用最广泛的**低温超导体 (LTS)**，主要用于 MRI/NMR 磁体（10kA–40kA 级导体）。其临界温度 Tc ≈ 9.5K，上临界场 Hc2 ≈ 14T（@4.2K）。

## Properties

| 参数 | 值 |
|------|-----|
| **化学成分** | Nb – 46.5 wt% Ti |
| **Tc（临界温度）** | 9.5 K |
| **Hc2（上临界场）** | 14 T @ 4.2K |
| **Jc（临界电流密度）** | ~3000 A/mm² @ 4.2K, 5T |
| **常用形态** | 多芯 NbTi/Cu 复合线材（filament + Cu matrix） |
| **工作温度** | 4.2 K（液氦） |

## Applications

- **MRI 磁体**：全球约 50,000+ 台，NbTi 是主力材料
- **NMR 磁体**：最高 ~28T 使用 NbTi（更高场用 Nb₃Sn 或 HTS）
- **高能物理**：CERN LHC 超导磁体（8T 级）
- **实验室磁体**：研究用 10–20T 级磁体

## Connection Challenge

NbTi 的超导接头是工业难题：
- Ti 表面易形成 TiOx 氧化层，阻碍电接触
- 传统 solder joint 接触电阻高（0.15–0.35 nΩ·cm²）
- 本研究使用 **NbN paste + HNA 表面处理** 实现更低阻连接

## Related
- [[entities/nbn]] — 高 Tc 超导材料，用于与 NbTi 的连接
- [[concepts/superconducting-joint]] — 接头技术
- [[concepts/hta-hts]] — 高 Tc 超导体（与 NbTi 对比）
