---
title: "NBTI Performance Enhancement with Process Integration of High Current Fluorine Incorporation and O2 Gasher Process in 45nm CMOS Technology"
type: source
tags: [nbti, fluorine, process-integration, nbti-mitigation, plasma-treatment, 45nm, interface-engineering]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/NBTI_performance_enhancement_with_process_integration_of_High_Current_Fluorine_incorporation_and_O2_gas_asher_process_in_45nm_CMOS_technology.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/nbti-mitigation", "NBTI Mitigation"]]
---

# NBTI Performance Enhancement with Process Integration of High Current Fluorine Incorporation and O2 Gasher Process in 45nm CMOS Technology

## Summary
本文通过**高电流氟离子注入 + O₂等离子清洗工艺**减轻 45nm CMOS 节点的 NBTI 退化。氟注入钝化 Si-H 键（用更强的 Si-F 键替代），O₂等离子处理去除界面污染，双重工艺协同显著改善 NBTI 稳定性。

## Key Findings

### Fluorine Incorporation Mechanism
- **Fluorine** 注入到 Si/SiO₂ 界面
- **F 替代 H**：Si-F 键能（~5.5 eV）比 Si-H 键能（~3.5 eV）更高
- **更强的钝化**：Si-F 键更难断裂 → NBTI 退化减少
- **注入能量/剂量**：需要优化（过多 F 会损伤晶格）

### O2 Plasma Asher Process
- **O₂等离子清洗**：去除光刻胶残留和界面碳污染
- **界面清洁**：更少的界面缺陷 → 更少的 NBTI 退化位点
- **HfO₂/high-k 界面**：等离子处理改善界面质量

### Process Sequence
1. **High-current F 注入**（大束流，F 离子轰击）
2. **RTA（快速热退火）**：激活 F，修复注入损伤
3. **O₂ plasma asher**：界面清洁处理
4. **HfO₂沉积**（high-k栅介质）

### NBTI Improvement Results
- **ΔVth 减少 30-50%**（相比无 F 处理）
- **Interface trap density Dit 减少 40%**
- **NBTI 激活能 Ea 增加** → 温度加速效应降低
- **HCI 影响**：F 注入对 HCI 影响需评估（可能轻微恶化）

## Comparison with Other NBTI Mitigation
| 方法 | 效果 | 代价 |
|------|------|------|
| **F 注入** | ΔVth ↓ 30-50% | 工艺复杂，可能轻微影响 HCI |
| **SiGe** | 性能提升 | 成本增加 |
| **HCl 清洗** | 中等改善 | 工艺兼容性 |
| **Gate dielectric** | 等效氧化层缩薄 | 栅极泄漏增加 |

## Process Integration Considerations
- **注入能量过高**：F 穿透太深，进入 bulk Si
- **注入能量过低**：F 未到达界面，钝化效果差
- **Annealing**：RTA 温度和时间需要 co-optimize
- **与现有 CMOS 工艺的兼容性**：不破坏现有器件性能

## Related
- [[concepts/nbti]] — NBTI 机制
- [[concepts/nbti-mitigation]] — NBTI 缓解技术

## Source
[NBTI Performance Enhancement with Process Integration of High Current Fluorine Incorporation and O2 Gasher Process in 45nm CMOS Technology](raw/sources/NBTI_performance_enhancement_with_process_integration_of_High_Current_Fluorine_incorporation_and_O2_gas_asher_process_in_45nm_CMOS_technology.pdf)
