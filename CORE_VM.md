# CORE_VM.md

**Last Updated:** 2025-12-27 23:55  
**VM_VERSION:** 20251227-2355  
**Status:** Delta applied - Baseline Product Slate & Regional Integration Strategy

## Core Virtual Memory

Authoritative canonical VM state. Updated only via delta application.

---

## Heber Campus VVLS Project - Initial Decisions (2026-02-07)

### Logistics & Payload Strategy
- High-cadence mass-to-LEO supply required primarily for raw building materials (steel, aluminum, tools, assembly parts), not sensitive payloads
- Raw cargo can tolerate up to ~100 g; rocket guidance/propulsion hardware is the limiting component

### Launch Architecture
- Stratospheric sky-ramp rejected as impractical
- **Vertical Vacuum Launch Shaft (VVLS)** selected as feasible path
- Vehicle exits vertically and must ignite immediately after tube exit to prevent fall-back
- Tug rendezvous used after orbital insertion/intercept
- Bolt-on solid rocket motors preferred for simplicity and reliability (fewer failure points)

### Mag-Lift Performance Targets
- Initial target exit velocity: 500 m/s
- Revised target: 700 m/s (with high-g-tolerant solid motor approach)

### Facility Concept
- 500 m concrete/steel launch tower with 4 vertical mag-lift shafts
- Service elevator/stair access
- Sabot/sled concept incorporated

### Campus Integration
- On-site power generation adjacent to launch complex
- Staged energy storage with recharge between launches (capacitor/supercap-only approach deprioritized)
- Hydrogen production at scale
- Solar farm
- Data center/SDC test center
- Manufacturing facilities as unified ecosystem
- Ground comms node for space resilience (reduce reliance on commercial LEO constellations)

### Grid & Revenue Strategy
- Excess campus power export to grid as revenue stream
- Regional coal retirements referenced as market pull for new firm capacity

### Site Options
**Island Siting:** Hawaii or Guam (remoteness, over-ocean safety corridors)

**Inland Siting:** Overgaard, AZ
- ~6,000 ft elevation
- Sparse population, available land
- Rail/highway access
- Labor availability
- Elevation reduces muzzle dynamic pressure proportionally to air density
- Overlie the Coconino aquifer (groundwater-assisted cooling identified as design consideration)

### Campus Land Planning
- Core developed area: ~3,400 acres
- Total acquisition target: ~8,000–12,000 acres (buffers + expansion)

### Private Airport
- On-site included
- High-elevation runway length target: ~9,000–9,500 ft with safety areas

### Staff Housing
- On-site apartment complex required
- **Phase A:** 120 units (40 studios, 60 one-bed, 20 two-bed)
- Phase A footprint: ~7 acres developed + ~7 acres reserved for Phase B
- Expansion potential to ~300 units
- Parking: ~1.3 stalls/unit with EV and accessible allocation

---

## Heber Autonomous Industrial Campus - Master Design (2026-02-07)

### Site Definition
- **Location:** North of Heber/Overgaard, Arizona
- **Size:** 1,200 acres total
- **Coordinate Grid:** SW-origin, 500 ft major / 100 ft minor intervals
- **Master Plan:** ARCH E format (36x48), base scale 1" = 400'; insets at 1" = 200' for dense zones

### Power System
- **Target:** 220 MW net, modular phased integration
- **Solar:** 40 MW farm (single-axis planning basis)
- **Battery Storage:** 500 MWh BESS for peak load support, ramping, black-start
- **SMR Integration:** 3x NuScale modules at 77 MW each (longest-lead regulatory item)

### Energy Production & Storage
- **SOEC Block:** Produces H₂ and O₂ from electricity
- **Ammonia Conversion:** H₂ converted to NH₃ for bulk storage and dispatchable energy
- **Tank Farm:** Bulkheads and loading for O₂ and NH₃ to truck tankers and railcars
- **Gas Turbines:** NH₃ and O₂ mix (oxy-combustion)

### Cooling Architecture
- **Ammonia Role:** Integrated campus cooling agent for climate control and data center cooling
- **Distribution:** Central NH₃ plants with secondary glycol/brine loops (NH₃ excluded from occupied IT halls)
- **Waste-Heat Recovery:** Absorption chilling (NH₃/H₂O) integrated into thermal plan
- **Thermal Storage:** Chilled-water system provides 6-10 hours N+1 data hall cooling resilience

