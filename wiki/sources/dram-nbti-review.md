---
title: "Comprehensive Review of DRAM NBTI Issues and Solutions"
type: source
tags: [nbti, dram, refresh, vth-shift, reliability, memory]
created: 2026-04-16
updated: 2026-04-16
sources: ["raw/sources/A_Comprehensive_Review_of_DRAM_NBTI_Issues_and_Solutions.pdf"]
related: [["concepts/nbti", "NBTI"], ["concepts/sram", "SRAM"]]
---

# Comprehensive Review of DRAM NBTI Issues and Solutions

## Source Info
- **Title**: A Comprehensive Review of DRAM NBTI Issues and Solutions
- **Date**: 2026-04-16
- **Key topics**: DRAM reliability, NBTI in DRAM, refresh time, cell stability

## Key Findings

### DRAM NBTI Problem
- DRAM cell uses pMOS access transistor (for 1T1C structure)
- NBTI causes Vth increase in pMOS access transistor over time
- Impact: **cell discharge rate increases** → refresh interval must decrease

### Specific DRAM NBTI Issues

#### 1. Refresh Time Increase
- NBTI → Vth shift (ΔVth ≈ 20-50mV after 10 years)
- Retention time degrades from ~64ms to ~32ms or less
- Requires more frequent refresh → **power penalty**

#### 2. Write Margin Degradation
- Write margin decreases due to NBTI in access transistor
- Write failures can occur at low Vdd

#### 3. Read Disturb
- NBTI-induced Vth shift makes cells more susceptible to read disturb
- Half-selected cells may flip during read operation

### NBTI in Different DRAM Types

| DRAM Type | NBTI Impact | Severity |
|-----------|-------------|----------|
| **1T1C** | pMOS access transistor NBTI | High |
| **3T** | Multiple pMOS stages affected | Medium |
| **Gain Cell** | Read transistor NBTI | Medium |
| **eDRAM** | Similar to 1T1C | High |

### Solutions for DRAM NBTI

#### Circuit-Level
- **Adaptive refresh**: increase refresh frequency as NBTI accumulates
- **Error correction codes (ECC)**: correct occasional read errors
- **Word-line boosting**: increase write voltage to overcome NBTI

#### Process-Level
- **Fluorine incorporation**: same as CMOS NBTI mitigation
- **Nitrogen profile optimization**: reduce interface trap generation
- **High-k/metal gate**: reduces NBTI (but cost increase)

#### Architecture-Level
- **Wear leveling** for DRAM in memory controllers
- **Refresh scheduling** based on temperature and age
- **Redundancy**: spare rows/columns to replace degraded cells

### Key Differences: DRAM NBTI vs. SRAM NBTI
| Aspect | DRAM NBTI | SRAM NBTI |
|--------|-----------|-----------|
| Degraded component | Access transistor | Pull-up/pull-down PFET |
| Primary impact | Retention time | Static noise margin |
| Recovery | No (stored charge lost) | Partial recovery |
| Failure mode | Data loss (soft) | Read failure |

## Related
- [[concepts/nbti]] — NBTI concept page
- [[concepts/sram]] — SRAM (related memory structure)
