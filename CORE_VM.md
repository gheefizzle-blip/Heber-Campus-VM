# CORE_VM.md

**Last Updated:** 2026-02-09 15:10
**VM_VERSION:** 20260209-1510
**Status:** Delta applied - Holbrook Ranch Dual-Campus Strategy & Acquisition Doctrine

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

---

## BESS Technology Selection & Bankability Doctrine (HC-MGD-001 Appendix B, 2026-02-07)

### Appendix B Approval & Governance Adoption

#### Document Status
- **Title:** BESS Technology Selection and Bankability Doctrine
- **Association:** Appendix B to HC-MGD-001 (Master Guideline Document)
- **Adoption Date:** 2026-02-07
- **Authority:** Governing policy for all Heber Campus battery system procurement and deployment decisions
- **Revision Path:** Subject to future revisions as commercial battery technology landscape evolves

#### Doctrine Purpose
Establish mandatory financial and commercial gating criteria for battery technology selection to ensure:
- Project financeability through standard debt/equity channels (not speculative venture funding)
- Insurance underwriting acceptance (eliminating uninsured single-point-of-failure risk)
- Price transparency and normalized vendor procurement processes
- Technical maturity appropriate to utility-scale operational criticality

### Bankability, Insurability, and Price as Mandatory Gate Criteria

#### Three-Pillar Selection Framework

**Pillar 1: Financeability (Bankability)**
- **Definition:** Technology must be acceptable to traditional project finance lenders (commercial banks, export credit agencies, infrastructure funds)
- **Assessment Basis:**
  - Existing installed base of 100+ MW for the technology class (supply chain proven)
  - 10+ years operational history or equivalent accelerated test data
  - Licensed vendor with investment-grade credit rating or venture backing (Series D+)
  - Demonstrable O&M cost experience from existing deployments
  - Clear warranty/liability structure with insurance underwriting support
- **Bankability Rejection Triggers:**
  - Technology < 100 MW cumulative deployment
  - No commercial insurance products available
  - Warranty claims history exceeding 5% annual failure rate
  - Single-vendor supply chain with <2 alternative sources

**Pillar 2: Insurability**
- **Definition:** Technology must have available commercial insurance products from A.M. Best-rated insurers
- **Insurance Products Required:**
  - Property/casualty coverage for fire, explosion, thermal runaway events
  - Performance coverage (availability guarantee, uptime SLA support)
  - Liability coverage for environmental contamination (electrolyte spill, thermal runaway emissions)
  - Warranty extension options through captive or commercial insurers
- **Insurability Assessment:**
  - Request for insurance quotes from 3+ primary insurers (Zurich, Allianz, Chubb, AXA, etc.)
  - Insurable value must be ≥95% of installed cost (full risk transfer possible)
  - Annual insurance premium acceptable if ≤5% of O&M budget
- **Insurability Rejection Triggers:**
  - No insurance quotes from A.M. Best A-rated insurers
  - Insurable value <90% of system cost
  - Insurance premium exceeds 5% annual O&M
  - Insurer exclusions for "experimental" or "developmental" technologies

**Pillar 3: Price (Levelized Cost)**
- **Definition:** Technology must demonstrate competitive total-cost-of-ownership relative to bankable alternatives
- **Pricing Metrics:**
  - **$/kWh (energy capacity cost):** Normalized turnkey installed cost per kilowatt-hour
  - **$/kW (power capacity cost):** Normalized turnkey installed cost per kilowatt of discharge/charge rate
  - **Lifecycle Cost:** $/kWh-cycle, accounting for degradation, replacement, and O&M over 25-year system life
- **Price Comparison Example:**
  - Option A (Lithium-ion): $150/kWh, $1,200/kW, 10,000 cycle life → $15/kWh-cycle + O&M
  - Option B (Flow battery): $180/kWh, $800/kW, 20,000+ cycle life → $9/kWh-cycle + O&M
  - Price weighting: 40% normalized $/kWh, 30% $/kW, 30% lifecycle cost
- **Price Rejection Triggers:**
  - Technology >20% more expensive than bankable alternatives on levelized cost basis
  - Vendor unwilling to provide 5-year fixed-price warranty
  - No independent cost validation from 3rd-party engineer (engineering firm, analyst)

### Heber Campus BESS Program Constraints

#### Technology Eligibility Framework

**Tier 1: Approved for Immediate Deployment (Phase 1 & 2)**
- Lithium-ion (LFP chemistry preferred for safety/cycle life)
  - Example vendors: CATL, BYD, LG Chem, Panasonic
  - Status: 200+ GW cumulative deployment globally
  - Insurance: Widely available, <3% annual premium
  - Price: $100-150/kWh, mature supply chain

- Flow batteries (Vanadium redox, zinc-bromine, iron-air emerging)
  - Example vendors: Redflow, Australian Vanadium, Form Energy
  - Status: 100+ MW cumulative deployment (growing)
  - Insurance: Available from specialty underwriters
  - Price: $150-200/kWh, but excellent cycle life advantage

- Hybrid systems
  - Example: Li-ion for power (fast response) + Flow for energy (duration)
  - Status: Case-by-case evaluation per sub-component bankability

**Tier 2: Conditional Approval (Pilot/Demonstration Only, <10% of Capacity)**
- Emerging chemistries with:
  - 10-50 MW cumulative deployment
  - Insurance quotes obtained (higher premium acceptable for demonstration)
  - Dedicated O&M budget for learning/optimization
  - Explicit ARCHITECT approval for each deployment
  - Timeline: Eligible for Phase 2 scaling only after Phase 1 pilot demonstrates <5% failure rate

**Tier 3: Excluded from Heber Campus Phases 1 & 2**
- Experimental/non-commercial technologies:
  - **All-Solid-State Batteries** (primary example)
  - Lithium-air, lithium-sulfur, sodium-ion (early stage)
  - Novel chemistries with <10 MW cumulative, no insurance products
  - Rationale: Cannot meet financeability, insurability, or price gate criteria

### All-Solid-State Battery Exclusion: Detailed Justification

#### Technology Status Assessment

**Commercial Readiness Level: TRL 7-8 (Prototype/Limited Commercial)**
- Current deployment: <1 MW globally (mostly research labs, limited pilot programs)
- Vendor status: Toyota (2027-2030 target production), Nissan, QuantumScape, Samsung (development stage)
- Production capacity: <100 MWh/year globally as of 2026

#### Financeability Assessment: FAILED
- **Deployed Base:** Insufficient (<1 MW vs. 100+ MW threshold)
- **Operational History:** <2 years in any field deployment; insufficient field data
- **O&M Experience:** No operational data from utility-scale systems
- **Warranty Structure:** No established warranty/liability framework from manufacturers
- **Lender Assessment:** Project finance lenders decline FICO scoring for all-solid-state as project technology risk

#### Insurability Assessment: FAILED
- **Insurance Availability:** NO commercial A.M. Best-rated insurers offer all-solid-state battery coverage
- **Thermal Runaway Risk:** Solid electrolyte fire propagation mechanisms not fully characterized; insurers require extensive testing
- **Performance Coverage:** No historical claims data to establish premium/SLA models
- **Liability Exclusion:** Environmental liability for solid electrolyte contamination unresolved in insurance contracts
- **Insurer Statement:** Top-tier insurers (Zurich, Allianz) explicitly exclude all-solid-state from current product offerings; 10+ year development timeline anticipated before mainstream coverage

#### Price Assessment: INADEQUATE
- **Current Pricing (2026 projections):**
  - Prototype units: $1,000+/kWh (unvetted quotes, limited data)
  - Manufacturing ramp-up (2027-2030): $300-500/kWh extrapolated (guidance only, unproven)
- **Comparison to Bankable Alternatives:**
  - Li-ion (2026): $100-150/kWh, 10,000 cycle life
  - Flow (2026): $150-200/kWh, 20,000+ cycle life
  - All-solid-state (2026 projection): $300-500/kWh, ~5,000 cycle life (estimated)
  - **Normalized lifecycle cost:** All-solid-state 4-6x more expensive than bankable alternatives
- **Price Rejection:** Fails gate criterion (>20% premium); no pathway to competitive pricing in Phase 1/2 timeframe

#### Risk Profile: Project Jeopardy
- **Single Vendor Dependency:** If Toyota/QuantumScape manufacturing fails, entire BESS program at risk
- **Unproven Failure Modes:** Thermal runaway in solid electrolytes could trigger catastrophic multi-unit failure (domino effect unknown)
- **Warranty Exposure:** Manufacturer warranty uncertain; full capital at risk if technology underperforms
- **Stranded Asset Risk:** If all-solid-state proves incompatible with Heber Campus thermal management or operational envelope, system replacement obligation falls to campus

### Explicit Deployment Prohibition

#### Policy Statement
**Heber Campus battery system procurement for Phase 1 and Phase 2 shall NOT include all-solid-state battery technology in any capacity, including:**
- Primary energy storage (BESS system core)
- Hybrid augmentation (secondary capacity)
- Pilot/demonstration (any scale, including <1 MW)
- Future phases unless all three gate criteria (financeability, insurability, price) are independently validated