### Water & Environmental
- **Primary Supply:** Coconino aquifer (subject to permitting and safeguards)
- **Wind Constraint:** Provisional prevailing wind direction SW to NE (pending met-mast confirmation)

### Data Center & Control
- **MECSAI System:** Terrestrial data center as backbone for campus master control and orchestration
- **Architecture:** Modular cell-level control with feedback to master control layer
- **Safety Interlocks:** Hard PLC-based, non-bypassable by MECSAI

### Manufacturing
- **Autonomous Houses:** Multiple models (on-site production)
- **Space Assets:** Space tugs, SDCs, communications modules (includes clean room environments)

### Launch Infrastructure
- **Vertical Mag-Lift Building:** 500 m height with dedicated safety zone
- **Launch Tower Zoning:** Exclusion radius 1,800 ft, placed far NW portion of site
- **Requirement:** Isolated as far from other infrastructure as practical

### Transportation & Access
- **Rail:** BNSF spur connection with campus rail yard for bulk product loading
- **Truck Access:** Dedicated tanker roads with scale house (tare/loaded measurement)
- **Airport:** Full taxiway, primary runway, crosswind runway (9,000 ft basis), plus helipad
- **Communications:** Fiber trunk backhaul via regional backbone; ground-based comms station for satellite redundancy

### Security
- **Perimeter:** 8 ft fencing with razor wire tops
- **Access:** Guarded entry with guard shack, camera system

### Residential & Support
- **Housing Complex:** 600-resident capacity
- **Amenities:** Rec center (weights/cardio/basketball), general store, pharmacy, casual dining
- **Units:** Mixed types (studio, 1BR, 2BR)

### Campus Design Philosophy
- **Modularity:** Flexible interconnections for power, water, communications via standardized corridors and nodes

---

## Magnetic Rail Gun Launch System - SDC-COMMS Projectile Architecture (2026-02-07)

### Orbital Targeting
- **Altitude Baseline:** 350-400 km LEO (canonical correction; 1,000 km targeting concepts retired)
- **Program:** Magnetic Rail Gun Launch System, Spear Enterprise global architecture

### Projectile Specifications
- **Mass:** 1,000 kg pod
- **Rail Exit Velocity:** ~1,500 m/s
- **Insertion Method:** SRB-assisted

### SRB Delta-V Profile
- **Total Delta-V Required:** 1.8-2.2 km/s for 350-400 km insertion
- **Burn Duration:** 300-400 s

### Reviews & Coordination
- **ATB Routing Packet:** ATB-ROUTE-MAGLIFT-POD-013 (corrected canonical review artifact)
- **Submitting Division:** SDC-COMMS (Mag-Lift projectile architecture and ATB coordination)
- **Integration Status:** Formally integrated into Spear Enterprise architecture

---

## Heber Campus Master Planning - AO v0.4 Progression (2026-02-07)

### Planning Baseline
- **Version:** AO v0.4 (canonical planning inputs)
- **Status:** Fixed block coordinates, safety setbacks, wind-aligned zoning established
- **Interconnection Doctrine:** Modular ICD-00 doctrine formalized

### Authoritative Reference
- **Spatial Authority:** AO v0.4 designated as authoritative reference for all downstream CAD drafting
- **Constraint:** MECHWORK must produce scaled A0 master site plans derived directly from AO coordinates without approximation

### Documentation Standards
- **Intermediate Artifacts:** Vector-mapped, near-scale visual representations approved for planning
- **Engineering Requirement:** CAD outputs (DWG/PDF) mandatory for any document entering engineering or ATB review
- **Format:** ARCH E (36x48), base scale 1" = 400'; insets at 1" = 200'

### Phase Transition
- **Execution Authority:** Granted to advance AO v0.4 into formal MECHWORK CAD drafting
- **Transition:** Concept phase → Engineering-grade site documentation phase
- **Responsible Division:** MECHWORK

---

## Media Handling Guidelines - HCV-VM-EXTRACT-002 (2026-02-07)

### Facebook Share Links
- **Authentication Requirement:** Share links may still require login after generation
- **Handling Rule:** If video cannot be accessed without authentication, must be provided as direct uploaded media file (MP4/MOV format)
- **Purpose:** Enables transcription/analysis without authentication barriers

