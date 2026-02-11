# Heber Campus Master Financial Model — Agent B Rev 1

**Document:** Heber_Master_CFO_AgentB_Rev1
**Source:** `Z:\SE_T1\Bible\Agent B\Heber_Master_CFO_AgentB_Rev1.xlsx`
**Date:** 2026-02-06
**Classification:** INTERNAL / PROPRIETARY
**Basis:** Bible Rev 4.1.1 locked parameters

---

## Sheet Overview

| # | Sheet | Purpose |
|---|-------|---------|
| 1 | ASSUMPTIONS | Master inputs — timeline, generation, fuel, power, DC, overhead, CapEx, market benchmarks |
| 2 | P&L_CONSOLIDATED | Consolidated P&L with revenue, COGS, EBITDA, net cash flow, key ratios |
| 3 | VOLUME_DRIVERS | Physical units — BPD, power MW, DC buildings, campus totals |
| 4 | CAPEX_RETURNS | Capital expenditure breakdown, DSCR, EBITDA/CapEx, simple payback |
| 5 | FUELS_ECONOMICS | Production cost vs market pricing for diesel, jet, propane, WTI |
| 6 | DC_ECONOMICS | Data center colocation vs AI/HPC revenue, COGS, margins |
| 7 | SENSITIVITY | Static scenario table — base/downside/upside for key variables |
| 8 | SOURCES | Audit trail — FRED URLs, Bible references for all data points |

---

## 1. ASSUMPTIONS

### Timeline

| Parameter | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-----------|---------|---------|---------|---------|---------|---------|
| Construction Start (Year) | 2027 | 2029 | 2031 | 2033 | 2035 | 2037 |
| COD (Commercial Operation) | 2030 | 2032 | 2034 | 2036 | 2038 | 2040 |
| PFTs Online (Cumulative) | 2 | 4 | 6 | 8 | 10 | 12 |

### Generation Capacity (per PFT)

| Source | Value | Notes |
|--------|-------|-------|
| AP1000 Nuclear (MWe per PFT) | 1,100 | Bible Rev 4.1.1 — 1 AP1000 per PFT |
| Biomass Total Campus (MWe) | 1,000 | Bible Rev 4.1.1 — single campus plant |
| Solar Perimeter Campus (MWe) | 5,000 | Bible Rev 4.1.1 — non-firm |
| Tail Gas Turbines (MWe per PFT) | 100 | Bible Rev 4.1.1 |
| Steam Turbines (MWe per PFT) | 20 | Bible Rev 4.1.1 |
| LPG Turbines Emergency (MWe per PFT) | 36 | Bible Rev 4.1.1 — non-firm |

### Fuel Production

| Parameter | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-----------|---------|---------|---------|---------|---------|---------|
| BPD per PFT | 13,000 | 13,000 | 13,000 | 13,000 | 13,000 | 13,000 |
| Direct Production Cost ($/bbl) | 70 | 68 | 66 | 65 | 63 | 60 |
| Diesel Yield (%) | 55% | 55% | 55% | 55% | 55% | 55% |
| Jet Fuel Yield (%) | 25% | 25% | 25% | 25% | 25% | 25% |
| Propane/LPG Yield (%) | 15% | 15% | 15% | 15% | 15% | 15% |
| Naphtha/Other Yield (%) | 5% | 5% | 5% | 5% | 5% | 5% |
| Diesel Sell Price ($/gal) | 2.55 | 2.30 | 2.15 | 2.05 | 1.98 | 1.92 |
| Jet Sell Price ($/gal) | 2.50 | 2.25 | 2.10 | 2.02 | 1.96 | 1.90 |
| Propane Sell Price ($/gal) | 0.85 | 0.80 | 0.78 | 0.76 | 0.74 | 0.73 |

### Power Sales

| Parameter | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-----------|---------|---------|---------|---------|---------|---------|
| Avg Export Price ($/MWh) | 45 | 45 | 47 | 47 | 48 | 48 |
| Power COGS as % of Revenue | 50% | 47% | 50% | 49% | 49% | 49% |
| Internal Consumption (MW avg) | 2,060 | 3,870 | 5,880 | 7,890 | 9,900 | 12,010 |

