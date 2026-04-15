# Wiki Index

A catalog of all pages in this wiki.

## Overview
This wiki follows the three-layer architecture: **raw sources** (immutable) → **wiki** (LLM-maintained) → **schema** (conventions).

## Entities (3)
- [[entities/nbn]] — NbN（氮化铌），Tc ≈ 17K，Hc2 ≈ 50T，用于超导接头膏体 — sources: 1
- [[entities/nb3sn]] — Nb₃Sn（铌三锡），Tc ≈ 18K，Hc2 ≈ 25-30T，14T+ MRI 磁体用高场超导体 — sources: 1
- [[entities/nbti]] — NbTi（铌钛合金），Tc ≈ 9.5K，Hc2 ≈ 14T，MRI/NMR 磁体最广泛使用的超导体 — sources: 3

## Concepts (20)
- [[concepts/ac-nbti]] — AC NBTI：PMOS NBTI + NMOS PBTI 共同作用，VM 向 NMOS 侧漂移，duty cycle 影响退化分布 — sources: 2
- [[concepts/circuit-aging]] — 电路老化：NBTI/PBTI/HCI/EM 导致 timing degradation，10年退化可达 10-20% — sources: 3
- [[concepts/em-tdds]] — EM（电迁移）和 TDDB（时变介质击穿）：先进节点互联两大失效机制 — sources: 2
- [[concepts/esd]] — ESD（静电放电）保护：ESD 与 NBTI/HCI 相互作用，复合失效模式 — sources: 1
- [[concepts/finfet]] — FinFET（鳍式场效应晶体管）：3D 栅极结构，3面包覆沟道，22nm-7nm 主流架构 — sources: 1
- [[concepts/gan-hemt]] — GaN HEMT（氮化镓高电子迁移率晶体管）：2DEG 沟道，宽禁带，高压/高温/高频应用 — sources: 1
- [[concepts/hci]] — HCI（热载流子注入）：高 Vds 下热载流子注入氧化层，PD-SOI 中比 Bulk 更严重 — sources: 1
- [[concepts/interconnect-reliability]] — 互联可靠性：EM/TDDB/应力迁移，7nm 节点电流密度 >10 MA/cm² — sources: 2
- [[concepts/iter]] — ITER（国际热核聚变实验堆）：全球最大聚变项目，Q=10，tokamak 装置，超导磁体系统 — sources: 1
- [[concepts/nbti]] — NBTI（负偏置温度不稳定性）：p-FET 负偏置高温退化；压应变恶化；DC > AC > 高频；SOI 有 history effect；GaN 有 free holes 机制 — sources: 13
- [[concepts/nbti-frequency-effect]] — NBTI 频率效应：频率越高 NBTI 越弱（recovery 充足），f > 1 MHz 可忽略；DC 是 worst case — sources: 2
- [[concepts/nbti-mitigation]] — NBTI 缓解技术：Gate Merging、Fluorine 注入、Adaptive Body Bias、Input Vector Control — sources: 3
- [[concepts/nanosheet-fet]] — Nanosheet FET (GAA) 架构：3nm/2nm 节点主流，堆叠多层水平纳米片，4面栅极环绕 — sources: 2
- [[concepts/on-chip-aging-sensor]] — 片上老化传感器：Ring Oscillator、Vth extraction 传感器，用于实时监测 NBTI 退化 — sources: 2
- [[concepts/pbti]] — PBTI（正偏置温度不稳定性）：n-FET 正偏置高温退化，张应变恶化；AC NBTI 中 NMOS 也承受 PBTI — sources: 2
- [[concepts/soi-mosfet]] — SOI MOSFET（PD-SOI/FD-SOI）：BOX 介质隔离，PD-SOI 有 floating-body 效应，HCI 更严重，NBTI 有 history effect — sources: 1
- [[concepts/sram]] — SRAM（静态随机存取存储器）：6T 单元，高速缓存，BTI 影响 SNM 和 sense amplifier offset — sources: 2
- [[concepts/strain-engineering]] — 应变工程：提升性能但与可靠性存在 tradeoff；NBTI/PBTI 响应相反 — sources: 1
- [[concepts/superconducting-joint]] — 超导接头技术：零电阻连接，MRI 持久模式运行关键，Nb₃Sn/NbTi 扩散焊接 — sources: 2
- [[concepts/variability-sources]] — 先进制程器件变异性来源：WFV/LER/MGG/厚度波动，RDD 在 7nm 节点显著 — sources: 2
- [[concepts/wide-bandgap]] — 宽禁带半导体：GaN/SiC，带隙 3+ eV，高压/高温/高频应用 — sources: 1