### iOS/Facebook Workflow Artifacts
- **Binary Property List (bplist) Artifact:** Apple binary format with file header "bplist00"
- **Content:** Contains metadata/pointers only, not playable video
- **Classification:** Non-media artifact
- **Action:** Request actual video file instead; do not attempt playback or analysis of bplist artifacts

---

## OSYE Orbital Logistics - Orbital Mechanics & Operations (2026-02-07)

### Orbital Mechanics Baseline
- **GEO Altitude:** ~35,786 km (only achievable geosynchronous orbit)
- **GEO Orbital Speed:** ~3.07 km/s
- **LEO (~400 km) Orbital Speed:** ~7.7 km/s
- **Ground-Fixed at 400 km:** Requires continuous thrust; tangential speed only ~0.49 km/s; not a gravity-free condition

### Hover/Hover-Fix Feasibility
- **Power Requirement:** Large masses (100+ ton) at LEO altitudes require continuous thrust to maintain ground-fixed position
- **Conclusion:** Infeasible under tens-of-megawatts-class NEP; orbital (elliptical/circular) dynamics required for all tug operations

### Heber Campus Launch Altitude Profile
- **Campus Elevation:** ~6,500 ft (~2,000 m) ASL
- **Launch Tower Height:** 500 m
- **Tube Exit Altitude:** ~2,500 m (~8,100 ft) ASL
- **SRM Ignition Criterion:** 10 km traveled after exit → ~12.5 km ASL for vertical ascent

### Vertical Ballistic Ascent Performance
- **Exit Velocity 2.5 km/s (no SRM):** ~318 km altitude gain (~320 km apogee, ignoring drag)
- **LEO Speed Allocated Vertically:** ~7.7 km/s → ~3,000 km apogee (ignoring losses)
- **10,000 km Apogee Requirement:** Would need ~14 km/s vertical cutoff speed (not practically achievable)

### SRM Sizing Baseline
- **Configuration:** 1.0 m diameter, 10 m length, propellant density ~1,700 kg/m³, casing 10% propellant mass
- **Propellant Mass:** ~13.3 t
- **Isp:** ~270 s
- **Delta-V (1 t pod + casing):** ~5.0 km/s
- **Combined System:** 2.5 km/s mag-lift + 5.0 km/s SRM supports low-thousands-km vertical apogee (~2,000–3,000 km with losses)

### SRM Scaling Effect
- **20 m Length (vs 10 m):** 2x propellant mass, but delta-v only ~5.6 km/s (logarithmic mass-ratio constraint)
- **Apogee Class:** Remains in low-thousands-km range; 10,000 km not achievable via scaling alone

### OSY-E Tug Rendezvous Doctrine
- **Tug Base Location:** OSY-E in GEO
- **Transfer Method:** GEO-to-LEO transfer ellipse (not vertical hovering)
- **Collection Zone:** Near perigee with matrix jig for pod collection
- **Return:** Tugs return to OSY-E via elliptical transfer
- **Requirement:** Rendezvous achieved by orbital state matching (low relative velocity)

### OSY-E Propellant Sustainability
- **Source:** Chemical propellant produced at OSY-E from delivered water
- **Constraint:** Chemical propellant mass consumed per cycle ≤ 0.50 of payload mass (0.25 preferred long-term)
- **Cost Driver:** Lower ratio = lower cost/kg over decade timescales

### Hybrid Tug Split Model
- **Reference Delta-V:** GEO-LEO-GEO transfer ~3.0 km/s
- **Ratio 0.50:1 (chem:payload):** Chemical ~1.4 km/s, NEP ~1.6 km/s
- **Ratio 0.25:1 (chem:payload):** Chemical ~0.76 km/s, NEP ~2.24 km/s
- **Trade:** Lower chemical fraction increases cycle time and tug count for fixed cadence

### Heber Launch Tower Operational Cadence
- **Nominal Rate:** 1 pod per 2.5 minutes
- **Duty Cycle:** 75% (maintenance/inspection allowance)
- **Daily Launches:** ~400–450 pods/day

### OSY-E Phased Construction Doctrine
- **Phases 1–4:** NEP-only logistics (dry materials, no water processing)
- **Water-Ready Transition:** After water storage/processing commissioned, cargo shifts majority-water for on-orbit reserves
- **Fuel Production:** Enables on-orbit propellant synthesis