### Data Center

| Parameter | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-----------|---------|---------|---------|---------|---------|---------|
| Colocation Buildings (cumulative) | 4 | 4 | 6 | 8 | 10 | 12 |
| AI/HPC Buildings (cumulative) | 0 | 4 | 6 | 8 | 10 | 12 |
| Revenue per Colo Bldg ($M/yr) | 37.5 | 75 | 58 | 56 | 55 | 54 |
| Revenue per AI Bldg ($M/yr) | 0 | 100 | 142 | 125 | 125 | 121 |
| DC COGS as % of Revenue | 40% | 17% | 15% | 15% | 14% | 14% |

### Other Revenue & Costs ($B)

| Parameter | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-----------|---------|---------|---------|---------|---------|---------|
| Oxygen Sales | 0.02 | 0.05 | 0.08 | 0.12 | 0.15 | 0.18 |
| Mineral Pellets | 0.01 | 0.01 | 0.02 | 0.03 | 0.04 | 0.05 |
| Software Licensing | 0 | 0.01 | 0.03 | 0.05 | 0.07 | 0.10 |
| Other COGS | 0.01 | 0.02 | 0.03 | 0.04 | 0.05 | 0.06 |

### Overhead & Financing ($B)

| Parameter | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-----------|---------|---------|---------|---------|---------|---------|
| Campus Overhead | 0.23 | 0.25 | 0.35 | 0.42 | 0.45 | 0.48 |
| Debt Service | 0.22 | 0.37 | 0.90 | 1.00 | 1.10 | 1.10 |

### Capital Expenditure ($B)

| Component | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-----------|---------|---------|---------|---------|---------|---------|
| Nuclear (AP1000 x PFTs) | 4.0 | 4.0 | 4.0 | 4.0 | 4.0 | 4.0 |
| FT Synthesis Plant | 1.5 | 1.5 | 1.5 | 1.5 | 1.5 | 1.5 |
| Data Centers | 0.4 | 0.8 | 0.6 | 0.6 | 0.6 | 0.6 |
| Solar Array | 1.0 | 0 | 0.8 | 0 | 0.8 | 0 |
| Balance of Plant | 0.8 | 0.5 | 0.5 | 0.5 | 0.5 | 0.5 |
| Biomass Plant | 0.5 | 0 | 0 | 0 | 0 | 0 |
| Site Infrastructure | 1.0 | 0.3 | 0.3 | 0.3 | 0.3 | 0.3 |
| **TOTAL PHASE CAPEX** | **9.2** | **7.1** | **7.7** | **6.9** | **7.7** | **6.9** |
| **CUMULATIVE CAPEX** | **9.2** | **16.3** | **24.0** | **30.9** | **38.6** | **45.5** |

### Market Benchmarks (12-month trailing)

| Commodity | Avg | Low | High | Source |
|-----------|-----|-----|------|--------|
| WTI Crude ($/bbl) | 65.46 | 57.97 | 75.74 | FRED MCOILWTICO |
| ULSD Diesel GC ($/gal) | 2.2259 | 2.015 | 2.401 | FRED MDFUELUSGULF |
| Jet Fuel GC ($/gal) | 2.1177 | 1.928 | 2.347 | FRED MJFUELUSGULF |
| Propane MB ($/gal) | 0.7502 | 0.605 | 0.925 | FRED MPROPANEMBTX |

---

## 2. P&L CONSOLIDATED

### Revenue ($B)

| Line Item | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-----------|---------|---------|---------|---------|---------|---------|
| Power Sales | 0.22 | 0.53 | 0.80 | 1.04 | 1.32 | 1.53 |
| Fuel Sales | 0.86 | 1.55 | 2.18 | 2.78 | 3.37 | 3.92 |
| DC — Colocation | 0.15 | 0.30 | 0.35 | 0.45 | 0.55 | 0.65 |
| DC — AI/HPC | 0 | 0.40 | 0.85 | 1.00 | 1.25 | 1.45 |
| Oxygen Sales | 0.02 | 0.05 | 0.08 | 0.12 | 0.15 | 0.18 |
| Mineral Pellets | 0.01 | 0.01 | 0.02 | 0.03 | 0.04 | 0.05 |
| Software Licensing | 0 | 0.01 | 0.03 | 0.05 | 0.07 | 0.10 |
| **TOTAL REVENUE** | **1.25** | **2.85** | **4.31** | **5.48** | **6.75** | **7.88** |

