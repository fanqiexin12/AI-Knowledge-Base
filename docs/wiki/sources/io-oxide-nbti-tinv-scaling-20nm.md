---
title: "Effect of I/O Oxide Process Optimization on the NBTI Dependence of Tinv Scaling for a 20nm Bulk Planar Replacement Gate Process"
type: source
tags: [nbti, io-oxide, tinv, replacement-gate, 20nm, process-optimization, interface-engineering]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Effect_of_I_O_oxide_process_optimization_on_the_nbti_dependence_of_Tinv_scaling_for_a_20_nm_bulk_planar_Replacement_Gate_process.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/tinv-scaling", "Tinv Scaling"]]
---

# Effect of I/O Oxide Process Optimization on the NBTI Dependence of Tinv Scaling for a 20nm Bulk Planar Replacement Gate Process

## Summary
本文研究 **20nm bulk planar Replacement Gate (RPG) 工艺** 中 **I/O oxide 工艺优化** 对 **NBTI 退化与 Tinv（等效栅氧化层厚度）缩放关系** 的影响。关键发现：I/O oxide 界面处理（如氮化、界面 Oxide 调控）改变了 NBTI 退化与 Tinv 的 scaling behavior；优化后的工艺可在保持 NBTI 稳定性的同时实现更薄的 Tinv。

## Key Findings

### Replacement Gate (RPG) Process
- **Gate-first → Gate-last**：先形成 dummy gate，HfSiON/Poly-Si dummy
- **High-k 沉积**：HfO₂ 原子层沉积（ALD）
- **Metal gate 填充**：替代 dummy poly-Si
- **I/O area**：使用厚 oxide（5-10 nm）而非 core 用的 thin high-k

### Tinv Scaling Challenges
- **Thinner Tinv** → 更好静电控制 → 更高性能
- **Thinner Tinv** → 更严重 NBTI（更强的电场）
- **NBTI 对 Tinv 的依赖**：E_ox = Vgb / Tinv → 电场随 Tinv 缩放

### I/O Oxide Process Optimization
- **Interface oxide (IL) control**：SiO₂/SiON IL 的生长条件优化
- **Nitridation**：界面 N 含量调节（影响 NBTI）
- **Post-deposition anneal (PDA)**：HfO₂ 结晶度和界面质量改善

### NBTI vs Tinv Relationship
| Tinv | E_ox | NBTI ΔVth | Scaling Trend |
|------|------|-----------|--------------|
| **Thick** | 低 | 小 | NBTI 不显著 |
| **Thin** | 高 | 大 | NBTI 主导 |
| **Optimized IL** | 低（same Tinv）| 小 | 改善 scaling |

### Key Optimization Levers
- **IL thickness**：增加 IL 厚度可降低 E_ox（但增加 Tinv）
- **N-content in IL**：适当 N 改善 B-shielding，但过多会加重 NBTI
- **HfO₂ thickness**：high-k 厚度 vs IL 厚度权衡

## 20nm Node Specifics
- **Core devices**：thin high-k, Lg ~ 20 nm
- **I/O devices**：thick SiON/SiO₂, Lg ~ 100-200 nm
- **Integration challenge**：core 和 I/O 需要不同的 oxide 条件

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/tinv-scaling]] — Tinv scaling

## Source
[Effect of I/O Oxide Process Optimization on the NBTI Dependence of Tinv Scaling for a 20nm Bulk Planar Replacement Gate Process](raw/sources/Effect_of_I_O_oxide_process_optimization_on_the_nbti_dependence_of_Tinv_scaling_for_a_20_nm_bulk_planar_Replacement_Gate_process.pdf)
