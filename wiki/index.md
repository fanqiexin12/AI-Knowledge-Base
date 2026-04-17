# Wiki Index

A catalog of all pages in this wiki.

## Overview
This wiki follows the three-layer architecture: **raw sources** (immutable) → **wiki** (LLM-maintained) → **schema** (conventions).

## Entities (3)
- [[entities/nbn]] — NbN（氮化铌），Tc ≈ 17K，Hc2 ≈ 50T，用于超导接头膏体 — sources: 1
- [[entities/nb3sn]] — Nb₃Sn（铌三锡），Tc ≈ 18K，Hc2 ≈ 25-30T，14T+ MRI 磁体用高场超导体 — sources: 1
- [[entities/nbti]] — NbTi（铌钛合金），Tc ≈ 9.5K，Hc2 ≈ 14T，MRI/NMR 磁体最广泛使用的超导体 — sources: 3

## Concepts (22)
- [[concepts/ac-nbti]] — AC NBTI：PMOS NBTI + NMOS PBTI 共同作用，VM 向 NMOS 侧漂移，duty cycle 影响退化分布 — sources: 2
- [[concepts/circuit-aging]] — 电路老化：NBTI/PBTI/HCI/EM 导致 timing degradation，10年退化可达 10-20% — sources: 3
- [[concepts/dram]] — DRAM（动态随机存取存储器）：1T1C 结构，NBTI 导致 retention time 退化，需 adaptive refresh — sources: 1
- [[concepts/em-tdds]] — EM（电迁移）和 TDDB（时变介质击穿）：先进节点互联两大失效机制 — sources: 2
- [[concepts/esd]] — ESD（静电放电）保护：ESD 与 NBTI/HCI 相互作用，复合失效模式 — sources: 1
- [[concepts/finfet]] — FinFET（鳍式场效应晶体管）：3D 栅极结构，3面包覆沟道，22nm-7nm 主流架构；Fin Width 10-15nm 为 HCI/NBTI 最佳平衡 — sources: 2
- [[concepts/gan-hemt]] — GaN HEMT（氮化镓高电子迁移率晶体管）：2DEG 沟道，宽禁带，高压/高温/高频应用 — sources: 1
- [[concepts/hci]] — HCI（热载流子注入）：高 Vds 下热载流子注入氧化层，PD-SOI 中比 Bulk 更严重；NBTI-HCI 协同退化 — sources: 3
- [[concepts/interconnect-reliability]] — 互联可靠性：EM/TDDB/应力迁移，7nm 节点电流密度 >10 MA/cm² — sources: 2
- [[concepts/iter]] — ITER（国际热核聚变实验堆）：全球最大聚变项目，Q=10，tokamak 装置，超导磁体系统 — sources: 1
- [[concepts/nbti]] — NBTI（负偏置温度不稳定性）：p-FET 负偏置高温退化；压应变恶化；DC > AC > 高频；SOI 有 history effect；GaN 有 free holes 机制；DRAM retention time 退化；oxide trap-assisted 模型；self-heating 加剧；hydrogen incorporation 缓解；GeOI 更敏感；ZrO₂ 优于 HfO₂ — sources: 25
- [[concepts/nbti-frequency-effect]] — NBTI 频率效应：频率越高 NBTI 越弱（recovery 充足），f > 1 MHz 可忽略；DC 是 worst case — sources: 2
- [[concepts/nbti-mitigation]] — NBTI 缓解技术：Gate Merging、Fluorine 注入、Adaptive Body Bias、Signal Probability Control — sources: 5
- [[concepts/nanosheet-fet]] — Nanosheet FET (GAA) 架构：3nm/2nm 节点主流，堆叠多层水平纳米片，4面栅极环绕 — sources: 2
- [[concepts/on-chip-aging-sensor]] — 片上老化传感器：Ring Oscillator、Vth extraction 传感器，用于实时监测 NBTI 退化；Cache BIST 监测 — sources: 3
- [[concepts/pbti]] — PBTI（正偏置温度不稳定性）：n-FET 正偏置高温退化，张应变恶化；AC NBTI 中 NMOS 也承受 PBTI — sources: 2
- [[concepts/soi-mosfet]] — SOI MOSFET（PD-SOI/FD-SOI）：BOX 介质隔离，PD-SOI 有 floating-body 效应，HCI 更严重，NBTI 有 history effect，自加热加剧 NBTI — sources: 2
- [[concepts/sram]] — SRAM（静态随机存取存储器）：6T 单元，高速缓存，BTI 影响 SNM 和 sense amplifier offset；GeOI 更敏感；Signal probability control；Bit-line boosting — sources: 6
- [[concepts/strain-engineering]] — 应变工程：提升性能但与可靠性存在 tradeoff；NBTI/PBTI 响应相反；halo implant channeling 加剧 PMOS NBTI — sources: 2
- [[concepts/superconducting-joint]] — 超导接头技术：零电阻连接，MRI 持久模式运行关键，Nb₃Sn/NbTi 扩散焊接，Nb₃Hf 无铅接头 — sources: 2
- [[concepts/variability-sources]] — 先进制程器件变异性来源：WFV/LER/MGG/厚度波动，RDD 在 7nm 节点显著 — sources: 2
- [[concepts/wide-bandgap]] — 宽禁带半导体：GaN/SiC，带隙 3+ eV，高压/高温/高频应用 — sources: 1