### Post-Water Hydrogen Carrier Option
- **Ammonia (NH₃) as H₂ Carrier:** H mass fraction ~17.6% (vs water ~11.1%)
- **Cracking Method:** On-orbit reactor waste heat decomposes NH₃ → H₂ + N₂
- **Downstream Use:** H₂ fed to fuel synthesis (e.g., methane) after reserves/processing established

---

## Heber Campus Nuclear Pivot - HTGR Baseline Adoption (2026-02-07)

### Reactor Selection
- **Baseline Pivot:** NuScale LWR SMR → Pebble-bed HTGR (Xe-100 class)
- **Rationale:** Align terrestrial operations with OSY-E reactor doctrine; maximize Earth-to-orbit operational learning transfer
- **Master Plan Impact:** Requires revision for nuclear island, thermal integration, controls, licensing/fuel-supply risk posture

### OSY-E Power Conversion
- **Baseline Preference:** Closed Brayton-class conversion
- **De-prioritized:** Rankine steam/two-phase in microgravity (high-complexity, high-risk)

### OSY-E Pebble-Bed Fuel Handling
- **Gating Issue:** Gravity-driven pebble circulation assumptions invalid in microgravity
- **Baseline Recommendation:** Option B/C selected
  - Static pebble campaign core with batch refuel, OR
  - Prismatic TRISO HTGR with helium primary retained
- **Conditional Upgrade:** Spin-gravity moving-pebble module is upgrade path only
- **Not Baselined:** Mechanical pebble recirculation in microgravity (reliability risk)

### OSY-E Spent Fuel Handling
- **Baseline:** Shielded cask storage in dedicated "nuclear yard" zone
- **Asset Class:** Spent fuel treated as shielding/ballast asset
- **Not Baselined:** Deep-space/Jupiter disposal

### HTGR Heat Integration
- **Prohibition Rule:** Do NOT swap coolant between water and ammonia
- **Primary Circuit:** Helium retained
- **Secondary Architecture:** Helium → Intermediate Heat Exchanger (IHX) → dedicated secondary loops
  - Steam/SOEC steam train
  - NH₃ feed preheat to cracker
- **Isolation:** Multi-barrier isolation with leak detection required

### Night Operations & Fuel Cell Integration
- **Anode Purge Routing:** Residual H₂ from fuel cell anode purge may route to dedicated catalytic oxidizer/burner
- **Heat Recovery:** Burner output feeds turbine hot-standby
- **Constraint:** NOT primary turbine fuel (variability, limited flow)

### Turbine Safety Rules (Locked)
- **Mixing Prohibition:** Do NOT mix H₂ and O₂ in piping
- **Controlled Combustion:** Mixing only at controlled combustor/burner with burner management and interlocks
- **Pure H₂/O₂ Firing:** Requires dilution (steam injection or exhaust recycle) to protect turbine materials

### ATB Submission Artifacts
- **HC-EN-NUC-PIVOT-DEC-001 Rev A** (decision document)
- **HC-EN-NUC-PIVOT-ADD-A-001 Rev A** (addendum A)
- **HC-EN-NUC-PIVOT-ADD-B-001 Rev A** (addendum B)

---

## Hydrogen System Design - Vendor Specification Research (2026-02-07)

### Design Philosophy
- **Approach:** Deep vendor-spec research to obtain precise device input requirements
- **Compliance:** Design hydrogen system to comply with formalized vendor requirements
- **Methodology:** Reverse-engineer system design from manufacturer specifications rather than apply generic assumptions

---

## Heber Campus Biomass Integration - SOEC Trim-Heat Architecture (2026-02-07)

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

---

## Heber Campus H2 Power Balance & Storage Architecture (2026-02-07)

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

---

## Heber Campus DC Power Architecture & SOEC Integration (2026-02-07)

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
- **Morning Ramp-Up:** Solar generation rises → battery discharges to level load → grid exports surplus above load + storage
- **Midday Peak:** Full solar output + battery available → supply data centers + SOEC at full rate → export excess to grid
- **Afternoon Ramp-Down:** Solar generation falls → battery charges from PV surplus → grid imports if battery depleting
- **Evening Transition:** Solar drops below load → SMR + biomass dispatch to AC grid (via MVAC substation) → AC->DC conversion for campus loads OR SMR thermal used to dispatch hydrogen production (SOEC steam feed)
- **Overnight:** Battery reserves depleted → firm generation (SMR + biomass) supplies all loads; excess thermal routed to SOEC for hydrogen production