#### Compliance Requirement
- Any proposal to deviate from this prohibition requires:
  - Written justification addressing all three gate criteria
  - Independent third-party bankability assessment (commercial finance advisor)
  - Insurance quote from minimum 3 A.M. Best A+ rated carriers
  - ARCHITECT-level approval (not delegable to project management)

### Vendor Selection Process & Procurement Protocol

#### Approach: Normalized Transparent Comparison

**Pricing Basis (Turnkey, Delivered, Installed)**
- **$/kWh:** Includes battery cells, electronics (inverter, BMS), installation labor, integration to campus DC bus, 1-year commissioning support
- **$/kW:** Per unit power capacity (MW rating × $1,000/MW or GW rating × $1,000,000/GW)
- **Warranty:** Standard commercial terms (5-10 years for Li-ion, 10-20 years for flow)
- **Insurance:** Vendor responsible for arranging initial insurance; cost responsibility to be negotiated

#### Vendor Evaluation Matrix

**Scoring (100-point scale):**
1. **Bankability (20 points)**
   - Installed base scale (0-5 pts)
   - Operational history (0-5 pts)
   - Financing customer list (0-5 pts)
   - Supply chain robustness (0-5 pts)

2. **Insurability (20 points)**
   - Insurance quote availability (0-8 pts)
   - Insurable value ≥95% (0-6 pts)
   - Premium acceptability <5% O&M (0-6 pts)

3. **Price (40 points)**
   - $/kWh competitive positioning (0-15 pts)
   - $/kW competitive positioning (0-15 pts)
   - Lifecycle cost (25-year NPV, 7% discount) (0-10 pts)

4. **Technical Fit (20 points)**
   - DC voltage/current compatibility (0-5 pts)
   - Thermal management integration (0-5 pts)
   - Operational envelope match (0-5 pts)
   - Warranty structure clarity (0-5 pts)

**Procurement Process:**
1. RFQ to qualified vendors (minimum 4 shortlisted)
2. Transparent pricing table published internally
3. Insurance quotes collected independently for each vendor option
4. Scoring applied per matrix; ARCHITECT validates weighting
5. Preferred vendor selected; negotiation on secondary terms (payment schedule, spare parts, training)

### Summary: BESS Doctrine Governance

- **Financeability** ensures project can access standard capital markets
- **Insurability** eliminates uncompensated risk transfer to campus owners
- **Price competitiveness** ensures resource efficiency within budget constraints
- **All-solid-state explicitly excluded** due to combined failure on all three criteria
- **Vendor selection transparently governed** with price as primary lever alongside technical/commercial quality
- **Future pathway open** if all-solid-state eventually achieves commercial maturity (10+ year horizon)

---

## Heber Campus Global Roadmap & Multi-Phase Expansion Doctrines (2026-02-08)

### Data Center Cooling Architecture

#### Primary System: Closed-Loop Geothermal Borefield
- **Technology:** Ground-source heat pump with depth-drilled wells (~300-500 m boreholes in northern Arizona geology)
- **Thermal Capacity:** Modeled for Phase 1 data center cluster cooling demand (estimated 50-100 MW thermal extraction)
- **Operational Profile:** Year-round baseload cooling source with relatively constant ~50-55°F ground temperature at depth
- **Advantage:** Eliminates seasonal swings; highly efficient vs. air-cooled or tower-cooled systems in Arizona high-temperature summers

#### Secondary System: Modular Central Ammonia (NH₃) Cooling Plant
- **Refrigerant:** Ammonia selected for high thermodynamic efficiency and low GWP (no ozone/climate impact)
- **Redundancy:** N+1 configuration (multiple compressor trains; loss of one unit does not degrade DC SLAs)
- **Modularity:** Central plant sized for Phase 1; additional NH₃ modules added in Phase 2/3 without redesign
- **Safety:** Ammonia leak detection + local ventilation + operator training per industrial standards

#### Control Logic Hierarchy (Priority Order)
1. **Free Cooling First** (Economizer Mode)
   - Outside air temperature <55°F during winter → direct air-side heat exchanger used
   - Eliminates compressor/geothermal draw when possible
   - Estimated 30-40% of annual hours in Arizona high-elevation sites

2. **Geothermal Second** (Ground-Source Heat Pump Active)
   - Outside air >55°F and DC cooling demand <geothermal capacity → geothermal supplies cooling load
   - Lower power consumption than compressor-driven refrigeration
   - Estimated 40-50% of annual hours

3. **Compressors Last** (NH₃ Plant Active)
   - Daytime peak cooling demand or geothermal capacity exceeded → NH₃ compressors activated
   - Estimated 10-20% of annual hours; primarily summer daytime

#### Net Effect
- **Energy Efficiency:** Annual cooling energy reduced 20-30% vs. all-air or all-tower-cooled systems
- **Cost Reduction:** Lower operational electricity cost for DC climate control
- **Thermal Stability:** Constant geothermal source temperature improves server reliability vs. fluctuating ambient

### Heat Recovery Water Loop (HRWL) Doctrine - Governance Policy

#### Formalized Authority
- **Governance Document:** HC-MGD-001 Appendix (heat recovery management)
- **Adoption Date:** 2026-02-08
- **Authority Level:** Binding operational and design constraint for all Heber Campus thermal systems

#### HRWL Architecture: HX-Only Isolation Design
- **Dedicated Circuit:** Closed-loop circuit carrying hot condensate from refrigeration plant and reject heat from electrical equipment
- **Design Principle:** No direct integration or cross-flow between HRWL and process loops; all heat transfer through isolated heat exchangers (HX) only
- **Containment Benefit:** Prevents contamination; prevents operational coupling

#### Thermal Buffer Tank Component
- **Function:** Intermediate storage vessel (estimated 500-1,000 m³ volume) at HRWL circuit midpoint
- **Purpose:** Smooth mismatch between heat generation (compressor operation, IT equipment) and heat demand cycles
- **Operational Benefit:** Allows short-duration peak loads without requiring simultaneous downstream consumption
- **Result:** Reduces cycling on compressors and process equipment

#### Heat Sink Registry & Allocation Control

**Heat Sink Registry (Pre-Approved Thermal Loads)**
- Formal list of all approved thermal loads that may consume HRWL heat:
  - SOEC feed water preheating (primary industrial heat sink)
  - Biomass plant steam conditioning (secondary)
  - Campus space heating (minimal in Arizona climate; winter-only)
  - Process water heating (if applicable; e.g., washdown water at fuels facility)

**Allocation Rules & MECSAI Authority**
- MECSAI (Multi-Energy Campus Supervisory Architecture Intelligence) system manages HRWL dispatch
- MECSAI may only distribute recovered heat to sinks on approved registry
- Heat allocation among registered sinks performed dynamically based on demand signals
- **Critical Constraint:** MECSAI cannot unilaterally alter loop topology, add new sinks, or bypass registry

**Rationale:** Prevents ad-hoc thermal connections that could:
- Introduce contamination from untested fluids
- Create uncontrolled feedback coupling (e.g., heating SOEC too much → electrolyzer efficiency loss → negative loop)
- Violate insurance liability underwriting (unvetted thermal interfaces)

### Phase 2 Operating & Financial Doctrine (HC-PH2-001 Rev A)

#### Governance Status
- **Formal Document:** HC-PH2-001 Revision A (binding policy)
- **Scope:** Phase 2 site planning, construction, commissioning, and 25-year operations baseline
- **Authority Level:** Governance-binding (all projects must align or seek explicit variance approval)

#### Operational Philosophy: DC + Solar-Led Expansion

**Strategic Approach**
- Phase 2 growth prioritizes data center buildout (DC2 building) and solar PV expansion (~3.5 GW additional)
- SMR and SOEC follow to support expanded DC cooling and H₂ production
- Rationale: DC and PV both have predictable capital recovery economics; SMR/SOEC deployment follows after cash-flow accumulation

**Night Treated as Managed Scarcity Window**
- Definition: ~6-8 PM to ~6-8 AM (winter shorter, summer longer)
- Operational Constraint: Night consumption must rely on battery (depleted by design) + firm generation (SMR/biomass at capacity limits)
- Control Strategy: No automatic fuel startup for load balancing; instead, load shaping enforced to fit available supply

**MECSAI Load-Shaping Enforcement**
- Automatic supervisory control system directs IT workloads, SOEC production, and chemical operations to fit night availability
- Objective: Avoid "routine" fuel burn (i.e., backup diesel generators or unplanned SMR load-follow)
- Trade-off: Intentional reduction in SOEC throughput and IT services during night hours (SLA guarantee reductions)

#### Phase 2 Night Load Management Targets (Planning)

**Data Center Night Deferrable IT: 35-40%**
- Definition: Workloads that can be deferred 4-6 hours without SLA violation (batch processing, archival backup, non-user-facing computation)
- Strategy: Schedule deferrable jobs for daytime when PV+battery abundant
- Result: Effective night DC load reduction 35-40% vs. 24/7 baseline
- Implementation: Application-level scheduling + workload broker (cloud orchestration)