## Sources (44)
- [[sources/7nm-yield-reliability-challenges]] — 7nm 及以下良率和可靠性挑战：RDD/WFV/variability/EUV/EM 等多重挑战 — date: 2026-04-14
- [[sources/9.2t-nbti-mri-magnet-design]] — 9.2T NbTi MRI 磁体设计研究：多线圈结构，±50ppm 均匀度，600mm 室温孔径 — date: 2026-04-14
- [[sources/ac-nbti-coarse-graining-model]] — AC-NBTI 模型粗粒化方法：多时间尺度问题聚合快动力学变量，加速电路仿真 — date: 2026-04-14
- [[sources/analysis-and-impacts-of-nbti]] — NBTI 电路级影响综述：SRAM SNM 退化、Ring Oscillator 频率下降、 Sense Amplifier Voffset 增加、DRAM retention time 缩短 — date: 2026-04-16
- [[sources/bti-sram-sense-amplifier]] — BTI 对 SRAM 灵敏放大器影响：Voffset 增加，SNM 退化 20-30%，read failure 风险 — date: 2026-04-14
- [[sources/cmos-inverter-nbti-ac-dc]] — CMOS inverter AC/DC NBTI 可靠性：DC 下 PMOS NBTI 主导；AC 下 PMOS NBTI + NMOS PBTI 共同作用 — date: 2026-04-14
- [[sources/dram-nbti-review]] — DRAM NBTI 综述：retention time 退化、refresh 频率增加、write margin 退化；adaptive refresh、ECC 等缓解方案 — date: 2026-04-16
- [[sources/euv-interconnect-reliability-7nm]] — EUV 互联可靠性：Cu/Co/Ru 材料，J > 10 MA/cm²，EM/TDDB 成为主要失效机制 — date: 2026-04-14
- [[sources/esd-nbti-hci-interaction-65nm]] — ESD 与 NBTI/HCI 相互作用：ESD 加速老化，老化后 ESD 阈值降低，复合失效模式 — date: 2026-04-14
- [[sources/finfet-nbti-tolerant-wide-fan-in-dynamic-logic]] — FinFET 宽扇入动态逻辑 NBTI tolerant 技术：Gate Merging 消除关键内部节点 — date: 2026-04-14
- [[sources/fin-width-hc-nbti-mugfet]] — MuGFET Fin Width 优化指南：10-15nm 为 HCI/NBTI 最佳平衡；narrow fin HCI 严重，wide fin NBTI 严重 — date: 2026-04-16
- [[sources/fluorine-dose-energy-nbti-pimplant]] — 氟离子 dose/能量对 NBTI 的影响：F dose 5×10¹⁴-1×10¹⁵ cm⁻² 最佳；p-implant 顺序影响 F 保留率 — date: 2026-04-16
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
- [[sources/oxide-trap-assisted-nbti-model]] — Oxide trap-assisted NBTI 模型：氧化层陷阱贡献显著；stretched exponential recovery；定量预测频率效应 — date: 2026-04-16
- [[sources/soi-floating-body-nbti-hci]] — PD-SOI floating-body 效应：NBTI 有 history effect，HCI 比 Bulk 更严重 — date: 2026-04-14
- [[sources/superconducting-connections-nbti-nbn]] — NbTi 超导连接：NbN paste + HNA 处理，Ic 从 10A 提升 — date: 2026-04-14
- [[sources/nbti-self-heating-highk-soi-finfet]] — High-k SOI FinFET 自加热效应：BOX 热阻导致温度升高 20-40°C，Arrhenius 加速 NBTI — date: 2026-04-16
- [[sources/deep-experimental-nbti-cmos-inverter-reliability]] — CMOS Inverter NBTI 可靠性：Vth 漂移 ~50mV，V_M 漂移 ~30mV，noise margin 退化 10-15% — date: 2026-04-16
- [[sources/polysilicon-tft-cmos-inverter-nbti-self-recovery]] — Poly-Si TFT CMOS Inverter 自恢复：70-80% 降解可逆，晶界陷阱 + 界面态机制 — date: 2026-04-16
- [[sources/halo-implant-channeling-enhanced-pmos-nbti]] — Halo implant channeling：引入局部压应变，NBTI 加剧 30-50% — date: 2026-04-16
- [[sources/finfet-nbti-hydrogen-self-heating-recovery]] — FinFET 氢钝化 + 自加热恢复：H 注入减少 ΔVth 30-50%，自加热增强 recovery 20-30% — date: 2026-04-16
- [[sources/nbti-35nm-cmos-digital-circuits]] — 35nm CMOS 数字电路 NBTI：10年延时增加 13-17%，Ring Oscillator 频率下降 8% — date: 2026-04-16
- [[sources/nbti-temporal-performance-degradation-digital-circuits]] — 数字电路时域性能退化：10年速度退化 15-20%，recovery 效应 25-40% — date: 2026-04-16
- [[sources/nbti-pbti-geoi-sram]] — GeOI 6T SRAM NBTI/PBTI：GeOI 迁移率高但 Dit 高，125°C 下 10⁶s SNM 失效 — date: 2026-04-16
- [[sources/zro2-hfo2-nbti-reliability]] — ZrO₂ vs HfO₂ 栅介质：ZrO₂ k~25，NBTI 表现更好，ΔVth 低 30-50% — date: 2026-04-16
- [[sources/nb3hf-superconducting-joint]] — Nb₃Hf 无铅超导接头：接头电阻 <0.5 nΩ，>12T 工作，HIP+扩散退火工艺 — date: 2026-04-16
- [[sources/nbti-control-techniques-hkmg-dram]] — HKMG DRAM NBTI 控制：F 注入减少 ΔVth 30-50%，retention time 恢复至接近 64ms — date: 2026-04-16
- [[sources/nbti-hci-separation-recovery]] — NBTI/HCI 分离方法：温度域/时间域分离，NBTI 可恢复 25-40%，HCI 几乎不可恢复 — date: 2026-04-16
- [[sources/signal-probability-nbti-sram]] — SRAM Signal Probability Control：数据模式优化减少 NBTI 20-40%，data inversion + wear leveling — date: 2026-04-16
- [[sources/reliable-cache-nbti-bist]] — Cache BIST 监测 NBTI：Ring oscillator 传感器嵌入，退化超阈值触发数据迁移，寿命延长 2-3x — date: 2026-04-16
- [[sources/nbti-hci-soi-pmosfet]] — 65nm SOI NBTI+HCI 复合退化：concurrent stress ΔVth 60-70mV，协同因子 1.3-1.5x — date: 2026-04-16
- [[sources/pmos-nbti-minimization-robust-design]] — PMOS NBTI 建模与最小化：ΔVth(t)=A×t^n，寿命预测 10yr ΔVth~50-80mV — date: 2026-04-16
- [[sources/nbti-detection-adaptive-body-bias]] — Adaptive Body Bias NBTI 检测：FBB 补偿 Vth，寿命延长 2-3x，power overhead <5% — date: 2026-04-16
- [[sources/hfo2-14nm-finfet-nbti-thermal-treatment]] — 14nm FinFET HfO₂ 热处理优化：后沉积退火减少 Dit，ΔVth 降低 20-30% — date: 2026-04-16
- [[sources/nbti-aware-sram-bit-line-voltage]] — NBTI 感知 Bit-line Voltage 控制：升压 Vdd 补偿 read stability 退化，改善 15-20% — date: 2026-04-16

## Syntheses (0)
_No syntheses yet. Ask questions to generate analyses._

## Recent Updates
- **2026-04-16**: 13 new papers from OneDrive — GeOI SRAM, ZrO₂ gate dielectric, Nb₃Hf joint, HKMG DRAM, NBTI-HCI separation, Signal Probability Control, Cache BIST, Adaptive Body Bias, Bit-line voltage, 35nm CMOS data. Updated NBTI (25 sources), SRAM, HCI, FinFET, DRAM, Circuit-aging, Superconducting-joint concept pages. Wiki now has 44 sources, 22 concepts.
- **2026-04-14**: Batch ingest 16 new papers (NBTI mechanisms, circuits, models, mitigation; GaN HEMT; interconnect reliability; superconductivity; SRAM; aging sensors; ITER)