---

## Heber Campus Phase 1/Phase 2 Expansion Planning & Governance Framework (2026-02-07)

### Phase 2 Expansion Capacity Target
- **Ultimate Solar Capacity:** Approximately 5 GW (Phase 1 + Phase 2 combined)
- **Phase 1 Planning Assumption:** Interim baseline (1.5 GW documented in prior deltas)
- **Phase 2 Growth:** Approximately 3.5 GW additional solar capacity
- **Data Center Expansion:** Beyond Phase 1 baseline (current footprint unspecified but reserved)
- **Constraint:** Phase 1 design must NOT require rework to accommodate Phase 2

### Export Substation Location & MVAC Infrastructure
- **Fixed Location:** Northwest quadrant of Heber Campus
- **Siting Rationale:** Shortest MVAC transmission line tie-in distance to regional transmission corridors
- **Cost Driver:** Grid interconnection distance minimizes tie-in cost — fixed endpoint constrains site
- **Phase 2 Planning:** Full Phase 2 footprint must be reserved in Phase 1 (no relocation possible)
- **Network Topology:** MVAC substation serves as central hub for grid export/import; location is non-negotiable

### Solar Field Primary Siting Strategy
- **Phase 1 Primary Location:** Northwest quadrant
- **Expansion Approach:** Geographic sweep corridors reserved for modular duplication at Phase 2
- **Modular Duplication Doctrine:** Solar arrays deploy in standardized footprint modules; Phase 2 expands along sweep corridors without redesigning Phase 1
- **Orientation Constraints:** Azimuth/tilt optimized for Arizona latitude; sweep corridors aligned to this orientation for consistency
- **Land Utilization:** Assumes flat or gently sloped terrain suitable for distributed array expansion

### Medium-Voltage Electrical Distribution Network

#### Phase 1 Configuration
- **Topology Minimum Requirement:** Loop-capable architecture at full Phase 2 buildout
- **Prohibited:** Radial-only Phase 1 designs (single point of failure; cannot transition to loop-redundancy later)
- **Planning Implication:** Phase 1 must include enough substations/switching to enable closed-loop operation when Phase 2 interconnects

#### Full Buildout (Phase 1 + Phase 2)
- **Closed-Loop Topology:** Multiple substations with cross-connections; loss of any single component does not isolate major load
- **Resilience Rationale:** Large campus loads (data centers, SOEC, VVLS) require high reliability; radial networks unacceptable for utility-scale operation

### Data Center District Spatial Planning

#### Phase 1 Reservation
- **Spatial Impact:** Phase 1 layout must reserve all future data center building pads
- **Utility Corridor Reserve:** Infrastructure corridors sized for "ultimate data center district" (full Phase 2 footprint)
- **Partial Buildout Allowed:** Only subset of reserved pads constructed in Phase 1; remainder constructed in Phase 2

#### Infrastructure Categories Reserved
- **Power Distribution:** AC/DC feed corridors for ultimate buildout
- **Cooling Loops:** Chilled water/coolant return mains sized for full load
- **Water Supply:** Potable + recirculated cooling source capacity planned for full campus
- **Fire Protection:** Suppression mains, pump house, monitoring loops for entire district
- **Hydrogen Distribution:** Pipe runs to all future facility locations (if H₂ used for heating/fuel)

### Infrastructure Corridor Freeze (Phase 1)

#### Categories Locked at Phase 1
1. **Electrical Distribution:** Medium/low-voltage backbone, substation locations
2. **Cooling Net:** Chilled water mains, return headers, pump house location
3. **Water Infrastructure:** Supply mains, recirculation loops, storage tank locations
4. **Fire Protection:** Sprinkler mains, foam lines, hydrant placement, pump/reservoir
5. **Hydrogen Distribution:** Main transmission line, branch points, isolation valves (if applicable)

#### Constraint
- **No Rework Allowed:** Phase 1 corridor placement governs Phase 2 connection points
- **Planning Impact:** Utility routing analyzed for Phase 1 + Phase 2 loads simultaneously; Phase 1 construction includes oversized capacity in corridors to accommodate Phase 2 without relocating pipes/cables

