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