### Direct Costs (COGS) ($B)

| Line Item | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-----------|---------|---------|---------|---------|---------|---------|
| Power COGS | 0.11 | 0.25 | 0.40 | 0.51 | 0.65 | 0.75 |
| Fuel COGS (direct) | 0.66 | 1.29 | 1.88 | 2.47 | 2.99 | 3.42 |
| DC COGS (incl. silicon amort.) | 0.06 | 0.12 | 0.18 | 0.22 | 0.25 | 0.29 |
| Other COGS | 0.01 | 0.02 | 0.03 | 0.04 | 0.05 | 0.06 |
| **TOTAL DIRECT COSTS** | **0.84** | **1.68** | **2.49** | **3.24** | **3.94** | **4.52** |

### Profitability ($B)

| Metric | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|--------|---------|---------|---------|---------|---------|---------|
| Contribution Margin | 0.41 | 1.17 | 1.82 | 2.24 | 2.81 | 3.36 |
| Contribution Margin % | 32.9% | 41.1% | 42.3% | 40.9% | 41.6% | 42.7% |
| Campus Overhead | 0.23 | 0.25 | 0.35 | 0.42 | 0.45 | 0.48 |
| **EBITDA** | **0.18** | **0.92** | **1.47** | **1.82** | **2.36** | **2.88** |
| EBITDA Margin % | 14.5% | 32.4% | 34.1% | 33.2% | 35.0% | 36.6% |
| Debt Service | 0.22 | 0.37 | 0.90 | 1.00 | 1.10 | 1.10 |
| **NET CASH FLOW** | **-0.04** | **0.55** | **0.57** | **0.82** | **1.26** | **1.78** |
| Net Cash Margin % | -3.0% | 19.4% | 13.3% | 15.0% | 18.7% | 22.6% |

### Key Ratios

| Ratio | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-------|---------|---------|---------|---------|---------|---------|
| DSCR (EBITDA / Debt Service) | 0.83x | 2.50x | 1.64x | 1.82x | 2.14x | 2.62x |
| Overhead as % of Revenue | 18.3% | 8.8% | 8.1% | 7.7% | 6.7% | 6.1% |
| Fuel Revenue as % of Total | 68.5% | 54.4% | 50.6% | 50.8% | 49.9% | 49.8% |
| DC Revenue as % of Total | 12.0% | 24.5% | 27.8% | 26.4% | 26.7% | 26.7% |

---

## 3. VOLUME DRIVERS

### Fuel Production

| Metric | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|--------|---------|---------|---------|---------|---------|---------|
| PFTs Online | 2 | 4 | 6 | 8 | 10 | 12 |
| BPD per PFT | 13,000 | 13,000 | 13,000 | 13,000 | 13,000 | 13,000 |
| Total BPD | 26,000 | 52,000 | 78,000 | 104,000 | 130,000 | 156,000 |
| Annual Barrels | 9.49M | 18.98M | 28.47M | 37.96M | 47.45M | 56.94M |
| Diesel (BPD) | 14,300 | 28,600 | 42,900 | 57,200 | 71,500 | 85,800 |
| Jet Fuel (BPD) | 6,500 | 13,000 | 19,500 | 26,000 | 32,500 | 39,000 |
| Propane/LPG (BPD) | 3,900 | 7,800 | 11,700 | 15,600 | 19,500 | 23,400 |

### Power Generation

| Metric | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|--------|---------|---------|---------|---------|---------|---------|
| Firm Generation (MW) | 2,607 | 5,213 | 7,820 | 10,427 | 13,033 | 15,640 |
| Internal Consumption (MW) | 2,060 | 3,870 | 5,880 | 7,890 | 9,900 | 12,010 |
| Net Export (MW avg) | 547 | 1,343 | 1,940 | 2,537 | 3,133 | 3,630 |
| Annual Export (GWh) | 4,789 | 11,768 | 16,994 | 22,221 | 27,448 | 31,799 |