### Architectural & Governance Alignment

#### AO Design Output Governance Review
- **Review Standard:** HC-MGD-001 (Heber Campus Management Governance Document 001 — defines expansion doctrine)
- **Charter Reference:** Master Architecture Charter (overarching design philosophy)
- **Timing:** Prior to "geometry hardening" (finalization of site layout before construction)
- **Purpose:** Ensure design compliance with multi-phase expansion expectations

#### ATB AO Governance Alignment Process
- **Required Confirmation:** Explicit statement of compliance with expansion doctrine from Agile-Technical-Board (ATB)
- **Variance Documentation:** Any deviations from doctrine must be:
  - Formally documented
  - Justified (cost, schedule, technical feasibility)
  - Approved by ARCHITECT authority
- **Design Lock:** Once governance alignment confirmed and variances approved, design proceeds to hardening phase

### Summary: Expansion-First Design Philosophy
- **Phase 1 is Infrastructure Proof-of-Concept:** Demonstrates VVLS, SOEC, data center operations at interim scale
- **Phase 2 is Scaling Replication:** Builds 3.5 GW additional solar, expanded data center (DC2, DC3...) using proven Phase 1 architecture
- **No Design Rework:** All Phase 1 corridors, connections, topologies compatible with Phase 2 without retrofit
- **Modular Growth:** Standardized module approach (solar arrays, data center buildings) enables rapid replication
- **Governance Gate:** Expansion strategy validated early; variances require formal ARCHITECT approval to prevent late-stage constraints

---

## Heber Campus Baseline Product Slate, Generation Capacity, & Expansion Envelope (2025-12-27)

### Baseline Liquid Fuels Production (Phase 1)
- **Total Capacity:** 18,000 bpd (barrels per day) liquids
  - Diesel: 12,000 bpd (66.7%)
  - Jet-A: 4,000 bpd (22.2%)
  - LPG: 2,000 bpd (11.1%)
- **Product Distribution:** Multi-product fuels enable diverse customer acquisition (aviation, trucking, agricultural equipment, industrial heating)
- **Feedstock:** Syngas from hydrogen + biomass-derived CO₂ routed through Fischer-Tropsch or similar catalytic synthesis
- **Market:** Merchant export after internal campus fuel requirements (VVLS, ground ops, data center fuel backup)

### Baseline Electrical Generation (Phase 1)
- **Nameplate Capacity:** 1.5 GW
- **Dispatch Priority:** Internal campus consumption (SOEC, data centers, VVLS launch prep, manufacturing, HVAC)
- **Surplus Capability:** Merchant export to regional grid during low-internal-load periods
- **Generation Mix:** PV (1.5 GW), SMR thermal (coupled with SOEC + biomass steam), battery storage (intra-day smoothing)
- **Revenue Model:** Premium pricing for off-peak solar export; potential grid services contracts (frequency regulation, etc.)

### Long-Term Expansion Envelope (50-Year Horizon)

#### Ultimate Capacity Targets
- **Electrical Generation:** Scale to approximately 5 GW nameplate
  - Phase 2 addition: ~3.5 GW (primarily solar expansion)
- **Liquid Fuels Production:** Scale to approximately 100,000 bpd
  - Product mix proportions may adjust based on market demand evolution

#### Expansion Contingency
- **Funding Model:** Phased, cash-flow-funded expansion
- **Rationale:** Each phase must be self-funding from prior-phase operations; no speculative debt financing on unproven capacity
- **Timing:** 50-year horizon allows for market evolution, technology maturation, and revenue accumulation to justify each expansion phase

#### Scaling Implications
- **Solar PV:** ~3.3x expansion (1.5 → 5 GW) on available flat land in northwest quadrant and reserve corridors
- **SOEC/H₂:** Proportional scaling to maintain H₂ production for synfuel synthesis (457 t/day → ~1,500 t/day estimated)
- **Data Centers:** Expansion from interim footprint to full reserved district (multi-building campus)
- **Biomass Feedstock:** External sourcing must scale proportionally to support larger synfuel production rates

### Master Guideline Document HC-MGD-001 Rev A

