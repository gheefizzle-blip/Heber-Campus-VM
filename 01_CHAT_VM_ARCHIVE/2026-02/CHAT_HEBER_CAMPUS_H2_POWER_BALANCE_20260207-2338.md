# CHAT_HEBER_CAMPUS_H2_POWER_BALANCE_20260207-2338

**Snapshot Timestamp:** 2026-02-07 23:38 UTC  
**Source:** ChatGPT Extraction (HCV-VM-EXTRACT-002)  
**Thread:** HEBER_CAMPUS_H2_POWER_BALANCE  
**VM_VERSION:** 20260207-2338  
**Immutable:** Yes

---

## Heber Campus H2 Power Balance & Storage Architecture

### PV Generation & Temporal Dynamics
- **Daylight Deliverable Target:** 1.5 GW via photovoltaic generation
- **Installed PV Capacity:** Approximately 8,000 acres of photovoltaic cells
- **Power Profile Characteristic:** Non-binary ramp (morning ramp-up → peak midday → evening ramp-down)
- **Modeling Requirement:** Dynamic (hourly) power production profile, not on/off binary assumption

### Seasonal Load Variation
- **Winter-Summer Daylight Variation:** Operating hours variable by season
  - Winter: Shorter daylight window, lower afternoon peak
  - Summer: Longer daylight window, higher afternoon peak
- **Non-Solar Production Hours:** Variable by time of year
- **Regional Load Shape:** Requires real-world Arizona regional demand data, not fixed percentage assumptions

### Storage Buffer Sizing
- **Low-Solar Buffer Duration:** Approximately 10 consecutive days of low-solar production
- **Purpose:** Bridge seasonal low-generation periods (winter, cloudy weeks, etc.)
- **Technology Assumption:** Multi-day stored energy (electrochemical + hydrogen tank)

### Overnight Firm Generation Baseline
- **Four SMR Units (NuScale/Pebble Bed Class):** 80 MW electric each = 320 MW subtotal
  - Mode selector: Electric output (80 MW) OR thermal output (~200 MW per unit)
- **Biomass Plant:** ~100 MW electric + continuous steam production
- **Combined Overnight Firm Baseline:** 420 MW electric generation when all units dispatched in electric mode
- **Dispatch Flexibility:** SMRs can split thermal/electric output to balance electricity + hydrogen production steam feeds

### Demand Asymmetry
- **Daytime Demand:** Higher (VVLS operations, manufacturing, data center cooling, hydrogen production)
- **Overnight Demand:** Lower than daytime
- **Deliverable Overnight Requirement:** Based on actual Arizona regional load profiles, not assumed percentages

### Hydrogen Production & Dispatch

#### Daytime Hydrogen Production
- **Primary Input:** PV electrical output (1.5 GW target during daylight)
- **Technology:** Solid Oxide Electrolysis Cells (SOEC)
- **Operational Mode:** Electrical H₂ production using grid-tied PV power

#### Overnight/Low-Solar Hydrogen Production
- **Secondary Dispatch:** Limited SMR electric output to power SOEC stacks at night
- **Benefit:** Reduces overnight battery storage drawdown by partially producing H₂ on-demand
- **Thermal Support:** Biomass plant steam + SMR thermal dispatch can support SOEC inlet steam conditioning

### Hydrogen End-Uses

#### Energy Storage & Power Generation
- **Storage Duration:** Overnight + multi-day low-solar bridging (via compressed H₂ tanks + fuel cell back-conversion)
- **Fuel Cell Dispatch:** Convert H₂ → electricity during non-solar hours
- **Gas Turbine Dispatch:** Use H₂ as fuel turbine input for peak load support

#### Petrochemical Operations & Synthetic Fuels
- **Carbon Feedstock Source:** Biogenic CO₂ captured from biomass plant
- **Syngas/Fischer-Tropsch Pathway:** H₂ + CO₂ → synthetic fuels (propane, diesel, kerosene, etc.)
- **Dual-Purpose System:** H₂ serves both energy storage AND chemical synthesis feedstock

### Integration Architecture
- **Biomass 24/7 Operation:** Constant electricity + steam production (no shutdown cycling)
- **SMR Thermal Flexibility:** Each unit dispatchable between 80 MW electric or ~200 MW thermal (or mixed modes)
- **SOEC Steam Conditioning:** Biomass steam + trim-heater (SMR or biogas combustion) = stable inlet to electrolyzer stacks
- **Hydrogen Tank Farm:** Multi-megawatt-hour capacity (location TBD, likely onsite thermal storage + underground cavern/pressure vessels)
- **Fuel Cell/Turbine Integration:** Discharge H₂ during non-solar to meet peak demand + low-solar buffer needs
