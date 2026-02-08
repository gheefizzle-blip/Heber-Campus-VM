# CORE_VM.md

**Last Updated:** 2026-02-07 23:59  
**VM_VERSION:** 20260207-2359  
**Status:** Delta applied - HCV-VM-EXTRACT-002 (Campus Master Planning v0.4)

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
