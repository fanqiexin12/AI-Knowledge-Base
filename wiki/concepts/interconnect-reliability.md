---
title: "Interconnect Reliability"
type: concept
tags: [interconnect, reliability, electromigration, tdds, copper, low-k, euv, 7nm]
created: 2026-04-14
updated: 2026-04-14
sources: ["raw/sources/Reliability_on_EUV_Interconnect_Technology_for_7nm_and_beyond.pdf", "raw/sources/Yield_and_Reliability_Challenges_at_7nm_and_Below.pdf"]
related: [["concepts/em-tdds", "EM and TDDB"], ["concepts/circuit-aging", "Circuit Aging"]]
---

# Interconnect Reliability

## Summary
互联可靠性（Interconnect reliability）研究芯片内部金属布线（铜/低k介质）在高电流密度和高电场下的失效机制。随着工艺节点缩小，互联可靠性问题日益严峻——**electromigration (EM)** 和 **TDDB** 成为 7nm 及以下节点的主要失效模式。

## Key Failure Mechanisms

### Electromigration (EM)
- **机制**：铜原子在高电流密度下迁移
- **失效**：viod 形成 → 电阻增加/开路
- **激活能**：~0.8-1.0 eV（Cu 晶界扩散）
- **电流密度 J > 10 MA/cm²**（7nm 节点）

### TDDB (Time Dependent Dielectric Breakdown)
- **机制**：低k介质在长时间高电场下击穿
- **失效**：漏电流增加 → 短路
- **与 EUV 相关**：光刻胶残留可能引入介质缺陷

### Stress Migration (SM)
- **机制**：热膨胀系数失配导致机械应力
- **失效**：金属断裂/界面脱粘

## Technology Node Evolution

| 节点 | 金属化 | 主要挑战 |
|------|--------|---------|
| **28nm** | Cu, SiO₂ | Cu EM |
| **14nm** | Cu, low-k | Via EM, TDDB |
| **7nm** | Cu/Co/Ru | J > 10 MA/cm², EUV defects |
| **5nm** | Co/Ru | 新材料可靠性 |

## Advanced Materials
- **Cobalt (Co)**：比 Cu 更抗 EM
- **Ruthenium (Ru)**：可直接镀覆，无阻挡层
- **Mo 合金**：高熔点，低电阻

## Related
- [[concepts/em-tdds]] — EM 和 TDDB 机制
- [[concepts/circuit-aging]] — 电路老化