#### Document Status & Authority
- **Adoption Date:** 2025-12-27
- **Form:** Revision A baseline (may be superseded by Revision B, C, etc. as design matures)
- **Governance Scope:** Governing design baseline for ALL Heber Campus subsystems and interfaces
- **Authority Level:** Canonical document; exceptions require explicit ARCHITECT approval

#### Scope of HC-MGD-001
- Power system architecture (1.5 GW Phase 1, 5 GW ultimate)
- Refinery/synfuel production (18,000 bpd Phase 1, 100,000 bpd ultimate)
- Data center cluster design and cooling/power integration
- VVLS facility integration and launch operational protocols
- Site plan and infrastructure corridor standards
- Environmental, regulatory, and social governance
- Expansion-first design principles (Phase 1/Phase 2 compatibility)

#### Reference Standard
- All subsequent AO (Agile-Observable) design outputs must be cross-checked against HC-MGD-001 prior to geometry hardening
- Variances documented and ARCHITECT-approved

### Agricultural Footprint Removal & External Biomass Sourcing

#### Phase 1 Decision
- **Footprint Elimination:** Remove all agricultural production from physical Heber Campus property
- **Rationale:** Land utility maximization (solar, buildings, infrastructure corridors take priority); agricultural < energy density of engineered infrastructure
- **Biomass Supply:** Transition to contract/partnership supply model

#### Biomass Supply Strategy

**Primary Model: External Partnerships**
- Contract for feedstock delivery from existing agricultural/forestry operations in northern Arizona
- Supply chain flexibility: can source from multiple regional vendors without on-site cultivation constraints
- Lower capital: no on-site biomass production facilities (HRSG, handling equipment for harvested material only)

**Strategic Partnership: Navajo Nation**
- **Integration Scope:** Integrated but non-co-located supply relationship
- **Partnership Structure:** Long-term agricultural/feedstock contracts with Navajo Nation entities
- **Supply Target:** Herbaceous biomass (switchgrass, miscanthus) or wood residues (forest thinning byproducts)
- **Economic Benefit:** Revenue-sharing partnership supports Navajo Nation economy; Heber Campus obtains sustainable, regional feedstock
- **Scale:** Potential to source 100+ thousand tons/year to support 100,000 bpd refinery expansion at full buildout

### Employment Baseline & Scaling

#### Phase 1 (Initial Build-Out)
- **Direct Employment:** Approximately 750-800 jobs
- **Labor Categories:**
  - Operations & maintenance (power, refinery, data center)
  - Manufacturing/assembly (VVLS hardware, synfuel testing)
  - Engineering & planning (AO design, subsystem integration)
  - Administration, security, environmental compliance
- **Wage Profile:** High-skill technical jobs (engineers, operators); regional wage baseline competitive with mining/energy sector

#### Phase 2 (Ultimate 5 GW / 100,000 bpd)
- **Direct Employment:** Approximately 1,800-2,300 jobs
- **Scaling Factor:** ~2.3x employment from Phase 1 → Phase 2
- **Role Evolution:** More maintenance/operations staff proportional to larger facility footprint; continuous data center operations growth
- **Economic Impact:** Highest per-capita employment opportunity in northern Arizona region

### Regional Labor Shed Model

#### Primary Feeder Communities
Identified commuting-distance communities with available workforce and housing:
1. **Winslow** (~50 miles south) — Historic rail hub; diverse labor pool
2. **Joseph City** (~25 miles southeast) — Rural agricultural community; light industrial experience
3. **Holbrook** (~70 miles east) — County seat; established services/housing
4. **Snowflake-Taylor** (~15 miles north) — Closest town cluster; primary feeder
5. **Show Low** (~40 miles north) — Regional employment hub; ski industry seasonal labor
6. **Payson** (~60 miles west/northwest) — Mountain community; outdoor recreation base

#### Commuting Distance Rationale
- 50-70 mile commute acceptable for high-wage technical jobs (3-4 hour round trip, carpool standard)
- Housing availability in feeder communities at rural price points (~$150-250K range estimated)
- No major city within short drive; workforce development strategy prioritizes skill training in existing communities

### Transportation Strategy & Regional Connectivity

#### Strategy Priority
- **Primary Focus:** Regional roadway and rail connectivity to/from campus
- **Explicit Constraint:** Minimize residential expansion within Heber-Overgaard town limits
- **Rationale:** Preserve town character; Heber Campus is major employment draw but not intended to transform local community into bedroom suburb

