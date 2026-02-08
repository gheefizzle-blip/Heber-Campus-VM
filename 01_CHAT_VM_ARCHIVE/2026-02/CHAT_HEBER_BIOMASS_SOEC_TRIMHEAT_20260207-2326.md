# CHAT_HEBER_BIOMASS_SOEC_TRIMHEAT_20260207-2326

**Snapshot Timestamp:** 2026-02-07 23:26 UTC  
**Source:** ChatGPT Extraction (HCV-VM-EXTRACT-002)  
**Thread:** HEBER_BIOMASS_SOEC_TRIMHEAT  
**VM_VERSION:** 20260207-2326  
**Immutable:** Yes

---

## Heber Campus Biomass Integration - SOEC Trim-Heat Architecture

### Biomass Plant Role
- **Integration Concept:** Biomass plant added to campus
- **Primary Function:** Capture of biogenic CO₂ for use as carbon feedstock in downstream chemical manufacturing

### SOEC Steam Conditioning Architecture
- **Multi-Stage Design:** Biomass/HRSG (Heat Recovery Steam Generator) provides mid-grade steam
- **Trim-Heater Stage:** Dedicated trim-heater provides final temperature lift to SOEC hot-box inlet temperature requirement
- **Fuel Source:** Trim heaters use SOEC byproduct O₂ as oxidizer paired with combustible streams

### Trim-Heater Fuel Eligibility
- **Eligible Combustibles:** Petrochemical/byproduct streams without market value:
  - Syngas
  - Off-gases
  - Purge gases
  - Light ends
  - Internal byproducts (stranded material)
- **Cost Advantage:** Repurposing waste/byproduct streams reduces need for external fuel purchases

### SOEC Contamination Control
- **Isolation Rule:** Combustion products from trim heating shall NOT be introduced into SOEC process gas path unless explicitly vendor-approved
- **Default Architecture:** Indirect-fired heat transfer (combustion separated from process gas)
- **Rationale:** Protect SOEC from sulfur compounds, nitrogen oxides, particulates that degrade electrolyzer performance

### SOEC Hot-Box Thermal Protection
- **Gradient Control:** Ramp-up and ramp-down must be slow with enforced gradient limits
- **Purpose:** Avoid thermal shock and consequent stack damage
- **Implementation:** Automatic control with ramping constraints on heater command signals

### Trim-Heater Instrumentation & Control
- **Fuel System Monitoring:** Continuous fuel composition/quality measurement OR LHV (Lower Heating Value) surrogate
- **Flow Monitoring:** Fuel flow and O₂ flow rate measurement
- **Purity Monitoring:** O₂ purity verification
- **Flame Monitoring:** Flame presence detection (safety)
- **Temperature Monitoring:** Steam temperature at key process points
- **Dual Control Objective:** Maintain steam outlet temperature within SOEC band AND combustion stoichiometry safety

### Deployment Phasing
- **Primary Thermal Source:** SMR reactors remain planned high-grade heat source
- **Regulatory Risk:** SMR approvals may delay deployment by years (licensing, permitting, environmental review)
- **Biomass Advantage:** Enables smaller-scale H₂ production earlier, prior to SMR availability
- **Scaling Option:** Biomass baseline can be sized for interim operation, then complemented by SMR later

### Regional Reference Plant
- **Facility:** Novo BioPower (Snowflake, AZ)
- **Capacity:** ~24-28 MW electric class
- **Current Status:** Power-only operation (no SOEC or electrolysis integration documented)
- **Distance:** Nearby reference for biomass resource availability and supply chain logistics in region