**SOEC Night Output: 70-75% of Average**
- Full-day average SOEC output: ~457 t/day H₂ / 24 hours = ~19 t/hour
- Night reduction target: 70-75% of average = ~13-14 t/hour
- Method: Current density modulation only (electrolyzer input voltage/current reduced; stack temperature kept stable)
- **Constraint:** No thermal cycling (avoid freeze-thaw damage in SOEC stacks)
- Result: Night H₂ production continues but at reduced rate; storage feeds daytime synfuel synthesis

**Shift 10-20 MW Chemical Compression/Transfer to Daylight**
- High-power industrial operations: Hydrogen compression (gas→liquid or high-pressure), CO₂ liquefaction, synfuel product pumping
- Night approach: Run at minimal operating point only; minimize night operation
- Daytime approach: Accumulate daytime power availability (excess PV after DC/SOEC primary loads) into compression/transfer operations
- Result: ~10-20 MW aggregate load shifted from night to daytime peak windows

### Phase 2 Power Export Doctrine (Planning)

#### Firm Export Limit: 50 MW 24/7

**Definition:** Contractual obligation to deliver minimum 50 MW to regional grid at all hours, backed by guaranteed supply (SMR + biomass)
- SMR baseline: 320 MW (4 units × 80 MW) electric capacity (constrained to 25 MW reserve)
- Biomass baseline: ~100 MW electric output (constrained to 25 MW reserve)
- Available for firm export: 50 MW maximum at any hour

**Rationale for Conservative Firm Limit:**
- Firm power contracts fetch highest price in wholesale markets (~$60-80/MWh vs. $30-40/MWh spot)
- But firm obligation creates operational constraint: cannot reduce output for internal SOEC needs
- Therefore, firm export limit is kept conservative (50 MW vs. 150-200 MW available from SMR/biomass)
- Excess capacity reserved for internal load variability and emergency response

**Backing Source:** SMR + Biomass ONLY
- Solar and battery cannot contribute to firm export (variable/intermittent)
- If SMR/biomass tripped offline, firm export not met → contract penalty
- Therefore, only capacities with high availability (~90%+) included in firm commitment

#### Flexible Exports: Primarily Daytime

**Definition:** Optional additional export above 50 MW firm, available when PV generation or other sources permit
- Daytime excess (PV >1.5 GW available after internal load) → flexible export opportunity
- Flexible price: spot market price (~$30-50/MWh), lower than firm but contributes revenue
- No contractual obligation; grid operator cannot rely on availability

**Operational Logic:**
- 1.5 GW PV available at midday
- Internal loads: DC (100-150 MW), SOEC (200-300 MW), VVLS (20-50 MW during ops), manufacturing (30-50 MW), campus intra-day (20-30 MW)
- Aggregate internal demand: 370-580 MW typically
- Excess available: 900-1,130 MW → 50 MW firm + 850-1,080 MW flexible export possible

**Financial Impact:** Flexible exports provide 15-25% additional revenue during high-PV seasons; limited to ~25-30% of total power revenue

#### Constraint: No Firm Export Shall Force SOEC Reduction or Fuel Burn

**Policy Statement:** If maintaining 50 MW firm export requires:
- Reducing SOEC below required daily H₂ production (~457 t/day minimum), OR
- Starting backup fuel generation (SMR thermal shift to electric overdrive, or biomass ramp to unsustainable speed)

Then:
- 50 MW firm export is suspended
- Internal loads (SOEC, DC, manufacturing) take full SMR/biomass output
- Grid notified of firm export curtailment (contractually allowed provisions)

**Rationale:** H₂ production and site autonomy are higher-priority than export revenue in case of conflict

### Phase 3 Expansion & Scale Doctrine (HC-PH3-001 Rev A)

#### Document Status
- **Formalized:** 2026-02-08 (governance-binding policy)
- **Scope:** Phase 3 planning and deployment guidance (estimated 2030-2035 timeframe and beyond)

#### Phase 3 Target Capacities

**Data Center Growth Trajectory**
- Phase 1: 1 DC building (200-300 MW IT electrical load)
- Phase 2: 2 DC buildings (400-600 MW total)
- Phase 3: 4 DC buildings (800-1,200 MW total)
- **Ultimate Potential (Phase 3 buildout): 16 DC buildings possible** (3.2-4.8 GW IT electrical load infrastructure)

**Solar Expansion**
- Phase 1: ~1.5 GW
- Phase 2: ~1.5 +3.5 GW = 5 GW cumulative
- Phase 3: 5 GW + expansion → up to 5 GW sustained (land constraints limit further in Arizona; may shift to Southwest replication sites)

**Refinery Scaling**
- Phase 1-2: 18,000 bpd baseline
- Phase 3: scale toward 100,000 bpd via:
  - SOEC H₂ production scaling (457 t/day → 1,500 t/day)
  - CO₂ sourcing expansion (40,000 t/day required)
  - SMR/SOEC modular replication (additional reactors added, not monolithic expansion)

**SMR/SOEC Replication Strategy**
- Phase 1: 4 SMR units + 3-4 SOEC modules planned
- Phase 2: Replicate modular pattern (no new designs required)
- Phase 3: Additional SMR/SOEC trains added if Phase 2 performance validates economics and regulatory approvals obtained

#### Gating Criteria: Phase 2 Performance Triggers

**Validation Requirements Before Phase 3 Commitment:**
1. **SMR operability:** >90% average availability over 3 years Phase 2 operation
2. **SOEC uptime:** >85% hydrogen production vs. target, <2% unplanned downtime
3. **Data center PUE:** <1.3 demonstrated over 2 high-cooling-demand seasons
4. **H₂ cost competitiveness:** Landed cost <$2.50/kg (all-in including capital recovery)
5. **Synfuel production margin:** >15% gross margin on Jet-A/Diesel sales
6. **Regulatory:** SMR licensing/operations approval + environmental permits for expanded scale

**Consequence of Trigger Failure:**
- Phase 3 expansion delayed or scaled back
- Alternative technology substitution evaluated (different SMR design, different thermal source, etc.)
- No automatic commitment to 100,000 bpd or 16-DC-building ultimate

### Global 100-Year Roadmap (Conceptual, Non-Binding Strategic Vision)

#### Phased Global Expansion (2026-2126)

**Phase 1: Heber, AZ Proof-of-Concept (2026-2035)**
- Demonstrate integrated power + refinery + data center model at 1.5 GW / 18,000 bpd scale
- Prove economic viability and operational maturity
- Establish workforce, regulatory pathway, supply chain

**Phase 2: Interior West Replication (2035-2050)**
- Replicate Heber model at 3-5 sites: Nevada, Idaho, Utah, Wyoming (high solar + inland locations)
- Leverage Phase 1 design library and O&M playbooks
- Reduce capital cost and delivery timeline via module standardization
- Target: 4-5 GW aggregate Interior West solar + refinery capacity

**Phase 3: Coastal Global Deployments (2050-2080)**
- Expand model to coastal regions (Australia, Gulf states, southern Spain, Chile)
- Adapt cooling (seawater vs. geothermal), feedstock (tropical biomass vs. Navajo Nation supply)
- Integrate desalination for water supply and export water as additional revenue stream
- Target: 10-15 sites globally, 20-30 GW aggregate

**Phase 4: OSY (Orbital Space Yeomanry) Integration (2080-2110)**
- Heber + Western US sites become export hubs for orbital logistics (fuels, utilities, materials)
- H₂ and synthetic fuels used for orbital transfer vehicles and LEO logistics
- VVLS and comparable launch facilities in multiple Interior West locations feed orbital demand
- Orbital platforms refueled from ground via tanker supply chains

**Phase 5: Lunar/Mars Extension (2110-2126)**
- In-situ resource utilization (ISRU) on Moon/Mars patterned after Heber model (trapped solar, thermal processes, electrolysis)
- Earth-based Heber sites provide initial feedstock (H₂, fuel, critical materials) for early lunar/Martian bases
- Conceptual only; technical pathway speculative

#### Critical Assumption: Fossil Fuels Not Eliminated

**Key Statement:** Fossil fuels decline in dependence but are NOT assumed eliminated by 2100+
- Backup SMR reactors provide firm power where solar insufficient (Phases 1-2 baseline)
- Biomass (renewable) replaces coal but **not assumed globally displaced**
- Synthetic fuels (H₂ + CO₂ → Jet-A/Diesel) themselves produced at Heber, **not fossil-free**—they require energy input (net zero only if production powered entirely by renewables)
- **Planning assumption:** Decarbonization path emphasizes intensity reduction, not elimination—civilization may still require chemical fuels for aviation/shipping even in 2100+

### Data Center Phasing & Load Variability

#### Sequential Commissioning Approach (Demand-Driven)

