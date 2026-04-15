---
title: "Fabrication and Test of Nb3Sn-NbTi Superconducting Joint for a 14-T MRI Magnet"
type: source
tags: [superconductor, nb3sn, nbti, superconducting-joint, mri-magnet, high-field, diffusion-bonding]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Fabrication_and_Test_of_Nb3Sn-NbTi_Superconducting_Joint_for_a_14-T_MRI_Magnet.pdf"]
related: [["entities/nbti", "NbTi"], ["entities/nb3sn", "Nb₃Sn"], ["concepts/superconducting-joint", "Superconducting Joint"]]
---

# Fabrication and Test of Nb3Sn-NbTi Superconducting Joint for a 14-T MRI Magnet

## Summary
本文实现 **Nb₃Sn 与 NbTi 超导体之间的超导接头**，用于 **14-T MRI 磁体**。采用 **diffusion bonding（扩散焊接）** 工艺，在 600-700°C 高温下实现 Nb₃Sn/NbTi 界面结合。接头在 14 T 强磁场下测试，性能满足 MRI 磁体要求。

## Key Findings

### Nb3Sn vs NbTi for High-Field MRI
| 参数 | NbTi | Nb₃Sn |
|------|------|-------|
| **Tc** | 9.5 K | 18 K |
| **Hc2** | 14 T | 25-30 T |
| **最高场** | ~10 T | >20 T |
| **工艺** | 挤出成型（简单） | bronze route / PIT（复杂） |
| **应变敏感性** | 低 | 高（应变敏感）|

### Why Join Nb3Sn to NbTi?
- **14 T MRI 需要 Nb₃Sn 高场超导体**
- **但 Nb₃Sn 工艺难度大**（需 600-700°C 热处理）
- **NbTi 接头技术成熟**，可在低温下工作
- **混合磁体设计**：高场区用 Nb₃Sn，低场区用 NbTi → 需要接头连接

### Diffusion Bonding Process
1. **表面处理**：机械抛光 + 化学清洗 Nb₃Sn 和 NbTi 表面
2. **堆叠**：Nb₃Sn / NbTi 层压结构
3. **扩散焊接**：600-700°C，high pressure (50-100 MPa)，惰性气氛
4. **热处理**：Nb₃Sn 形成反应（600°C 退火）
5. **测试**：液氦温度（4.2 K），14 T 磁场

### Joint Performance
- **接头电阻**：< 0.5 nΩ（目标 < 1 nΩ）
- **临界电流 Ic**：满足 MRI 磁体设计要求
- **磁场均匀性**：接头区域磁場扰动 < 0.1%
- **机械强度**：扩散焊接界面强度足够

## 14-T MRI Magnet Design Implications
- ** Nb₃Sn 提供中心高场（>10 T）**
- ** NbTi 提供外层低场区（<10 T）**
- **接头连接两种材料实现连续超导回路**
- **挑战**：Nb₃Sn 的应变敏感性（需控制接头应力）

## Related
- [[entities/nbti]] — NbTi 超导体
- [[entities/nb3sn]] — Nb₃Sn 超导体
- [[concepts/superconducting-joint]] — 超导接头技术

## Source
[Fabrication and Test of Nb3Sn-NbTi Superconducting Joint for a 14-T MRI Magnet](raw/sources/Fabrication_and_Test_of_Nb3Sn-NbTi_Superconducting_Joint_for_a_14-T_MRI_Magnet.pdf)
