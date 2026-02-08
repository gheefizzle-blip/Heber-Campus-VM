# CORE_VM.md

**Last Updated:** 2026-02-07 23:17  
**VM_VERSION:** 20260207-2317  
**Status:** Delta applied - HCV-VM-EXTRACT-002 (Nuclear Pivot)

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