#### Infrastructure Strategy Components

1. **Rail Loop Connectivity**
   - Northbound spine toward I-40 leverages existing corridors
   - Goal: Heavy rail access for bulk fuel/chemical shipment and power plant equipment delivery
   - I-40 as terminal hub (national rail network access)

2. **Pipeline Access**
   - Northbound corridor also accommodates pipeline for synfuel export
   - Possibility of grid-interconnected H₂ pipeline to regional end-users (future)

3. **Highway Integration**
   - AZ-99 identified as preferred backbone for campus connectivity to I-40
   - Minimizes new road construction; builds on existing right-of-way where feasible

#### Specific Roadway Projects

**AZ-99 Backbone Upgrade**
- Current status: Exists but 2-lane configuration
- Role: Primary daily commute route for workforce; also main delivery/export route for bulk cargo
- Upgrade: Estimated 4-lane with truck lanes; cost split with state/county partners

**SR-260 Four-Lane Expansion**
- **Existing Study:** ADOT already planning SR-260 expansion as part of statewide corridor optimization
- **Heber Campus Role:** Material demand anchor (350-400 daily truck trips estimated at full buildout)
- **Leverage Opportunity:** Heber Campus can accelerate ADOT funding prioritization by demonstrated anchor demand
- **Timeline:** Coordination with state capital plan cycles (5-10 year horizon)

### Governance Engagement Sequencing

#### Phase Sequence (Early Engagement)
1. **Navajo County Leadership** (first)
   - County Commission, Economic Development Authority
   - Goal: Early county support, zoning alignment, permitting pathway clarity
   - Risk Mitigation: Establish local political baseline before state/federal engagement

2. **State Agencies** (second)
   - Arizona Department of Energy Minerals & Natural Resources
   - Arizona Corporation Commission (grid interconnection oversight)
   - ADOT (roadway planning coordination)
   - Arizona Department of Environmental Quality (air quality, water, waste permits)

3. **Federal Agencies** (third, contingent on state alignment)
   - U.S. Forest Service (if any national forest access required)
   - BLM (if public lands involved; unlikely at Heber-Overgaard)
   - Department of Energy (potential loan guarantees, hydrogen hub grants)

#### Rationale for Sequencing
- **Local First:** County's support is prerequisite for any larger engagement; early alignment reduces downstream opposition
- **State Next:** ADOT/environmental agencies set permitting pathway; state approval faster/more predictable than federal
- **Federal Last:** Engage after state/local alignment; federal grants/loans support pre-approved projects

### Integrated Power + Refinery + Data Center Campus Model

#### Economic Model Validation
- **Multi-Revenue-Stream Architecture:**
  1. Electricity export to grid (merchant power sales)
  2. Liquid fuels export (diesel, Jet-A, LPG merchant sales)
  3. Data center services (compute rental, cloud infrastructure)
  4. VVLS launch services (payload-to-orbit revenue)
  5. Hydrogen sales (if external market develops; currently internal)

#### Resilience & Budget Stability
- **Single-Revenue Dependency Risk Eliminated:** No single market collapse destroys economics
  - Power market downturn → refinery/data center/VVLS still operational
  - Fuel market volatility → power/data center/VVLS cushion margins
  - Data center demand plateau → power/fuel/VVLS still generate revenue
- **Revenue Timing Diversity:** Power (daily spot market), fuels (monthly contracts), data center (recurring SaaS), VVLS (per-launch)
- **Cost Absorption:** Fixed campus costs (payroll, utilities, maintenance) spread across 4-5 revenue streams = lower breakeven threshold

#### Financial Implications
- **IPO/Financing Attractiveness:** Multi-revenue campus model is materially stronger than pure-play power or pure-play refinery
- **Insurance/Risk Profile:** Portfolio approach makes project bankable even if one sector faces temporary downturn
- **Expansion Path:** Each revenue stream can fund next phase without dependent timing

#### Competitive Moat
- **Integrated Thermal Management:** Reject heat from power generation → synfuel synthesis thermal input → data center cooling source
- **Location Advantage:** Northern Arizona solar + seasonal cooling + workforce access + existing corridors = compound site advantage
- **Technology Integration:** VVLS facility uses campus power + hydrogen; launch services market exclusive to Heber location