### Data Centers

| Metric | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|--------|---------|---------|---------|---------|---------|---------|
| Colocation Buildings | 4 | 4 | 6 | 8 | 10 | 12 |
| AI/HPC Buildings | 0 | 4 | 6 | 8 | 10 | 12 |
| Total Buildings | 4 | 8 | 12 | 16 | 20 | 24 |
| Total DC Capacity (MW est.) | 240 | 480 | 720 | 960 | 1,200 | 1,440 |

### Campus Totals

| Metric | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|--------|---------|---------|---------|---------|---------|---------|
| Installed Generation (GW) | 8.51 | 11.02 | 13.54 | 16.05 | 18.56 | 21.07 |
| Firm Export (GW) | 0.55 | 1.34 | 1.94 | 2.54 | 3.13 | 3.63 |
| Total BPD | 26,000 | 52,000 | 78,000 | 104,000 | 130,000 | 156,000 |

---

## 4. CAPEX & RETURNS

### Capital Expenditure ($B)

| Component | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|-----------|---------|---------|---------|---------|---------|---------|
| Nuclear (AP1000 x PFTs) | 4.0 | 4.0 | 4.0 | 4.0 | 4.0 | 4.0 |
| FT Synthesis Plant | 1.5 | 1.5 | 1.5 | 1.5 | 1.5 | 1.5 |
| Data Centers | 0.4 | 0.8 | 0.6 | 0.6 | 0.6 | 0.6 |
| Solar Array | 1.0 | 0 | 0.8 | 0 | 0.8 | 0 |
| Balance of Plant | 0.8 | 0.5 | 0.5 | 0.5 | 0.5 | 0.5 |
| Biomass Plant | 0.5 | 0 | 0 | 0 | 0 | 0 |
| Site Infrastructure | 1.0 | 0.3 | 0.3 | 0.3 | 0.3 | 0.3 |
| **TOTAL PHASE CAPEX** | **9.2** | **7.1** | **7.7** | **6.9** | **7.7** | **6.9** |
| **Cumulative CapEx** | **9.2** | **16.3** | **24.0** | **30.9** | **38.6** | **45.5** |

### Investment Returns

| Metric | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|--------|---------|---------|---------|---------|---------|---------|
| EBITDA ($B) | 0.18 | 0.92 | 1.47 | 1.82 | 2.36 | 2.88 |
| Net Cash Flow ($B) | -0.04 | 0.55 | 0.57 | 0.82 | 1.26 | 1.78 |
| DSCR | 0.83x | 2.50x | 1.64x | 1.82x | 2.14x | 2.62x |
| EBITDA / Phase CapEx | 2.0% | 13.0% | 19.1% | 26.4% | 30.6% | 41.8% |
| Net Cash / Cumulative CapEx | -0.4% | 3.4% | 2.4% | 2.7% | 3.3% | 3.9% |
| Simple Payback (years) | N/A | 29.4 | 42.0 | 37.7 | 30.7 | 25.5 |

---

## 5. FUELS ECONOMICS

### Production Cost vs Delivered Price

| Metric | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|--------|---------|---------|---------|---------|---------|---------|
| Production Cost ($/bbl) | 70 | 68 | 66 | 65 | 63 | 60 |
| Diesel Delivered ($/gal) | 2.55 | 2.30 | 2.15 | 2.05 | 1.98 | 1.92 |
| Jet Delivered ($/gal) | 2.50 | 2.25 | 2.10 | 2.02 | 1.96 | 1.90 |
| Propane Delivered ($/gal) | 0.85 | 0.80 | 0.78 | 0.76 | 0.74 | 0.73 |

### Market Benchmarks (Static)

| Commodity | Price |
|-----------|-------|
| ULSD Diesel ($/gal) | 2.2259 |
| Jet Fuel ($/gal) | 2.1177 |
| Propane ($/gal) | 0.7502 |
| WTI Crude ($/bbl) | 65.46 |