## Sources (21)
- [[sources/7nm-yield-reliability-challenges]] — 7nm 及以下良率和可靠性挑战：RDD/WFV/variability/EUV/EM 等多重挑战 — date: 2026-04-14
- [[sources/9.2t-nbti-mri-magnet-design]] — 9.2T NbTi MRI 磁体设计研究：多线圈结构，±50ppm 均匀度，600mm 室温孔径 — date: 2026-04-14
- [[sources/ac-nbti-coarse-graining-model]] — AC-NBTI 模型粗粒化方法：多时间尺度问题聚合快动力学变量，加速电路仿真 — date: 2026-04-14
- [[sources/bti-sram-sense-amplifier]] — BTI 对 SRAM 灵敏放大器影响：Voffset 增加，SNM 退化 20-30%，read failure 风险 — date: 2026-04-14
- [[sources/cmos-inverter-nbti-ac-dc]] — CMOS inverter AC/DC NBTI 可靠性：DC 下 PMOS NBTI 主导；AC 下 PMOS NBTI + NMOS PBTI 共同作用 — date: 2026-04-14
- [[sources/euv-interconnect-reliability-7nm]] — EUV 互联可靠性：Cu/Co/Ru 材料，J > 10 MA/cm²，EM/TDDB 成为主要失效机制 — date: 2026-04-14
- [[sources/esd-nbti-hci-interaction-65nm]] — ESD 与 NBTI/HCI 相互作用：ESD 加速老化，老化后 ESD 阈值降低，复合失效模式 — date: 2026-04-14
- [[sources/finfet-nbti-tolerant-wide-fan-in-dynamic-logic]] — FinFET 宽扇入动态逻辑 NBTI tolerant 技术：Gate Merging 消除关键内部节点 — date: 2026-04-14
- [[sources/gate-merging-nbti-mitigation]] — Gate Merging NBTI 缓解方法：合并门电路消除 critical internal node，减少 timing degradation 30-50% — date: 2026-04-14
- [[sources/gan-hemt-nbti-free-holes]] — GaN-on-Si MOS-HEMT nBTI 机制：free holes（空穴气）导致 2DEG 退化，与 Si NBTI 机制不同 — date: 2026-04-14
- [[sources/impact-of-material-variability-nanosheet-fets]] — Nanosheet FET 可靠性仿真：variability 对 BTI 退化影响，WFV 是最大变异性来源 — date: 2026-04-14
- [[sources/io-oxide-nbti-tinv-scaling-20nm]] — 20nm RPG 工艺 I/O oxide 优化对 NBTI/Tinv scaling 的影响 — date: 2026-04-14
- [[sources/iter-nbti-conductor-assessment]] — ITER 主总线 NbTi 导体 DC 性能测试：CICC 导体 Ic、n 值、磁化强度评估 — date: 2026-04-14
- [[sources/nb3sn-nbti-superconducting-joint-14t-mri]] — Nb₃Sn-NbTi 超导接头：扩散焊接工艺，14T MRI 磁体，接头电阻 < 0.5 nΩ — date: 2026-04-14
- [[sources/nbti-fast-switching-ss-degradation]] — 快速开关 NBTI 表征方法：stress 期间超快速 SS 测量(<1μs)，避免恢复误差 — date: 2026-04-14
- [[sources/nbti-fluorine-incorporation-45nm]] — 45nm 氟离子注入 + O₂等离子清洗 NBTI 改善：Si-F 键替代 Si-H，ΔVth 减少 30-50% — date: 2026-04-14
- [[sources/nbti-frequency-dependence]] — NBTI 频率效应：f > 1 MHz NBTI 可忽略；DC stress 是 worst case — date: 2026-04-14
- [[sources/nbti-monitor-on-chip-sram]] — 6T SRAM 片上 NBTI 缓解传感器：自适应 body bias 补偿 Vth 漂移，寿命延长 — date: 2026-04-14
- [[sources/nbti-pbti-multiplexer-circuit]] — MUX 电路 NBTI/PBTI 影响：rise/fall time 退化，10年运行 τp 退化可达 15-25% — date: 2026-04-14
- [[sources/nbti-recovery-analog-cmos-circuits]] — 模拟 CMOS 电路 NBTI 恢复效应建模：transconductance gm 恢复，compact model 集成 — date: 2026-04-14
- [[sources/nbti-strain-dependence-sipmosfet]] — NBTI 应变效应：压应变加剧 NBTI、张应变减轻；Si-H 键能受应变调制 — date: 2026-04-14
- [[sources/nbti-two-stage-model-states-kinetics]] — Two-Stage NBTI 模型：interface trap creation + hole trapping，states kinetics 研究 — date: 2026-04-14
- [[sources/nitrogen-enhanced-nbti-universal-model]] — 氮增强 NBTI 效应：N clustering 形成 deep traps，universal prediction model 预测 — date: 2026-04-14
- [[sources/on-chip-nbti-tracking-monitor]] — 简单片上 NBTI 监测器：Ring oscillator 频率追踪，实时监测 IC 老化 — date: 2026-04-14
- [[sources/soi-floating-body-nbti-hci]] — PD-SOI floating-body 效应：NBTI 有 history effect，HCI 比 Bulk 更严重 — date: 2026-04-14
- [[sources/superconducting-connections-nbti-nbn]] — NbTi 超导连接：NbN paste + HNA 处理，Ic 从 10A 提升 — date: 2026-04-14

## Syntheses (0)
_No syntheses yet. Ask questions to generate analyses._

## Recent Updates
- **2026-04-14**: Batch ingest 16 new papers (NBTI mechanisms, circuits, models, mitigation; GaN HEMT; interconnect reliability; superconductivity; SRAM; aging sensors; ITER)