**Phase 1-3 Building Rollout (Planning)**
- Phase 1: 1 DC building commissioned (2027-2028 estimated)
- Phase 2: Add 1 more (DC2), total 2 buildings (2030-2032 estimated)
- Phase 3-A: Add 2 more (DC3, DC4), total 4 buildings (2035-2037 estimated)
- Phase 3-B (Ultimate): Add up to 12 more buildings, total 16 (buildout by 2045+)

**Demand-Driven Commissioning Philosophy**
- Each DC building commissioned only when anchor tenant contracts obtained
- No speculative buildout; each building financed by customer contracts before steel casting
- Delivers site scaling without stranded capacity risk

#### Data Center Load Modeling: Variable via PUE and Workload Migration

**PUE (Power Usage Effectiveness) Targets**
- Definition: Total campus power / IT electrical load = PUA / ITLoad
- Phase 1 Target: <1.25 PUE (cooling + overhead ~25% vs. IT workload)
- Phase 2 Target: <1.23 PUE (economies of scale in cooling/air handling)
- Phase 3 Target: <1.20 PUE (multiple DC buildings share cooling infrastructure)

**Workload Shifting Variability**
- Cloud tenants permitted to migrate workloads between Heber DC buildings and other regions
- Annual workload profile: 60-80% minimum (stable baseload), 20-40% variable (migrates seasonally or by demand)
- Campus planning assumes 70% utilization year-round (conservative) but models 40-100% operational range

**Impact:** Night load reduction strategies must account for workload variability; typical night reduction may vary 30-50% depending on customer demand patterns

### Biomass Feedstock Planning (Phase 1-2 Basis)

#### Daily Dry Mass Input Requirement

**Baseline Specification:** 7,000 tons/day dry biomass
- HRSG conversion: ~7,000 tons/day → ~100 MW thermal output (assumed 6.5 GJ/ton feedstock × 0.85 boiler efficiency)
- Syngas/chemical production: ~2-3 MW thermal equivalent for drying, preprocessing, handling

**Supply Source Strategy:** External partnership (no on-site cultivation)
- Primary: Navajo Nation agricultural/forestry partnership (estimated 4,000-5,000 t/day)
- Secondary: Regional biomass aggregators (Arizona, New Mexico) (estimated 2,000-3,000 t/day)
- Emergency: Purchased green waste / urban forestry (short-term only; higher cost)

**Baseline Pricing & Economics**
- Contract pricing baseline: ~$6/ton delivered
- Stress-test ranges: $4-8/ton
- Annual biomass cost: 7,000 t/day × 365 days × $6/t = **$15.3M/year baseline**

#### Sustainability & Supply Resilience

**Multi-Vendor Strategy:** Multiple vendors contracted; no single-source dependency ensures continuity

**Carbon Accounting:** Biogenic CO₂ from biomass combustion counted as carbon-neutral (replanted/regrown feedstock assumption)
- Does not contribute to carbon footprint of synfuel products
- Allows H₂ + biomass-CO₂ → Jet-A/Diesel to claim ~50% carbon intensity reduction vs. conventional refining

### Coastal Deployment Option: Seawater Desalination Revenue

#### Enhanced Model for Future Coastal Sites

**Technology Selection:** Reverse osmosis (RO) or multi-effect distillation (MED) co-located with coastal Heber-class campus
- Process water demand: ~500-1,000 m³/day for cooling, industrial use
- If overbuilt: 2,000-3,000 m³/day capacity, excess fresh water sold to local water authorities or industrial users

**Revenue Model:** Water sales as tertiary revenue stream (after power + fuels + data center)
- Desalinated water wholesale price: ~$0.50-1.00/m³ depending on region and contract terms
- Revenue potential: 1,500 m³/day × $0.75/m³ × 365 days = **$410K/year additional revenue** (modest but non-trivial)

**Efficiency Integration:** Campus waste heat from HRSG/SMR employed to drive thermal distillation or reduce RO energy consumption
- Estimate: 10-30% reduction in desal electricity demand via thermal integration

### Phase 3 Carbon Sourcing Strategy (Long-Horizon Variable)

#### CO₂ Supply Challenge for 100,000 bpd Target

**Total CO₂ Requirement:** ~40,000 t/day for 100,000 bpd refinery throughput

**Working Planning Split (Modeling Basis Only; Not Binding Commitment)**
- **40% Biogenic CO₂ Capture:** From biomass combustion HRSG exhaust (direct capture, minimal cost)
- **20% Fermentation CO₂:** From beer/ethanol production, agricultural facilities (regional partnership sourcing)
- **40% Direct Air Capture (DAC):** Atmospheric CO₂ via advanced separation (emerging technology; high energy cost)

**CO₂ Production Timeline**
- Phase 1-2: 7,000-8,000 t/day biomass → ~2,500-3,000 t/day CO₂ captured (single HRSG stream)
- Phase 3: Add fermentation sources (regional ethanol producers) → +1,000 t/day available
- Phase 3: Deploy DAC units → remaining 35,000+ t/day required (estimated 10-20 MW electrical equivalent for advanced separation)

**Long-Horizon Risk & Contingency**
- DAC technology not yet cost-competitive (<$150/ton CO₂ required; current $200-400/ton)
- Phase 3 CO₂ sourcing contingent on:
  1. DAC cost reduction (technology learning curve)
  2. Availability of waste heat sources for DAC energy efficiency improvement
  3. Regulatory support for CO₂ utilization (tax credits, carbon accounting pathways)

**Contingency Plan:** If DAC infeasible by Phase 3 gate, refinery capped at 50,000-60,000 bpd using biogenic + fermentation CO₂ only

### Revenue Strategy Doctrine (Clarified Hierarchy)

#### Primary Profit Engines

**1. Refined Fuels (Diesel, Jet-A, LPG) — Dominant Revenue**
- Gross margin target: 15-20% (synfuel production cost vs. market price)
- Phase 1-2 capacity: 18,000 bpd → ~$30-40M annual revenue (at $50/barrel average)
- Phase 3 capacity: 100,000 bpd → ~$170-200M annual revenue
- Market positioning: Premium price for low-carbon/synthesized fuels (avoid commodity competition)
- **Financial Dominance:** Typically 60-70% of total site revenue

**2. Data Center Services — Secondary Major Engine**
- Lease rates: $6,000-8,000/kW annual commitment (IT equipment load, colocation service)
- Phase 1: 300 MW IT load → $1.8-2.4B annual revenue (at full utilization)
- Phase 2: 600 MW → $3.6-4.8B annual revenue
- Phase 3: 1.2 GW → $7.2-9.6B annual revenue (largest single absolute revenue stream by Phase 3)
- Margin: 40-50% gross (power + cooling + facilities cost ~50-60% of revenue)
- **Financial Dominance:** Initially 25-35% of revenue, grows to 90%+ by Phase 3 due to scaling

#### Stabilizing Backbone

**Power Exports (Firm + Flexible) — Stabilizing, Not Core**
- Firm 50 MW @ $70/MWh = $307M annually
- Flexible daytime 400 MW average @ $40/MWh = $140M annually
- Total power revenue: ~$450M/year Phase 2 (modest vs. DC/fuels)
- Role: Provides revenue stability when customer demand fluctuates; smooths earnings variability
- **Financial Role:** 5-10% of total revenue (intentionally kept small due to operational constraints)

#### Capital Allocation Philosophy: Upside Flexibility Over Firm Commitments

**Firm Power Commitments: Keep Small with Optional Flexible Upside**
- Conservative approach: 50 MW firm committed (backed by SMR/biomass) only
- Additional capacity (up to 1.5 GW potential) kept flexible for:
  - Internal load growth (SOEC expansion, DC growth, VVLS demand)
  - Spot market sales (higher volatility but also higher marginal price)
  - Emergency/backup (reserve capacity not committed to customers)

**Rationale for Structured Upside:**
- Avoid locking in low-price long-term contracts that constrain operational flexibility
- Preserve ability to shift generation to internal high-value uses (H₂ production, DC cooling) when profitable
- Allow gradual market entry; reduce risk of unilateral contract default if SMR/biomass experience downtime

**Net Revenue Effect (Phase 2 Aggregated):**
- Refined fuels: $30-40M
- Data center: $3.6-4.8B
- Power (firm + flexible): ~$450M
- **Total Phase 2 gross revenue: ~$4.1-5.3B**

**Operating margin target:** 15-20% EBITDA (industry-typical for integrated energy + IT facilities) → ~$600-1,000M annual EBITDA Phase 2

**Capital recovery:** 10-15 year payback on $30-50B Phase 1+2 capital investment (varies by debt/equity structure and power prices)

---

## Phase 1 Energy Architecture Constraints, SOEC Procurement Policy, Nuclear Scaling Strategy & DC Bus Portability (2026-02-08)

### Phase 1 Energy Architecture: Commercial-Grade Nuclear & SOEC Only

#### Constraint Rationale