### Atlas vs Market Differential ($/gal or $/bbl)

| Metric | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|--------|---------|---------|---------|---------|---------|---------|
| Diesel vs Market | +0.32 | +0.07 | -0.08 | -0.18 | -0.25 | -0.31 |
| Jet vs Market | +0.38 | +0.13 | -0.02 | -0.10 | -0.16 | -0.22 |
| Propane vs Market | +0.10 | +0.05 | +0.03 | +0.01 | -0.01 | -0.02 |
| Production vs WTI ($/bbl) | +4.54 | +2.54 | +0.54 | -0.46 | -2.46 | -5.46 |

Positive = Atlas more expensive than market. Negative = Atlas cheaper than market.

---

## 6. DC ECONOMICS

Doctrine: P1 = 4 colo; P2 = +4 AI; P3-6 = +2 colo +2 AI each.

| Metric | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|--------|---------|---------|---------|---------|---------|---------|
| Colo Buildings | 4 | 4 | 6 | 8 | 10 | 12 |
| AI/HPC Buildings | 0 | 4 | 6 | 8 | 10 | 12 |
| Colo Revenue ($B) | 0.15 | 0.30 | 0.35 | 0.45 | 0.55 | 0.65 |
| AI Revenue ($B) | 0 | 0.40 | 0.85 | 1.00 | 1.25 | 1.45 |
| Total DC Revenue ($B) | 0.15 | 0.70 | 1.20 | 1.45 | 1.80 | 2.10 |
| DC COGS ($B) | 0.06 | 0.12 | 0.18 | 0.22 | 0.25 | 0.29 |
| DC Gross Margin ($B) | 0.09 | 0.58 | 1.02 | 1.23 | 1.55 | 1.81 |
| Margin % | 60% | 83% | 85% | 85% | 86% | 86% |

### Phase 6 Full Revenue Mix ($B)

| Segment | Revenue |
|---------|---------|
| Power | 1.53 |
| Fuels | 3.92 |
| DC Colo | 0.65 |
| DC AI/HPC | 1.45 |
| Other | 0.33 |
| **Total** | **7.88** |

---

## 7. SENSITIVITY

Phase 6 Full Build — Impact of key variable changes on EBITDA and Net Cash Flow.

| Scenario | Base Case | Downside | Upside |
|----------|-----------|----------|--------|
| WTI Crude ($/bbl) | 65.46 | 50 | 85 |
| Diesel Market ($/gal) | 2.23 | 1.80 | 2.80 |
| Fuel Production Cost ($/bbl) | 60 | 70 | 55 |
| DC AI Revenue per Bldg ($M) | 121 | 90 | 160 |
| Power Export Price ($/MWh) | 52 | 40 | 65 |
| Campus Overhead ($B) | 0.48 | 0.60 | 0.40 |

Note: Static scenario table. For dynamic sensitivity, adjust values on ASSUMPTIONS sheet in the Excel source.

---

## 8. SOURCES

| Data Point | Source |
|------------|--------|
| WTI Monthly | https://fred.stlouisfed.org/series/MCOILWTICO |
| ULSD Monthly | https://fred.stlouisfed.org/series/MDFUELUSGULF |
| Jet Fuel Monthly | https://fred.stlouisfed.org/series/MJFUELUSGULF |
| Propane Monthly | https://fred.stlouisfed.org/series/MPROPANEMBTX |
| EIA Spot Price Definitions | https://www.eia.gov/dnav/pet/TblDefs/pet_pri_spt_tbldef2.asp |
| AP1000 Unit Cost | Bible Rev 4.1.1 Vol II — ~$2B/unit (2 per phase = $4B) |
| Generation Capacity | Bible Rev 4.1.1 Vol II — 21 GW installed, 16 GW firm |
| BPD Target | Bible Rev 4.1.1 Vol V — 100,000 BPD full build (12 PFT x ~9,000) |
| DC Doctrine | Bible Rev 4.1.1 Vol III — 16 buildings Phase 1, scaling to 24 |
| Constraint Hierarchy | Bible Rev 4.1.1 Vol VII — Pipe > Loop B > Biomass > O2 > DAC > SOEC |
