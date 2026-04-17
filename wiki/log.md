# Wiki Log

Chronological record of wiki operations. Format: `## [YYYY-MM-DD] operation | description`

---

## [2026-04-14] init | Wiki initialized
- Action: Created initial structure
- Schema: CLAUDE.md with three-layer architecture
- Next: Add first source to `raw/sources/` and ingest

## [2026-04-14] ingest | Impact_of_Material_Variability_on_the_Reliability_of_Nanosheet_FETs.pdf
- Action: Extracted key findings, created source summary + 4 concept pages
- Files touched: sources/impact-of-material-variability-nanosheet-fets, concepts/nanosheet-fet, concepts/nbti, concepts/pbti, concepts/variability-sources, index.md, log.md
- Key findings: WFV is the dominant variability source; Multi-sheet nanosheet is more robust than single-sheet; NBTI affects p-FET, PBTI affects n-FET

## [2026-04-14] ingest | Superconducting_Connections_Between_NbTi_Thin_Films_With_NbN_Paste.pdf
- Action: Created source summary + 1 concept + 2 entity pages
- Files touched: sources/superconducting-connections-nbti-nbn, entities/nbti, entities/nbn, concepts/superconducting-joint, index.md, log.md
- Key findings: Ti surface oxidation阻碍电接触; HNA etching + NbN paste烧结实现超导连接

## [2026-04-14] ingest | Experimental_Study_on_NBTI_Degradation_Behaviors_in_Si_pMOSFETs_Under_Compressive_and_Tensile_Strains.pdf
- Action: Created source summary + 1 concept; updated NBTI and PBTI pages with strain effects
- Files touched: sources/nbti-strain-dependence-sipmosfet, concepts/strain-engineering, concepts/nbti (updated), concepts/pbti (updated), index.md, log.md
- Key findings: Compressive strain worsens NBTI; Tensile strain alleviates NBTI; Si-H bond energy modulated by strain

## [2026-04-14] ingest | Effect_of_Floating-Body_and_Stress_Bias_on_NBTI_and_HCI_on_65-nm_SOI_pMOSFETs.pdf
- Action: Created source summary + 2 concept pages; updated NBTI page
- Files touched: sources/soi-floating-body-nbti-hci, concepts/soi-mosfet, concepts/hci, concepts/nbti (updated), index.md, log.md
- Key findings: PD-SOI floating body causes NBTI history effect; HCI worse in PD-SOI than Bulk

## [2026-04-14] ingest | Delay_effects_and_frequency_dependence_of_NBTI + Reliability_analysis_of_CMOS_inverter_subjected_to_AC_and_DC_NBTI.pdf
- Action: Created 2 source summaries + 2 concept pages; updated NBTI page
- Files touched: sources/nbti-frequency-dependence, sources/cmos-inverter-nbti-ac-dc, concepts/nbti-frequency-effect, concepts/ac-nbti, concepts/nbti (updated), index.md, log.md
- Key findings: NBTI frequency dependence: f > 1 MHz negligible; DC is worst case; AC NBTI: PMOS NBTI + NMOS PBTI both contribute

## [2026-04-16] ingest | 13 new papers from OneDrive
- Action: Created 13 source summaries; updated NBTI, SRAM, HCI, FinFET, DRAM, Circuit-aging, Superconducting-joint, On-chip-aging-sensor, NBTI-mitigation concept pages
- New sources: nbti-35nm-cmos-digital-circuits, nbti-temporal-performance-degradation-digital-circuits, nbti-pbti-geoi-sram, zro2-hfo2-nbti-reliability, nb3hf-superconducting-joint, nbti-control-techniques-hkmg-dram, nbti-hci-separation-recovery, signal-probability-nbti-sram, reliable-cache-nbti-bist, nbti-hci-soi-pmosfet, pmos-nbti-minimization-robust-design, nbti-detection-adaptive-body-bias, hfo2-14nm-finfet-nbti-thermal-treatment, nbti-aware-sram-bit-line-voltage
- Key topics:
  - GeOI SRAM: higher mobility but more NBTI-sensitive, SNM fails at 10⁶s @ 125°C
  - ZrO₂ vs HfO₂: k~25 vs k~20, ZrO₂ ΔVth 30-50% lower
  - 35nm CMOS: 10yr delay increase 13-17%, RO freq degradation 8%
  - Concurrent HCI-NBTI in SOI: synergistic factor 1.3-1.5x
  - SRAM Signal Probability Control: data pattern optimization reduces NBTI 20-40%
  - Adaptive Body Bias: lifetime extension 2-3x, power overhead <5%
  - Cache BIST monitoring: lifetime extension 2-3x via data migration
  - Nb₃Hf joint: Pb-free, R < 0.5nΩ, works at >12T

