# CHAT_HeberCampus_SOEC_DC_20260207-2330

**Snapshot Timestamp:** 2026-02-07 23:30 UTC  
**Source:** ChatGPT Extraction (HCV-VM-EXTRACT-002)  
**Thread:** HeberCampus_SOEC_DC  
**VM_VERSION:** 20260207-2330  
**Immutable:** Yes

---

## Heber Campus DC Power Architecture & SOEC Integration

### Hydrogen Demand Baseline
- **Planning Baseline:** 457 t/day (457,000 kg/day)
- **Status:** Interim planning figure until replaced by detailed Process Flow Diagram (PFD) mass balance
- **Revalidation Required:** Final demand will be calculated from detailed PFD including VVLS operations, synthetic fuel production, fuel cell round-trip losses, and contingency reserves

### Solar Generation DC Profile
- **Photovoltaic Output:** 1.5 GW in DC form (not AC inverted)
- **Delivery Format:** Direct DC to campus distribution bus
- **Constraint:** Non-dispatchable (weather-dependent) source; requires buffering for load matching

### Grid Interconnection - MVAC Substation
- **Connection Type:** Medium-voltage AC (MVAC) transmission line tie-in to regional grid
- **Functions:**
  - Export surplus renewable power during high-generation hours
  - Import grid power during overnight/low-solar periods if battery depleted
  - Revenue opportunity: Sell peak solar generation to grid, reduce campus power costs
- **Integration:** Separate from internal DC distribution; utility-scale interconnection point

### Data Center DC Bus Architecture
- **Power Delivery Format:** Direct DC voltage (nominal TBD; likely 400-600 VDC for large-scale IT loads)
- **Efficiency Advantage:** Eliminates AC->DC conversion stage in data center PSUs; IT loads are inherently DC
- **Load Profile:** Assumed 24/7 continuous operation; variable cooling demand with seasonal thermal variation
- **Integration Point:** Campus main DC bus for low-loss internal power distribution

### SOEC Plant Electrical Delivery - DC Preferred
- **Primary Constraint:** Reduction of conversion losses in power chain: PV DC → (AC inversion + AC transmission + DC rectification in SOEC) vs. direct DC path
- **Conversion Loss Comparison:**
  - DC->AC->DC path: ~6-10% round-trip loss (inverter 2-3% + transmission 1-2% + rectifier 3-4%)
  - Direct DC path: ~1-2% loss (local distribution resistance only)
- **Status:** "If feasible" indicates technical assessment pending on:
  - SOEC electrolyzer rectifier design (can it accept DC input directly?)
  - DC bus voltage/current capability vs. SOEC input requirements
  - Safety/isolation requirements for DC distribution
- **Mechanical Benefit:** Reduced waste heat in power conversion = lower trim-heater steam load

### Utility-Scale Battery System for DC Bus Stabilization
- **Primary Function:** Smooth and stabilize DC bus voltage/frequency for large DC loads
- **Sizing Basis:** Multi-hour capacity (TBD) to support:
  - Morning ramp-down from PV startup (load ramp matching)
  - Evening load-carry until night generation sources (SMR/biomass) fully dispatch
  - Transient support for SOEC electrolyzer startup/shutdown events (DC loads have steep current ramps)
- **Technology Options:**
  - Lithium-ion battery (high power capability, temperature sensitive)
  - Flow battery (longer discharge duration, lower power density)
  - Hybrid architecture (Li-ion for fast response + flow for duration)
- **DC Voltage Regulation:** Battery acts as local voltage source to stabilize DC bus against load step changes

### Campus Dual-Bus Power Architecture
- **MVAC Bus (Utility Interface):**
  - Grid tie-in point for import/export
  - AC generation sources if deployed future (wind, etc.)
  - Substation equipment (transformers, switchgear, protection relays)
  - Backup generator (if adopted)

- **Internal DC Bus (Campus Distribution):**
  - PV DC feed from solar array (1.5 GW)
  - Battery system (smoothing/stabilization)
  - Data center loads
  - SOEC electrolyzer loads (if DC delivery validated)
  - DC-DC converters for lower-voltage systems (HVDC->LVDC for controls, sensors, etc.)
  - Potential future DC loads (advanced manufacturing, EV charging, etc.)

### Integration Logic
- **Morning Ramp-Up:** Solar generation rises → battery discharges to level load \ → grid exports surplus above load + storage
- **Midday Peak:** Full solar output + battery available → supply data centers + SOEC at full rate → export excess to grid
- **Afternoon Ramp-Down:** Solar generation falls → battery charges from PV surplus → grid imports if battery depleting
- **Evening Transition:** Solar drops below load → SMR + biomass dispatch to AC grid (via MVAC substation) → AC->DC conversion for campus loads OR SMR thermal used to dispatch hydrogen production (SOEC steam feed)
- **Overnight:** Battery reserves depleted → firm generation (SMR + biomass) supplies all loads; excess thermal routed to SOEC for hydrogen production