**Insurance & Lender Requirement**
- Phase 1 project must secure project-level financing (~$30-50B estimated capital)
- Lenders (commercial banks, development finance institutions) require:
  - Proven operational track record of core technology (nuclear reactors, electrolyzer systems)
  - Commercially insurable equipment with underwriter acceptance
  - Regulatory approval pathways with established precedent (no experimental reactor types)
  - Vendor performance guarantees and warranty structures

**Insurance Underwriting Acceptance**
- Nuclear reactor insurance is available ONLY for:
  - NuScale SMR (licensed by NRC; commercial deployment pathway established)
  - Gen III+ Large Light Water Reactors (Westinghouse, AREVA, etc. with operational fleet)
  - CANDU reactors (low commercial relevance in US context)
- Experimental designs (HTGRs, MSRs, FBRs) are uninsurable for commercial power plant liability
- SOEC electrolyzer systems must have:
  - 5,000+ cumulative operating hours in production environments (third-party vendors only)
  - Product liability insurance from vendor or underwriter
  - Spare parts/warranty availability from manufacturer (no internal spares sufficiency)

**Regulatory Approval Pathway**
- US NRC (Nuclear Regulatory Commission) has established licensing frameworks for:
  - NuScale SMR (generic design approval pathway underway)
  - Large reactors (existing precedent with Westinghouse, Combustion Engineering reactors)
- Licensing timelines: 5-7 years for new reactor type (prohibitive for Phase 1 2026-2033 window)
- Alternative designs (HTGRs, molten salt) require new regulatory evaluation (10-15 year timelines or longer)

#### Phase 1 Constraint: Commercially Insurable Systems Only

**Implication for Heber Campus Phase 1:**
- Nuclear: NuScale SMR only (4 units @ 77 MW each = 308 MW baseload)
- Electrolyzers: Established vendors (Cummins, ITM Power, Plug Power, or equivalent proven providers)
- Storage: Lithium-ion BESS (all-solid-state excluded per Delta 14 doctrine)
- Gas turbines: Proven industrial designs burning H₂ + ammonia blends (General Electric, Siemens, Mitsubishi)

**Operational Consequence:**
- Phase 1 energy system is fully locked-in to commercial vendor solutions
- No in-house reactors, no experimental electrolyzers, no prototype storage
- Technology risk is transferred to vendors via warranties and insurance

### SOEC Procurement Policy: Established Vendors Only in Phase 1

#### Procurement Rules

**Commercial SOEC Vendor Requirement**
- Definition: SOEC vendor must have deployed ≥3 commercial units of ≥100 kW capacity in production environments (NOT pilot, NOT demo, NOT lab)
- Required proof: Third-party operational documentation, customer references, available spare parts

**Approved Vendors (Example Candidates)**
- Plug Power (PEM electrolyzer focus; SOECs emerging)
- ITM Power (alkaline + PEM; SOEC partnerships)
- Cummins (acquiring SOEC vendors; ramp toward production)
- Silyzer (Siemens subsidiary; PEM focus, SOEC development)

**Excluded from Phase 1**
- Internal Heber Campus SOEC development (even if prototype-ready)
- University/research institution designs (no production experience)
- Start-up SOEC companies (insufficient operational history to satisfy insurance requirements)
- Chinese vendors (regulatory/political exposure for US project financing)

#### Rationale: Risk Transfer & Operational Maturity

**Why Exclude Internal SOEC Design?**
1. **Insurance Uninsurable:** Underwriters will not accept proprietary unknown-performance electrolyzer design
2. **Lender Non-Bankable:** Development bank or commercial lender will not finance project where core equipment has no third-party proven operation
3. **Warranty/Spares Unavailable:** No external vendor means no commercial warranty period or spare parts supply chain
4. **Operational Risk Unacceptable:** If internal SOEC design fails unexpectedly (stack degradation, thermal shock, contamination), no vendor support available to recover operations

**Example Scenario (Why This Matters):**
- If Heber Campus deploys internally-developed SOEC in Phase 1 and stack suffers delamination failure at month 6:
  - No vendor warranty covers the failure
  - No spare stack units available for immediate swap
  - Internal R&D team must diagnose and redesign on the fly
  - Project H₂ production halts for weeks/months
  - Tenants in data center experience load curtailment
  - Refinery production offline; revenue loss cascades
  - **Result:** Lender defaults project or demands operational guarantees site cannot meet

### Internal SOEC R&D: Phase 2+ Development Track

#### Parallel Development Authorization

**Phase 2+ Internal SOEC Program (Separate from Phase 1 Production)**
- **Authorization:** Heber Campus may conduct internal SOEC stack development during Phase 2 operations
- **Objective:** Develop proprietary SOEC design targeting Phase 3 capabilities (higher temperature, longer life, lower cost)
- **Constraints:**
  - Internal R&D does NOT contribute to Phase 1 H₂ production targets
  - Internal R&D does NOT replace commercial SOEC capacity (commercial units remain primary)
  - Parallel operation allowed: Internal test module (10-50 kW scale) running alongside commercial production fleet

#### Validation Path: Third-Party Testing Requirement

**Before Internal SOEC Can Replace Commercial Units:**
1. **Operating Hours Accumulation:** Internal design must accumulate ≥5,000 hours in test loop without major failures
2. **Third-Party Validation:** Independent engineering firm (not Heber Campus, not design team) must:
   - Audit design (thermodynamics, materials, design margins)
   - Witness full 5,000-hour test run
   - Publish validation report
3. **Insurance Assessment:** Underwriter must reassess SOEC design for insurability (may still decline even after validation)
4. **Pilot Deployment:** Even after validation, initial commercial deployment limited to 10-25% of H₂ production capacity (risk-limited rollout)

**Consequence:** Internal SOEC cannot displace commercial units until Phase 3 at earliest, and only if all validation gates passed

### Campus-Wide DC Main Bus Architecture: Long-Term Design Requirement

#### Definition & Functional Purpose

**DC Main Bus Concept:**
- High-voltage DC backbone (±400 kV or ±500 kV estimated) connecting:
  - Nuclear reactor primary power output
  - Solar farm DC output (1.5 GW cumulative Phase 1-2)
  - BESS DC side
  - Electrolyzer DC input
  - Data center DC server load
  - Power export converter (to AC grid via HVDC converter station)

**Advantages of DC Main Bus:**
1. **Direct Coupling Efficiency:** Eliminates AC power stage conversion losses (3-5% typical per conversion)
2. **Fast Transient Response:** DC-coupled systems respond faster to voltage/frequency disturbances than AC-coupled
3. **Converter Cost Reduction:** Fewer power electronics stages = lower capital cost and higher reliability
4. **Energy Arbitrage Optimization:** Direct DC coupling of storage + electrolyzer + load allows real-time optimization without AC grid losses

**Example Energy Flow (Midday Peak):**
```
Solar 1.5 GW DC output
  → BESS (charge surplus: 500 MW if available)
  → Electrolyzer (primary: 450 MW nominal → 457 t/day H₂)
  → Data center DC load (100-150 MW)
  → Export to AC grid via HVDC station (remainder)
  → NO intermediate AC conversion steps
```

**Typical AC Architecture (Comparison - Inefficient):**
```
Solar → DC/AC inverter (2% loss) → AC bus → AC/DC for storage (2% loss) → 
AC/DC for electrolyzer (2% loss) → AC/DC for data center (2% loss) →  
AC/DC export converter (2% loss) = 10% total cascade loss
```

#### Implementation Timeline

**Phase 1 (2026-2033):**
- DC main bus designed and committed to but NOT fully deployed
- Partial DC coupling: Solar DC → BESS DC side (avoids inverter). Reactor still AC output (legacy)
- Planning reserve: All future equipment specified as DC-compatible (future retrofit ease)

**Phase 2 (2033-2040):**
- Reactor upgrade or new SMR reactor designed with native DC output option
- DC main bus backbone fully constructed (cabling, switchgear, HVDC stations)
- Solar output directly DC-coupled
- SOEC electrolyzer has DC input directly connected (no AC/DC conversion)

**Phase 3 (2040+):**
- Multiple reactors/SOEC/storage all native DC-coupled
- Full DC main bus operational at multi-GW capacity
- Enables orbital/off-world system replication

### DC Main Bus as Portability Requirement: Off-World & Orbital Deployment

#### Market Background: Orbital Ascent Demand

**Future Scenario (2040-2080):**
- LEO (Low Earth Orbit) infrastructure demand grows exponentially (communications, manufacturing, tourism, resource extraction)
- Orbital industrial park concept: Large platforms in LEO supporting manufacturing, refining, power generation
- **Energy requirement:** Orbital platforms need compact power sources + processing equipment
- **Chemical fuel advantage:** Synthetic fuels (H₂, methane, LOX/LH2) enable propellant supply chains; essential for space vehicles

#### Heber Campus as Prototype for Orbital Deployment

**DC Bus Portability Requirement:**
- Design Heber Campus with DC power architecture matching potential orbital platform design
- Modularize DC coupling interfaces so they can be replicated in orbital/off-world contexts
- Example: If Heber uses ±400 kV DC standard, orbital platform inherits same voltage standard (reduces custom converters)