## [2026-04-16] ingest | 5 new papers (self-heating, inverter, halo implant, H incorporation)
- Action: Created 5 source summaries; updated NBTI, FinFET, SOI MOSFET, Strain Engineering, Circuit Aging concept pages
- New sources: nbti-self-heating-highk-soi-finfet, deep-experimental-nbti-cmos-inverter-reliability, polysilicon-tft-cmos-inverter-nbti-self-recovery, halo-implant-channeling-enhanced-pmos-nbti, finfet-nbti-hydrogen-self-heating-recovery
- Updated concepts: nbti (added self-heating, CMOS inverter, halo implant, H incorporation sections), finfet (added self-heating, H incorporation), soi-mosfet (added self-heating), strain-engineering (added halo implant channeling), circuit-aging (added CMOS inverter aging)
- Key topics:
  - Self-heating in SOI/FinFET: 20-40°C temperature rise, accelerates NBTI by Arrhenius
  - CMOS inverter NBTI: Vth shift ~50mV, V_M shift ~30mV, noise margin degradation 10-15%
  - Poly-Si TFT self-recovery: 70-80% degradation reversible
  - Halo implant channeling: compressive strain worsens NBTI 30-50%
  - Hydrogen incorporation: ΔVth reduced 30-50%, enhanced recovery 20-30%

## [2026-04-16] ingest | 5 new papers
- Action: Created 5 source summaries, updated NBTI and FinFET concept pages, created new DRAM concept
- New sources: analysis-and-impacts-of-nbti, fluorine-dose-energy-nbti-pimplant, oxide-trap-assisted-nbti-model, fin-width-hc-nbti-mugfet, dram-nbti-review
- New concepts: dram
- Updated concepts: nbti (added oxide trap model, DRAM NBTI, circuit impacts), finfet (added fin width optimization)
- Key topics:
  - NBTI circuit impacts: SRAM, Ring Oscillator, Sense Amplifier, DRAM retention
  - Oxide trap-assisted degradation model (stretched exponential)
  - F dose/energy optimization for NBTI mitigation
  - MuGFET fin width tradeoff: HCI vs NBTI
  - DRAM NBTI: retention time degradation, adaptive refresh

## [2026-04-15] batch-ingest | 16 new papers
- Action: Batch processed 16 new papers
- New sources: 15 new source summaries created
- New concepts: 9 new concept pages (circuit-aging, em-tdds, esd, finfet, gan-hemt, interconnect-reliability, iter, nbti-mitigation, on-chip-aging-sensor, sram, wide-bandgap)
- New entities: 1 new entity (Nb3Sn)
- Updated concepts: nbti (updated with GaN free holes mechanism, fluorine mitigation, nitrogen-enhanced NBTI, two-stage model), nanosheet-fet (updated)
- Key topics covered:
  - NBTI mechanisms: two-stage model, nitrogen-enhanced, fast-switching characterization, coarse-grained AC model
  - NBTI circuit impact: SRAM sense amplifier, multiplexer, analog CMOS recovery
  - NBTI mitigation: gate merging, fluorine incorporation, FinFET tolerance
  - GaN HEMT reliability: free holes in nBTI degradation
  - Interconnect: EUV reliability, EM/TDDB at 7nm
  - Superconductivity: Nb3Sn-NbTi joint for 14T MRI, ITER busbar, 9.2T MRI magnet design
  - ESD-NBTI-HCI interaction
  - On-chip aging sensors