**Orbital Deployment Implication (Future):**
- Lunar base power system: Solar + electrolyzer + SOEC + storage all DC-coupled (replicating Heber model)
- Mars base power system: Nuclear + solar + SOEC, all DC-coupled, using Heber design library
- Orbital manufacturing platform: Power/process architecture duplicates Heber scaling

**Why This Matters:**
- Simplifies orbital engineering by reusing proven terrestrial designs
- Reduces development cost for space-based industrial systems
- Creates export market for Heber-proven power architectures (lunar equipment sales, Mars base contracts)

### Phase 3 Nuclear Scaling: Mixed-Reactor Strategy

#### Current Phase 1 Design (SMR-Only)

**Phase 1 Nuclear Deployment:**
- 4 × NuScale SMR @ 77 MW each = 308 MW total electric
- Advantage: Modular, proven, lower financing risk
- Disadvantage: Higher per-MW capital cost; higher staffing/O&M overhead for 4 units vs. 1 large reactor

#### Phase 3 Strategy Shift: Mixed Reactor Model

**Phase 3 Nuclear Mix (Planning)**
- Replace 4 SMRs with:
  - **1 × Large Gen III+ Reactor** (1,200 MW class, e.g., Westinghouse AP1000)
  - **2 × SMR** (154 MW combined, backup/peak shaving)
  - **Total: 1,354 MW electric** vs. 308 MW Phase 1 (4.4x increase)

**Operational Rationale:**

1. **Reduced Outage Risk via Redundancy**
   - Phase 1 with 4 SMRs: Outage of 1 unit = 25% power loss
   - Phase 3 with 1 large + 2 SMRs: Large reactor outage = 88% loss BUT occurs ~1x per 30 years (planned maintenance every 18 months, 4-week duration). SMR outage = 7% loss (tolerable from battery/peaking)
   - **Net effect:** Large reactor outage is rarer but more severe; SMRs provide backup capacity to ride through large planned maintenance

2. **Maintenance Complexity Reduction**
   - Phase 1: 4 separate control rooms, 4 separate security perimeters, 4 separate containment buildings = 4x staffing overhead
   - Phase 3 with 1+2 mix: 1 control room operators primary fleet, SMRs secondary staff = ~2.5x staffing (scaled down)

3. **Capital Cost Efficiency (Scaled Deployment)**
   - SMR capital cost: ~$6-8B per 308 MW (Phase 1 baseline)
   - Large reactor capital cost: ~$12-15B per 1,200 MW (~$10-12.5M per MW)
   - Large reactor LCOE becomes competitive with SMRs at multi-GW scale due to economies of scale

#### Contingency: Large Reactor Deferred Until Phase 3

**Phase 3 Deployment Gate (Conditional)**
Large reactor is authorized for Phase 3 ONLY if:
1. **Storage Capacity Established:** Phase 2 BESS or alternative storage (500+ MWh confirmed operational)
2. **Hydrogen Storage Capacity Confirmed:** H₂ tank farm (40,000+ t capacity established; enables multi-day load carry-over)
3. **Load-Following Capability Proven:** SOEC demonstrated to modulate output to follow variable load (70-75% of average target per HC-PH2-001)

**Rationale for Contingency:**
- Large reactor cannot ramp quickly (nuclear plants designed for baseload, ~5% per minute ramp rate maximum)
- If storage or SOEC cannot cover transient load swings, large reactor cannot balance grid
- Phase 3 deployment gated on proof that load-following infrastructure is in place

### Electrolyzer Capacity Scaling: Modular Plant-Train Architecture

#### Definition: Plant-Train Modular Unit

**Plant-Train Concept:**
- Functional unit = 50-100 MW electrolyzer capacity (estimated)
- Comprises: Electrolyzer stacks (15-25 MW each), water processing, oxygen separation, hydrogen compression, thermal management as single packaged system
- Can be manufactured off-site, shipped to campus, connected via standardized DC/water/gas interfaces

**Advantages of Plant-Train Modularity:**
1. **Factory Manufacturing:** Each plant-train built in controlled factory environment (higher quality control than site-built)
2. **Parallel Deployment:** Multiple plant-trains can be shipped/installed simultaneously (faster ramp vs. single monolithic system)
3. **Redundancy:** If 1 plant-train fails, other trains continue (N-1 resilience)
4. **Scaling Simplicity:** Phase 1 = 4-5 plant-trains; Phase 2 = 6-8 trains; Phase 3 = 10-15 trains (simply add identical units)
5. **Obsolescence Management:** Older plant-train can be retired and replaced with newer design without stopping entire system

**Example Scaling Path:**
- Phase 1 (457 t/day H₂): 4-5 × 100 MW plant-trains (400-500 MW SOEC capacity, 10-15% downtime reserve)
- Phase 2 (same 457 t/day): Same 4-5 trains maintained, reduced utilization during low-demand periods
- Phase 3 (1,500 t/day H₂): Add 10-15 new plant-trains of same modular design (legacy units retired or repurposed)

#### Contrast: Rejected Monolithic Architecture

**Monolithic Single-Stack Approach (Rejected):**
- 500-1,000 MW electrolyzer with single-location stacks
- Advantages: Simplified control, single vendor interface
- Disadvantages:
  - Factory capacity bottleneck (no single vendor produces >200 MW SOEC units today)
  - Site-of-failure risk (single failure halts entire H₂ production)
  - Inflexible scaling (cannot add capacity without major redesign)
  - Thermal management complexity at gigawatt scale
  - **Decision:** Plant-train modular approach is mandatory for Phase 1+ deployment

### SMR Unit Count Reduction at Multi-Gigawatt Scale

#### Strategic Objective: Staffing & Complexity Reduction

**Current Phase 1: 4 SMR Units**
- Staffing: ~80-100 personnel (operators, maintenance, security, health physics)
- Control rooms: 4 (one per unit)
- Containment buildings: 4
- Annual O&M cost: ~$30-40M estimated

**Target Phase 3: 2 SMR Units (in mixed architecture with large reactor)**
- Staffing: ~50-60 personnel (large reactor primary, SMRs secondary support)
- Control rooms: 1.5 (large reactor primary, SMRs secondary/shared)
- Containment buildings: 3 (large reactor + 2 SMRs)
- Annual O&M cost: ~$25-35M (lower per MW due to large reactor efficiency)

#### Complexity Reduction Strategy

**Staffing Reduction Tactics:**
1. **Consolidated Control Rooms:** Large reactor serves as control center; SMRs operated as secondary load-following units from single control point
2. **Shared Support Functions:** Maintenance teams, health physics, security consolidated under single organizational structure (vs. 4 independent teams)
3. **Simplified Security Perimeter:** 2-3 large containment buildings easier to secure than 4 separate SMR silos
4. **Predictive Maintenance:** Instrumentation of large reactor + SMR fleet allows predictive maintenance scheduling (reduces unplanned downtime)

**Consequence: Lower Total Cost of Ownership**
- Phase 3 nuclear fleet (1,354 MW) costs less per MW to operate than Phase 1 fleet (308 MW) due to economies of scale
- Enables Phase 3 H₂ production cost to reach <$2.50/kg target (lower steam cost, lower O&M allocation per kg)

---

## DC Fault Protection Autonomy, Hardware-Enforced Clearing & Software Prohibition (2026-02-08)

### Hardware-Enforced Autonomous Fault Detection & Interruption

#### Rationale: Microsecond Clearing Requirement

**DC System Fault Propagation Dynamics**
- DC arc faults develop with energy dissipation rates orders of magnitude faster than AC systems
- DC arc temperature: >6,000 K (copper vaporization), terminal erosion within ~1 millisecond for high-energy faults
- **Arc self-extinguishing behavior:** Unlike AC systems (zero-crossing natural commutation), DC arcs sustain and continue energy transfer until current supply physically interrupted
- **Propagation timescale:** Fault initiation → peak current ramp in ~10-100 microseconds
- **Software response time:** Best-case MECSAI fault detection (microprocessor sampling + logic) = 1-5 milliseconds minimum
- **DC fault clearing window:** Hardware devices must clear in <100 microseconds to prevent arc propagation to adjacent equipment

**Consequence:** Any software-participated fault clearing introduces unacceptable delay. Hardware-only autonomous clearing is non-negotiable.

#### Hardware Protection Device Requirements

**Solid-State Circuit Breaker (SSCB) Specification**
- **Topology:** Power semiconductor switch (MOSFET or IGBT) in series with sensing circuit
- **Clearing Time Target:** <10 microseconds from fault detection to gate command cessation
- **Current Rating:** Device-specific (10 kA to 100+ kA depending on location)
- **Voltage Rating:** Full DC bus voltage (±400-500 kV backbone, ±48 V distributed DC)
- **Manufacturer Examples:** Littelfuse, ABB, Siemens, Vicor (emerging SSCBs for multi-kV DC)

**Hybrid Electromechanical Breaker Alternative**
- Solid-state primary (microsecond sensing + gate switching) backed by mechanical breaker (interrupts high fault currents when SSCB begins saturation)
- Mechanical stage provides "second strike" for sustained faults
- Faster than mechanical-only (~1 ms typical) but slower than pure SSCB; acceptable if SSCB stage clears initial arc energy

**Protection Device Locations (Mandatory)**

1. **Device Level (Distributed DC Bus)**
   - Each inverter, rectifier, solar string combiner: Local SSCB
   - Each electrolyzer module: Input SSCB + hydrogen/oxygen compartment SSCBs
   - Each data center rack: PDU SSCB protecting 48 V distribution
   - **Purpose:** Prevent single-device fault from cascading to zone or backbone

2. **Zone Level (Medium-Voltage DC Distribution)**
   - Between solar farm and main DC bus: SSCB or hybrid breaker
   - Between battery pack and main DC bus: SSCB or hybrid breaker
   - Between electrolyzer plant and main DC bus: SSCB or hybrid breaker
   - Between data center DC distribution and main DC bus: SSCB or hybrid breaker
   - **Purpose:** Isolate subsystem-wide faults from propagating to backbone

3. **Backbone Level (High-Voltage DC Transmission)**
   - Main ±400 kV DC trunk line: High-rupture-capacity hybrid breakers or HVDC circuit breakers
   - Export HVDC converter input: SSCB or DC-rated breaker
   - SMR reactor DC output: SSCB before main bus coupling
   - **Purpose:** Protect entire campus power system and external grid connection

#### Autonomous Detection Hardware (Non-Programmable Analog Circuits)

**Fault Current Comparison (Differential Relay Logic)**
- Analog current sensors (rogowski coil, Hall-effect) on supply and load sides of each protection device
- Differential comparator (non-programmable analog circuit, no software): If load-side current exceeds supply-side by >threshold (typically 20-30% overage), fault condition declared
- Threshold setting is fixed at manufacturing time (cannot be changed in field without hardware replacement)

**Arc Voltage Detection (Arc Signature Recognition)**
- High-frequency voltage oscillation during arc fault (~100-500 kHz harmonic content typical)
- Bandpass filter circuit tuned to arc frequency signature → rectified signal → threshold comparator
- No microprocessor involvement; pure analog circuit detecting characteristic arc waveform and triggering gate command

**Temperature & Fiber-Optic Sensing (Secondary Confirmation)**
- Temperature sensors (RTD or thermocouple) at protection device location
- Excessive local heat (>100°C ambient) within breaker triggers backup isolation
- Fiber-optic current transducers (immune to EMI) provide redundant fault signature
- **Redundancy:** Any two of three detection methods (differential current, arc voltage, temperature) can independently trigger clearing

### MECSAI Functional Redesignation: Read-Only Monitoring & Analytics Only

#### Permitted Functions After Delta 17

1. **Monitoring:** Real-time observation of all fault events (SSCB trip signals, arc detection triggers)
2. **Analytics:** Aggregation of fault statistics (fault rate per zone, seasonal trends, correlation with load patterns)
3. **Reporting:** Dashboard visualization of protection device health, predicted maintenance scheduling
4. **Trend Analysis:** Machine learning on historical fault data to identify emerging failure patterns (arc frequency increase = aging equipment signal)

#### Explicitly Prohibited Functions

1. **Breaker Commands:** MECSAI cannot issue "close breaker" or "open breaker" commands to any protection device
2. **Override Authority:** MECSAI cannot override hardware fault lockouts (e.g., "allow SSCB to re-close even though fault signature detected")
3. **Reset Functions:** Cannot reset protection device latches or clear fault memory without manual technician action
4. **Automatic Reclosure:** Cannot initiate automatic breaker re-closure after fault clearing (prevents repeated arc formation if fault persists)

**Operational Consequence:**
- After SSCB clears fault, zone/device remains de-energized until manual field technician inspects and resets breaker
- Data center cannot automatically restart rack after fault (requires ticket + physical visit)
- Electrolyzer cannot auto-restart module after high-current event (requires technician diagnosis)
- Site remains in "safe" de-energized state until human verification of fault resolution

### SCADA Role Redesignation: Read-Only Observers for Fault Events

#### SCADA Permitted Functions

1. **Fault Event Logging:** Capture timestamp, device location, fault type, SSCB clearing time from protection relay telemetry
2. **Status Indication:** Display breaker state (open/closed) and fault counter from devices (not state command authority)
3. **Alarms:** Generate operator notifications when fault rate exceeds threshold (e.g., >5 faults/hour indicates equipment degradation)
4. **Historical Data:** Archive all fault events for compliance logging and equipment warranty analysis

#### SCADA Explicitly Prohibited

1. **Automatic Resets:** Cannot command protection device to re-close breaker
2. **Voltage/Frequency Control:** Cannot adjust setpoints on analog protection circuits
3. **Load Shedding:** Cannot shed customer loads in response to fault events (previously SCADA capability)
4. **Generation Control:** Cannot ramp generators up/down in reaction to detected faults

**Consequence:** Faults are logged and reported in real-time to operators, but system response is passive (no automated mitigation). Operators must manually intervene for recovery.

### Fault Clearing Interaction with Load-Shedding (Clarification)

#### New Load-Shedding Paradigm (Post-Delta 17)

**Hypothetical Night Shortage Scenario:**
- Solar unavailable; BESS depleted to 10% capacity; SMR #1 down for maintenance
- MECSAI predicts insufficient capacity in 30 minutes to supply 500 MW demand

**Available Options (All Voluntary, No Hardware Override):**
1. **Operator discretion:** Manually request electrolyzer operator to ramp module #3 offline (voluntary, not automatic)
2. **Tenant coordination:** Call data center customer support; negotiate temporary workload deferral (contractual discussion, not forced shutdown)
3. **Import power:** Request grid operator to supply 100 MW from external market (economic, not technical control)

**Not Available:**
- MECSAI cannot force breaker open to shed load
- MECSAI cannot override tenant SLA by shutting down their racks
- MECSAI cannot prevent electrolyzer restart by locking protection device

**Consequence:** Night shortage management becomes a planning + negotiation problem, not a real-time automated control solution

### Fault Isolation Architecture: Three-Level Protection Hierarchy

#### Level 1: Device Protection (Microsecond Scale)
- Fault confined to single device (inverter, battery pack, electrolyzer module)
- SSCB clears; only that device de-energized
- Rest of system unaffected
- Example: Solar string fault → only that combiner de-energized; other 99 strings continue

#### Level 2: Zone Protection (Microsecond Scale, Higher Current Rating)
- Device-level protection fails (SSCB stuck ON due to gate drive failure)
- Zone protection picks up; higher current SSCB actuates
- Entire zone (e.g., solar farm) isolated; backup zones (battery, reactor) supply campus
- Example: Combiner stuck closed, arc propagates to feeder line → zone SSCB clears feeder; solar farm isolated but site continues operation

#### Level 3: Backbone Protection (>10 ms Timescale, Highest Current Rating)
- Zone protection fails
- Main backbone HVDC breaker/HVDC circuit breaker actuates
- Entire campus splits into isolated sections; each section operates on local generation/storage
- Example: Multi-zone arc propagates to main bus → backbone breaker opens; north campus (reactor #1 + battery) and south campus (reactor #2 + solar) operate independently

#### Redundancy Requirement

**Mandatory Dual Protection:**
- Every wire, bus, and cable must have ≥2 independent protection devices
- If SSCB #1 fails (gate drive shorted, MOSFET failure), SSCB #2 is independent backup
- Sensing circuit for device #2 is completely independent (separate analog comparator, separate current sensor)
- **Cannot share analog sensing or signal conditioning** (failure mode correlation)

**Maintenance Implication:**
- After fault clearing, only one protection device can be off-line for repair at a time
- Second protection device must be verified operational before first device is returned to service
- Staffing requirement: Technicians trained in dual-device coordination procedure

### Manufacturing Standards & Certification Requirement

**SSCB Acceptance Criteria:**
1. **Third-party shortcircuit testing:** Device must withstand rated shortcircuit current (10 kA, 50 kA, 100 kA class) without component failure
2. **Clearing time validation:** Independent lab test confirmation of <10 μs clearing time under rated shortcircuit
3. **Repeatability:** Device must clear ≥1,000 consecutive shortcircuits without performance degradation
4. **Temperature cycling:** Thermal cycling -40°C to +85°C over 500 cycles; clearing time specification maintained
5. **Qualification to IEC 61008 (DC Switching) or IEEE C37.14** (DC circuit breaker standards)

**Supply Chain Impact:**
- Cost: SSCB ~$50-200 per unit depending on current rating (vs. $10-20 for AC breaker)
- Availability: SSCB production capacity globally is <5 GW equivalent capacity/year; Heber demand for 1.5+ GW DC system represents 20-30% of global SSCB market
- Lead time: 12-18 months for delivery of purpose-designed SSCB fleet

**Phase 1 Implication:** Campus DC protection specification must be finalized by 2026 Q2 (this month) to meet 2027-2028 construction timelines

---

## HeberCampus VM Extract — Steam & SOEC Water Chemistry, Vendor Doctrine, and Execution Constraints (2026-02-08 23:59 UTC)

**Source:** VM_DELTA_HeberCampus_VMExtract_20260208-2359.md

[2026-02-08] Formal acceptance standard for steam and SOEC-grade water chemistry established as procurement, FAT/SAT, insurer, and warranty gate; chemistry limits, sampling locations, materials compatibility, corrosion monitoring, and enforcement language defined.

[2026-02-08] Vendor compliance checklist doctrine established requiring modular scalability from Phase 1 through Phase 3 without chemistry envelope change, system redesign, or warranty reset; applies to SOEC systems and balance-of-plant.

[2026-02-08] Water purification vendors formally bound to modular Phase 1–Phase 3 expansion doctrine; purification systems required to scale via modular skid replication while maintaining SOEC-grade outlet chemistry and warranty continuity.

[2026-02-08] Explicit separation doctrine reinforced: VM extraction and canonical governance operations must be executed in retrieval-only context; file-generation and sandboxed execution contexts are non-authoritative for VM mutation.

[2026-02-08] Execution constraint acknowledged: sandboxed file-generation sessions are non-authoritative for external canonical retrieval; governance process requires isolation of VM extraction from document generation workflows.

---

## Hybrid Architecture, Project Isolation & Governance Spine Doctrines (2026-02-08)

**Source:** VM_DELTA_HCV-VM-EXTRACT-002_20260209-0120.md

[2026-02-08] Canonical governance decision ratified establishing a Hybrid Architecture for project execution: a shared platform sandbox (SE_T1) for agents, templates, and tooling, with fully isolated per-project tenant roots for all client and project data, artifacts, and governance files.

[2026-02-08] Project onboarding pipeline formally adopted as a canonical operational doctrine, defining deterministic intake, validation, provisioning, execution, validation, release, and closeout phases, with no cross-project data access permitted at any stage.

[2026-02-08] Mandatory project identifier format formalized as PRJ-<CLIENT_SLUG>-<YYYY>-<NNNN>, enforced at intake and provisioning layers to prevent cross-project collision and enable deterministic routing, auditing, and archival.

[2026-02-08] Router authority formally designated as the sole component authorized to provision project tenants, create canonical governance artifacts (CTX, PRI, MANIFEST), apply access controls, generate cryptographic hashes, and emit PROJECT_READY lifecycle events.

[2026-02-08] Governance spine doctrine formalized requiring every project to instantiate three canonical artifacts at provisioning: Context Anchor (CTX), Project Reference Index (PRI), and Machine Manifest, with all subsequent execution bound to these artifacts.

[2026-02-08] Schema-per-project database isolation adopted as the default operational mode, with explicit allowance for database-per-project escalation for high-risk or high-sensitivity projects; mandatory project_id scoping enforced on all retrieval and write operations.

[2026-02-08] Risk-based validation gates codified requiring mandatory Agent R security validation for all projects classified as HIGH or CRITICAL risk prior to provisioning or execution.

[2026-02-08] Emergency project control doctrine established authorizing immediate PAUSE, FREEZE, or TERMINATE actions at the Router level to halt execution, preserve state, or initiate controlled shutdown in response to security, scope, or client-driven events.

[2026-02-08] Canonical JSON schema contracts ratified for project intake, project provisioning request, provisioning response, and project-ready event payloads, establishing machine-verifiable governance interfaces between orchestration, routing, and agent execution layers.

[2026-02-08] Operational separation rule reinforced: VM extraction, governance validation, and canonical memory mutation are retrieval-only activities and must remain isolated from sandboxed generation or execution environments.

---

## Green Compliance, Fuel Quality & Lifecycle Carbon Doctrine (2026-02-09)

**Source:** VM_DELTA_HCV-VM-EXTRACT-002_20260209-0715.md

[2026-02-09] Campus fuel production doctrine includes lifecycle net-zero carbon claim only if carbon feedstock is biogenic or air-captured CO2 and the energy inputs are low-carbon, requiring formal lifecycle accounting boundaries for validation.

[2026-02-09] Campus synthetic fuels (FT liquids) design must include aggressive syngas cleanup to achieve very low sulfur content meeting ULSD and Jet-A sulfur specifications.

[2026-02-09] A "Green Compliance and Fuel Quality Doctrine" addendum is required to lock allowed carbon sources (biogenic, DAC), limits on external fossil CO2 makeup, and sulfur spec targets with required analyzers/COAs for acceptance.

---

## CO2 Capture Integration, DAC Sizing & Carbon Tiering Doctrine (2026-02-09)

**Source:** VM_DELTA_CO2_CAPTURE_INTEGRATION_20260209-1045.md

[2026-02-09] Determined that biomass gasification alone cannot reliably supply required carbon for 18,000 bpd synthetic fuel production under all operating conditions.

[2026-02-09] Established that supplemental CO2 capture is structurally required to maintain 110 percent carbon availability as mandated by HC-MGD-001.

[2026-02-09] Defined Direct Air Capture (DAC) as the only non-fossil pathway capable of closing the projected carbon shortfall at Heber Campus scale.

[2026-02-09] Set engineering planning basis for supplemental CO2 capacity at approximately 1,500 to 3,000 metric tons per day.

[2026-02-09] Formally designated DAC systems as process utilities, not revenue-generating assets, within campus architecture.

[2026-02-09] Established carbon capture tiering doctrine: biomass gasification as primary carbon source, DAC as makeup carbon, flue-gas capture as optimization layer.

[2026-02-09] Accepted industrial-scale DAC architectures (liquid solvent class) as baseload-capable; rejected small-scale or pilot-only DAC systems as insufficient for primary makeup duty.

[2026-02-09] Mandated that external CO2 systems shall not become single points of failure and shall not dictate upstream process design.

[2026-02-09] Locked requirement that DAC and CO2 capture loads be dispatchable based on internal power availability and not constrain primary energy systems.

---

## Space R&D Charter, OSY Manufacturing & Microgravity Engineering Doctrine (2026-02-09)

**Source:** VM_DELTA_HCV-VM-EXTRACT-002_20260209-1420.md

[2026-02-09] R&D scope expanded beyond efficiency and safety optimization to include generative engineering of non-existent infrastructure required for space and orbital operations.

[2026-02-09] R&D charter includes invention of new materials, coatings, joining methods, and manufacturing processes with no terrestrial equivalents.

[2026-02-09] Purpose-built robotic systems for microgravity manufacturing are designated as core R&D outputs, not derivative adaptations of terrestrial automation.

[2026-02-09] Microgravity manufacturing defined as a first-principles engineering domain; gravity-dependent processes are considered non-viable by default for OSY deployment.

[2026-02-09] Orbital Shipyard (OSY) designated as heavy vehicle manufacturing environment requiring space-native manufacturing architectures developed through R&D.

[2026-02-09] Heber Campus designated as ground-truth validation environment for space infrastructure R&D, including materials, robotics, coatings, and manufacturing physics prior to orbital deployment.

---

## Holbrook Ranch Dual-Campus Strategy & Acquisition Doctrine (2026-02-09)

**Source:** VM_DELTA_HOLBROOK_DUAL_CAMPUS_20260209-1510.md

[2026-02-09] Holbrook Ranch identified as a viable secondary campus capable of full duplication of Heber Campus core functions, including energy generation, fuels production, fertilizer production, data centers, and R&D, contingent on water and rights verification.

[2026-02-09] Holbrook Ranch parcels totaling approximately 30,000+ acres confirmed as contiguous or adjacent and held under a single trust ownership, materially reducing land assembly risk and enabling unified industrial zoning.

[2026-02-09] Active rail right-of-way crossing Holbrook Ranch parcels confirmed as a strategic logistics asset enabling bulk inbound and outbound transport without third-party industrial park dependency.

[2026-02-09] Holbrook Ranch designated as a strategic fallback site to mitigate federal land (BLM/USFS) permitting risk associated with Heber Campus.

[2026-02-09] Governance position established that Holbrook Ranch may function as a peer campus rather than a satellite, with potential specialization toward fertilizer, bulk materials, biomass processing, and logistics-heavy operations.

[2026-02-09] Decision boundary defined for Holbrook Ranch acquisition: acquisition remains viable below an aggregate purchase price threshold of approximately $50–60M, assuming clean title, intact mineral rights, controlled rail access, and viable water rights.

[2026-02-09] Acquisition price bands defined as internal decision framework: strong-buy below ~$15M, acceptable with negotiation ~$15–30M, conditional ~$30–50M, no-go above ~$50M unless Heber Campus execution is materially constrained.

[2026-02-09] Strategic doctrine established that land price alone is not a disqualifier; loss of operational control, mineral rights, water access, or rail rights constitutes a hard no-go condition regardless of purchase price.

[2026-02-09] Dual-campus operating model formalized as enabling modular redundancy, phased replication, and market-driven specialization between Heber Campus and Holbrook Ranch.
