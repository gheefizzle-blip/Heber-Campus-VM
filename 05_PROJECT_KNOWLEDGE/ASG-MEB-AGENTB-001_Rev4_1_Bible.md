# ATLAS SYSTEMS GROUP
# MASTER ENGINEERING BIBLE
## Revision 4.1 — Three-Loop Thermal Cascade Architecture
## HEBER INDUSTRIAL CAMPUS MASTER PLAN
### Integrated Nuclear-Electric Power, Synthetic Fuels & Data Center Operations

---

**Document Number:** ASG-MEB-AGENTB-001  
**Revision:** 4.1  
**Date:** 2026-01-30  
**Classification:** INTERNAL / PROPRIETARY  
**Prepared By:** Agent B (Claude) — Validation Authority  
**SUPERSEDES:** Rev 4.0, Rev 3.0, Rev 2.1, Rev 2.0, Rev 1.0

---

## REVISION HISTORY

| Rev | Date | Description | Author |
|-----|------|-------------|--------|
| 1.0 | 2026-01-15 | Initial release — conceptual architecture | Agent B |
| 2.0 | 2026-01-20 | Thermal cascade integration, 7 volumes | Agent B |
| 2.1 | 2026-01-22 | High-resolution diagrams, print optimization | Agent B |
| 3.0 | 2026-01-28 | PFT modular architecture, 2x Xe-100 + FLiNaK salt loop | Agent B |
| 4.0 | 2026-01-29 | ALL-ELECTRIC ARCHITECTURE — Eliminated Xe-100/salt loop, LPG peakers added | Agent B |
| **4.1** | **2026-01-30** | **THREE-LOOP THERMAL CASCADE — WP-1 through WP-8 integration, freeze doctrine, constraint hierarchy, 50% night margin improvement** | **Agent B** |

### Rev 4.1 Change Summary

**Architecture Evolution:**
- Integrated WP-1 through WP-8 from Session 23 PFT architecture sprint
- Established canonical constraint hierarchy governing all operating modes
- Implemented three-loop thermal cascade with complete fluid separation
- Added four-layer freeze protection doctrine with 36" burial standard
- Defined three-stage steam generation (Economizer → Boiler → Electric Trim)

**Performance Improvements:**
- Night margin improved from +129 MWe to **+193 MWe** (50% improvement)
- Electric heater load reduced from 219 MWe to **140 MWe** (36% reduction)
- O₂ handling night load reduced from 40 MWe to **5 MWe** (88% reduction via mode shedding)
- LPG utilization path optimized: boiler-first yields +85 MWe vs turbine path

**New Content Added:**
- Vol 0: Canonical constraint hierarchy, doctrine statements, firm margin definition
- Vol I: Freeze protection doctrine, Loop B specifications, underground distribution
- Vol II: Three-tier BESS architecture (175/50/500 MWh), SOEC power electronics ICD
- Vol III: Three-loop thermal cascade, steam generation staging, HX cascade
- Vol V: O₂ system ICD with operating modes A/B/C/D
- Vol VI: LPG fuel closure accounting, BTU trade study framework
- Vol X: Underground distribution standard, valve vault requirements

---

## TABLE OF CONTENTS

1. [EXECUTIVE SUMMARY](#executive-summary)
2. [VOLUME 0: DESIGN BASIS & PHILOSOPHY](#volume-0-design-basis--philosophy)
3. [VOLUME I: WATER SYSTEMS](#volume-i-water-systems)
4. [VOLUME II: POWER SYSTEMS](#volume-ii-power-systems)
5. [VOLUME III: THERMAL CASCADE](#volume-iii-thermal-cascade)
6. [VOLUME IV: CARBON CAPTURE](#volume-iv-carbon-capture)
7. [VOLUME V: HYDROGEN & OXYGEN PRODUCTION](#volume-v-hydrogen--oxygen-production)
8. [VOLUME VI: FUEL SYNTHESIS](#volume-vi-fuel-synthesis)
9. [VOLUME VII: LOGISTICS](#volume-vii-logistics)
10. [VOLUME VIII: DATA CENTERS](#volume-viii-data-centers)
11. [VOLUME IX: CONTROL SYSTEMS & INTELLIGENCE](#volume-ix-control-systems--intelligence)
12. [VOLUME X: SITE INFRASTRUCTURE](#volume-x-site-infrastructure)
13. [APPENDICES](#appendices)

---

# EXECUTIVE SUMMARY

## Mission Statement

Atlas Systems Group will design, construct, and operate the Heber Industrial Campus — a fully integrated complex producing carbon-neutral synthetic fuels, clean hydrogen, and high-performance computing services, powered by nuclear baseload generation with renewable supplementation. The enterprise follows a 100-year roadmap from terrestrial proof-of-concept through orbital industrialization.

## Rev 4.1 Architecture Philosophy

The Three-Loop Thermal Cascade architecture represents the engineering maturation of the Rev 4.0 all-electric concept. By integrating recovered waste heat, LPG+O₂ boiler preheat, and electric trim heating in a staged approach, Rev 4.1 achieves significant improvements across all key metrics while establishing permanent doctrines for freeze protection, fluid separation, and operating hierarchy.

### Key Achievements

| Metric | Rev 4.0 | Rev 4.1 | Improvement |
|--------|---------|---------|-------------|
| Electric heater load | 219 MWe | **140 MWe** | -79 MWe (36% reduction) |
| O₂ handling (night) | 40 MWe | **5 MWe** | -35 MWe (88% reduction) |
| Total night load | 1,308 MWe | **1,194 MWe** | -114 MWe |
| Night margin | +129 MWe | **+193 MWe** | +64 MWe (50% improvement) |
| Steam generation | All-electric | Three-stage | Thermal efficiency gain |

### Architecture Principles (Locked)

1. **Three-Loop Fluid Separation** — Loops A, B, and C never mix; heat transfers via HX surfaces only
2. **Four-Layer Freeze Protection** — Circulation, segmentation, targeted heat trace, drainback
3. **36" Minimum Burial** — Exceeds 24" frost depth with margin for all underground distribution
4. **Constraint Hierarchy** — Pipe integrity and Loop B circulation are sacrosanct
5. **LPG Boiler-First** — Thermal displacement yields +85 MWe benefit vs turbine generation

## Ultimate Envelope (Full Buildout)

| Metric | Per PFT | Phase 3 (6 PFT) | Phase 4 (8 PFT) | Full Build (12 PFT) |
|--------|---------|-----------------|-----------------|---------------------|
| Nuclear Capacity | 1,100 MWe | 6,600 MWe | 8,800 MWe | 13,200 MWe |
| H₂ Production | 500 t/day | 3,000 t/day | 4,000 t/day | 6,000 t/day |
| Fuel Production | 13,812 BPD | 82,870 BPD | **110,500 BPD** | 165,750 BPD |
| Data Center IT Load | 120 MWe | 720 MWe | 960 MWe | 1,440 MWe |
| CO₂ Captured (DAC) | ~6,200 t/day | ~37,200 t/day | ~49,600 t/day | ~74,400 t/day |
| Night Margin | +193 MWe | +1,158 MWe | +1,544 MWe | +2,316 MWe |

**100,000 BPD milestone achieved at Phase 4 (8 PFT)**

## Three-Legged Revenue Model

The enterprise derives revenue from three synergistic streams:

| Revenue Stream | Primary Products | Market Position |
|----------------|------------------|-----------------|
| **Power Generation** | Nuclear baseload, solar, biomass, grid services | 24/7 carbon-free electricity |
| **Fuel Production** | ULSD, Jet-A/SAF, LPG | Drop-in carbon-neutral fuels |
| **Data Center Operations** | AI/ML compute, enterprise services | Nuclear-powered, carbon-negative compute |

The thermal integration between these streams creates operational efficiency unavailable to single-purpose facilities. Data center waste heat drives DAC regeneration. Nuclear power enables 24/7 hydrogen production. Carbon capture feeds fuel synthesis.

---

# VOLUME 0: DESIGN BASIS & PHILOSOPHY

## 0.1 Corporate Structure

Atlas Systems Group operates through seven specialized subsidiaries, each with clearly defined scope and accountability:

| Subsidiary | Function | Key Deliverables |
|------------|----------|------------------|
| **Helios Power** | Nuclear & renewable generation | AP1000 operations, solar arrays, biomass plant |
| **Prometheus Fuels** | Synthetic fuel production | Diesel, Jet-A/SAF, LPG via Fischer-Tropsch |
| **Hermes Data** | Data center operations | AI/ML compute, enterprise cloud services |
| **Poseidon Water** | Water treatment & recycling | SOEC feedwater, ZLD systems, aquifer management |
| **Hephaestus Robotics** | Automation & maintenance | Robotic inspection, predictive maintenance systems |
| **Athena Intelligence** | AI/ML & compliance platforms | MECSAI supervisory AI, AEGIS regulatory system |
| **Apollo Orbital** | Space systems (future phases) | Orbital manufacturing, communications networks |

## 0.2 Governance Framework

All operations are governed by SE-CONSTITUTION-001, which establishes:

**Non-Delegable Human Authorities:**
- Final decision power rests with Commander Gary Spear
- Liability-bearing decisions require human approval
- Regulatory filings and public statements require human sign-off
- Financial commitments above defined thresholds require human authorization

**Multi-Agent Validation Protocol (D-AVP-001):**
- Agent A (ChatGPT): Planning, drafting, strategic analysis
- Agent B (Claude): Independent validation, quality assurance
- Agent R (Grok): Adversarial review, assumption challenge
- Agent G (Gemini): Integration, cross-system verification
- Circular validation required: No agent validates its own work

**Document Hierarchy:**
```
SE-CONSTITUTION-001 (Constitutional Charter)
    ↓
Master Engineering Bible (This Document)
    ↓
Phase Doctrines & ICDs
    ↓
Work Packages & Specifications
    ↓
Work Orders & Execution Documents
```

## 0.3 Design Principles

The following principles govern all engineering decisions:

| Principle | Description | Application |
|-----------|-------------|-------------|
| **MODULAR** | Each PFT is identical, self-contained, independently operable | Enables phased construction, simplified training, spare parts commonality |
| **SIMPLICITY** | One reactor type, standard industrial equipment, proven technologies | Reduces complexity, accelerates licensing, improves reliability |
| **NO SHORTCUTS** | Full redundancy, conservative margins, complete engineering | Safety and reliability over schedule or cost optimization |
| **SAFETY FIRST** | NRC-certified reactor, passive safety systems, defense in depth | Human life and environmental protection are paramount |

## 0.4 Canonical Constraint Hierarchy ◄━━ LOCKED

*Source: ATLAS_CORE_Memory_v20.md Section 2 — Verbatim*

This hierarchy governs all operating modes and **overrides economic or optimization logic**:

```
┌─────────────────────────────────────────────────────────────┐
│  CANONICAL CONSTRAINT HIERARCHY — NON-NEGOTIABLE            │
├─────────────────────────────────────────────────────────────┤
│  1. PIPE INTEGRITY              ◄── NEVER COMPROMISED       │
│  2. LOOP B CIRCULATION          ◄── SACROSANCT              │
│  3. BIOMASS TEMPERATURE STABILIZATION                       │
│  4. O₂ HANDLING SHED                                        │
│  5. DAC REDUCTION                                           │
│  6. SOEC CURTAILMENT            ◄── LAST RESORT             │
└─────────────────────────────────────────────────────────────┘
```

**Nothing above Loop B circulation gets touched in winter mode.**

This hierarchy ensures that during any power shortfall, contingency, or emergency:
- Underground piping is protected from freeze damage (Priority 1)
- Loop B heat recovery continues circulating (Priority 2)
- Biomass provides temperature stabilization before load shedding begins (Priority 3)
- O₂ handling sheds first among flexible loads (Priority 4)
- DAC reduces before touching hydrogen production (Priority 5)
- SOEC curtailment is the absolute last resort (Priority 6)

## 0.5 Doctrine Statements ◄━━ CANON

*Source: Session_24_Quick_Start.md — Copied Verbatim*

These four doctrine statements are permanent architectural commitments:

### Doctrine 1: Three-Loop Separation Mandatory

> Thermal cascade uses three separated loops (A: DC internal, B: campus heat recovery, C: boiler feedwater/steam). Fluids never mix. Heat transfers via HX surfaces only.

**Rationale:** Fluid separation prevents contamination between vendor-controlled data center coolant, campus heat recovery water, and high-purity boiler feedwater. Each loop operates at optimal chemistry for its application.

### Doctrine 2: Constraint Hierarchy

> Winter mode hierarchy: Pipe integrity → Loop B circulation → Biomass stabilization → O₂ shed → DAC reduction → SOEC curtailment. Nothing above Loop B circulation gets touched.

**Rationale:** Freeze damage to underground piping would cause weeks of downtime and millions in repairs. The hierarchy protects physical infrastructure before shedding production loads.

### Doctrine 3: LPG Boiler Path Superior

> LPG+O₂ boiler displacing electric heating provides 85 MWe better net benefit than LPG turbines (120.7 MWe vs 35.8 MWe from same fuel). Retain turbines for emergency/black-start only.

**Rationale:** Direct thermal application of LPG avoids the ~35% efficiency loss inherent in combustion-to-electricity conversion. Every BTU of LPG that displaces an electric heater BTU saves more power than burning that LPG in a turbine would generate.

### Doctrine 4: Underground Distribution

> 36" minimum burial with pre-insulated factory-jacketed pipe. Four-layer freeze protection: circulation, segmentation, targeted heat trace, drainback.

**Rationale:** Factory-applied insulation with HDPE jackets provides consistent quality impossible to achieve with field-wrapped systems. Integrated leak detection enables early warning before failures escalate.

## 0.6 Firm Margin Definition

*Integrated from WP-3 ASG-PFT-WP3-OM-001 Rev A*

Firm margin is **not** simply the difference between generation capacity and load. Firm margin is the **dispatchable net power at the campus boundary under worst-case winter night conditions**.

### Firm Margin Satisfaction Criteria

Firm margin is satisfied when ALL of the following conditions are met:

1. All critical loads are powered (safety systems, control power, freeze protection)
2. Loop B circulation is maintained at minimum flow
3. Steam header is maintained above minimum temperature (no thermal shock risk)
4. BESS reserve state of charge is above minimum threshold
5. No SOEC thermal cycling is occurring (stacks at stable operating point)

### Firm Margin Calculation Conditions

Firm margin shall be calculated under:
- Worst-case winter night (no solar, minimum temperatures)
- No reliance on LPG turbines (emergency reserve only)
- Single contingency event (N-1 criterion on major equipment)
- BESS providing only transient support (not steady-state load balancing)

### Rev 4.1 Firm Margin Result

| Supply Source | Capacity (MWe) |
|---------------|----------------|
| AP1000 Nuclear | 1,100 |
| Tail Gas Turbine | 100 |
| Biomass (PFT share) | 167 |
| Boiler Steam Turbine | 20 |
| **TOTAL SUPPLY** | **1,387** |

| Load Component | Rev 4.0 (MWe) | Rev 4.1 (MWe) |
|----------------|---------------|---------------|
| Steam generation | 219 | **140** |
| O₂ handling | 40 | **5** |
| All other loads | 1,049 | 1,049 |
| **TOTAL LOAD** | **1,308** | **1,194** |

| Margin | Rev 4.0 | Rev 4.1 | Improvement |
|--------|---------|---------|-------------|
| **Night Margin** | +79 MWe | **+193 MWe** | **+144%** |

## 0.7 Operating Mode Framework

*Integrated from WP-3, WP-6*

The campus operates in four primary modes, with transitions managed by MECSAI:

### Day Mode (Solar Abundant)

- Solar generation active, excess power available
- O₂ handling at Mode A (full capture enabled)
- DAC fully active (maximum CO₂ capture)
- Electric trim heaters permitted at full duty
- BESS charging prioritized
- LPG boiler may idle (preserved for night)

### Evening Transition Mode

- Solar declining, power balance shifting
- O₂ handling transitions to Mode B (scheduled ramp-down)
- DAC begins controlled reduction
- Biomass heat comes online for Loop B stabilization
- Electric trim heaters begin ramp-down
- LPG boiler begins ramp-up
- **No reduction in Loop B circulation permitted**

### Night Mode (Winter)

- No solar contribution
- O₂ handling at Mode C (shed to 5 MWe)
- DAC at reduced capacity
- LPG boiler active at planned duty
- Electric trim at minimum (140 MWe)
- Biomass heat active as temperature stabilizer
- BESS reserved for contingencies only

### Contingency Mode

- Triggered by: generation trip, underfrequency, BESS reserve threat
- O₂ handling immediately to Mode D (emergency shed)
- Immediate PFT BESS discharge
- Campus BESS discharge if needed
- Electric trim reduced to warm standby
- SOEC curtailed only if reserves threatened
- **Loop B circulation maintained throughout**

---

# VOLUME I: WATER SYSTEMS

## 1.1 Water Requirements Overview

Water is a critical resource consumed across multiple campus systems:

| Use Category | Per PFT | Phase 3 (6 PFT) | Notes |
|--------------|---------|-----------------|-------|
| SOEC Feedwater | ~1.1 MGD | ~6.6 MGD | Ultra-pure <1 ppm TDS required |
| Cooling Makeup | ~0.5 MGD | ~3.0 MGD | Evaporative and blowdown losses |
| Process Water | ~0.2 MGD | ~1.2 MGD | Refinery, cleaning, misc. |
| Domestic | ~0.1 MGD | ~0.6 MGD | Potable, sanitary, safety showers |
| **GROSS TOTAL** | **~1.9 MGD** | **~11.4 MGD** | Before recycling |
| **NET (after recycle)** | **~1.3 MGD** | **~7.8 MGD** | 30-40% reduction |

## 1.2 Water Source — Coconino Aquifer

**Primary Source:** Coconino Aquifer (regional sandstone aquifer)

| Parameter | Specification |
|-----------|---------------|
| Aquifer Type | Confined sandstone |
| Depth to Water | 500-1,000 ft |
| Well Construction | Deep submersible pumps |
| Raw Water Quality | Moderate TDS, requires treatment |
| Sustainable Yield | Under hydrological study |
| Water Rights | Acquisition in progress (CRITICAL PATH) |

**Backup/Supplemental:** Treated effluent from nearby municipalities (under evaluation)

## 1.3 Water Treatment Train

Raw aquifer water requires multi-stage treatment to meet SOEC feedwater specifications:

```
Raw Water Intake
    ↓
Coarse Filtration (sand, particulates)
    ↓
Softening (calcium, magnesium removal)
    ↓
Reverse Osmosis (TDS reduction)
    ↓
Deionization (polish to <1 ppm TDS)
    ↓
Degasification (dissolved gas removal)
    ↓
Storage (ultra-pure water tank)
    ↓
SOEC Feedwater Supply
```

**Output Quality Specification:** <1 ppm TDS (required for SOEC stack longevity)

## 1.4 Water Recycling Strategy

Multiple streams are recovered and recycled to minimize net water consumption:

| Recovery Stream | Source | Treatment | Destination |
|-----------------|--------|-----------|-------------|
| FT Reaction Water | Fischer-Tropsch reactor | Condensation, polishing | SOEC feed (~30% of requirement) |
| RWGS Reaction Water | Reverse water-gas shift | Condensation, recycling | Process water |
| Cooling Blowdown | Cooling towers | Treatment, concentration | Recycled or ZLD |
| Steam Condensate | Steam systems | Deaeration, polishing | Boiler feedwater |
| DC Cooling | Data center loops | Closed loop, makeup only | Recirculated |

**Zero Liquid Discharge (ZLD):** Brine crystallizers concentrate final reject streams to solid salts for disposal. No liquid discharge to environment.

## 1.5 Three-Loop Water/Heat Architecture ◄━━ LOCKED

*Integrated from WP-8 ASG-PFT-WP8-ICD-001 Rev B*

The campus water and heat distribution uses three physically isolated loops:

### Loop A: Data Center Internal Cooling

| Parameter | Specification |
|-----------|---------------|
| Purpose | Remove heat from IT equipment |
| Fluid | Vendor-controlled chemistry (typically glycol or proprietary) |
| Supply Temperature | 30-45°C |
| Return Temperature | 50-65°C |
| Ownership | Data center vendor (Hermes Data) |
| Interface | Heat exchanger HX-DC to Loop B |

**Loop A is electrically and hydraulically isolated from campus systems.** Atlas does not control Loop A chemistry or operations — only receives heat via HX-DC.

### Loop B: Campus Heat Recovery Loop

| Parameter | Specification |
|-----------|---------------|
| Purpose | Move recovered heat between systems |
| Fluid | Treated water with corrosion inhibitors |
| Supply Temperature | 30°C (nominal) |
| Return Temperature | 70-110°C (load dependent) |
| Distribution | Underground pre-insulated mains |
| Key Interfaces | HX-DC (from DC), HX-BIOMASS (from biomass), HX-DAC (to DAC), HX-ECO (to BFW) |

**Loop B is the campus thermal backbone.** It collects waste heat from data centers, accepts temperature lift from biomass, and delivers heat to DAC regeneration and boiler feedwater preheat.

### Loop C: Boiler Feedwater and Steam

| Parameter | Specification |
|-----------|---------------|
| Purpose | Generate 800°C steam for SOEC |
| Fluid | High-purity deaerated water / superheated steam |
| Feedwater Temperature | 25°C (raw) → 80°C (after HX-ECO) |
| Steam Temperature | 800°C at SOEC inlet |
| Pressure | Per SOEC vendor requirement |
| Treatment | Deaeration, chemical treatment, continuous blowdown |

**Loop C fluid quality is critical for SOEC stack life.** Contaminants cause stack degradation and premature failure.

### Fluid Separation Doctrine

> **Fluids never mix. Heat transfers via HX surfaces only.**

This doctrine ensures:
- No contamination between loops
- Each loop operates at optimal chemistry
- Vendor-controlled systems remain isolated
- Failure in one loop does not propagate

## 1.6 Loop B Specifications ◄━━ LOCKED

*Integrated from WP-8*

### Design Parameters

| Parameter | Specification |
|-----------|---------------|
| Design Pressure | Per piping class (TBD by detailed design) |
| Design Temperature | 150°C maximum |
| Minimum Operating Temperature | 30°C |
| Maximum Operating Temperature | 110°C (normal), 120°C (upset) |
| Flow Rate | Per thermal load (sized by heat balance) |
| Pipe Material | Carbon steel (buried), stainless (above-grade risers) |
| Insulation | Factory-applied polyurethane foam |
| Jacket | HDPE (high-density polyethylene) |

### Fluid Selection

| Option | Status | Notes |
|--------|--------|-------|
| Treated Water | **DEFAULT** | With corrosion inhibitors, biocide |
| Glycol Solution | Permitted if required | Only after freeze contingency analysis proves water alone is insufficient |
| Ammonia | **PROHIBITED** | Toxicity, leak consequences unacceptable for campus-wide distribution |

## 1.7 Freeze Protection Doctrine ◄━━ LOCKED

*Source: ATLAS_CORE_Memory_v20.md Section 4 — Verbatim*

> Freeze protection relies on layered defense. Insulation alone is insufficient.

### Four-Layer Defense

| Layer | Implementation | Purpose |
|-------|----------------|---------|
| **1. Continuous Circulation** | Minimum flow bypasses at all pump stations; automatic recirculation on pump trip | Prevents stagnation that allows heat loss |
| **2. Segmentation** | Valve vaults at branches and regular intervals; isolation valves sized for full flow | Limits exposure zone if circulation is lost |
| **3. Targeted Heat Trace** | Electric heat trace at valve vaults, above-grade risers, dead legs, instrument taps | Protects vulnerable points where heat loss is greatest |
| **4. Drainback** | All segments that may be intentionally de-energized must be fully drainable | Eliminates freeze risk in inactive sections |

### Critical Constraints

- **Loop B stagnation during winter operation is prohibited unless drained**
- Full-length heat trace on buried mains is **NOT required** (burial + insulation is sufficient)
- Targeted heat trace **IS required** at:
  - Valve vaults
  - Above-grade risers
  - Dead legs
  - Instrument taps
  - Any location where heat loss rate exceeds insulation capability

### Freeze Protection and Constraint Hierarchy

Per Section 0.4, Loop B circulation is Priority 2 in the constraint hierarchy:

```
1. PIPE INTEGRITY       ← Freeze protection systems
2. LOOP B CIRCULATION   ← Minimum flow maintained
    ...
```

**O₂ handling shall be shed before any reduction in Loop B circulation.**

## 1.8 Underground Distribution Standard ◄━━ LOCKED

*Integrated from WP-8*

### Burial Depth

| Requirement | Specification | Rationale |
|-------------|---------------|-----------|
| Minimum Cover | **36 inches** to top of outer pipe jacket | Exceeds 24" frost depth with margin |
| Road Crossings | Deeper burial or sleeved casing | Protect against vehicle loads |
| Rail Crossings | Per railroad authority requirements | Typically cased crossing |

### Pipe System Specification

| Component | Specification |
|-----------|---------------|
| Carrier Pipe | Carbon steel or stainless (per chemistry) |
| Insulation | Factory-applied polyurethane foam |
| Jacket | HDPE (high-density polyethylene) |
| System Type | Pre-insulated, factory-jacketed, district energy grade |

**Field-wrapped insulation is PROHIBITED on long runs.** Factory application ensures consistent thickness, no gaps, proper bonding, and integrated leak detection.

### Leak Detection and Locating

| Feature | Specification |
|---------|---------------|
| Leak Detection | Integrated conductors embedded in insulation annulus |
| Locating Wire | Separate tracer wire installed above jacket |
| Separation | Leak detection wire shall NOT be used for utility locating |

**Rationale:** Leak detection wires are fragile and calibrated for moisture sensing. Using them for locating risks damage and false alarms.

### Valve Vault Requirements

Valve vaults shall be installed at:
- Every branch connection
- Regular intervals along mains (spacing per thermal analysis)
- Major equipment connections

Each valve vault shall contain:

| Component | Purpose |
|-----------|---------|
| Isolation Valves | Segment isolation |
| Drain Connection | Segment drainback |
| Air Release Valve | Trapped air removal |
| Local Temperature Sensor | Freeze monitoring |
| Leak Detection Termination | Zone identification |
| Heat Trace | Vault freeze protection |

**Vaults must be accessible year-round** (not blocked by snow, flooding, or other obstructions).

### Utility Tunnels

| Application | Status |
|-------------|--------|
| Dense plant cores (200-800 ft) | **Permitted** |
| Campus-wide distribution | **Prohibited** |
| Hazardous fluid routing | Requires full life safety design justification |

**Rationale:** Campus-wide tunnels are expensive, require confined space entry for maintenance, and create fire/flood propagation paths. Direct burial is preferred except in dense process areas.

---

# VOLUME II: POWER SYSTEMS

## 2.1 AP1000 Nuclear — Primary Baseload

Each Power-Fuels Train (PFT) is anchored by one Westinghouse AP1000 pressurized water reactor:

| Parameter | Value | Notes |
|-----------|-------|-------|
| Electrical Output | 1,100 MWe net | After house loads |
| Thermal Output | 3,400 MWth | Core thermal power |
| Reactor Type | PWR (Gen III+) | Pressurized water reactor |
| Fuel | UO₂ enriched to <5% | Standard LEU fuel |
| Refueling Cycle | 18-24 months | Online ~92% capacity factor |
| Design Life | 60 years (extendable to 80) | With license renewal |
| Safety Systems | Passive | No operator action required for 72 hours |
| Containment | Steel + concrete | Aircraft impact resistant |
| NRC Status | Design certified | COL applications successful, units under construction |

### Selection Rationale

The AP1000 was selected over alternatives for:

1. **Passive Safety:** Gravity-fed cooling, no pumps required for emergency core cooling
2. **NRC Certification:** Design certified, eliminating licensing uncertainty
3. **Construction Experience:** Multiple units under construction globally, lessons learned incorporated
4. **Standardization:** Identical units enable common training, spare parts, procedures
5. **Output Match:** 1,100 MWe aligns with PFT load requirements

## 2.2 LPG Turbine System — Emergency/Grid Services

*Updated per WP-4, WP-7 — Turbine role reduced to emergency only*

| Component | Quantity | Output | Role |
|-----------|----------|--------|------|
| LPG Gas Turbine | 3 | 30 MWe each | Emergency, black start, grid services |
| Heat Recovery Steam Generator | 1 | ~45 MWth recovered | Exhaust heat capture |
| LP Steam Turbine | 1 | 15 MWe | Bottoming cycle |
| CO₂ Capture System | 1 | ~95% capture | Exhaust scrubbing |
| **TOTAL SYSTEM** | — | **105 MWe** | Combined cycle |

### Permitted Uses

- Black start (energize campus from cold iron)
- Fast response to grid frequency events
- Emergency backup generation
- Grid ancillary services (when contracted)

### Prohibited Uses ◄━━ LOCKED

- **Continuous baseload generation** — Turbines shall not run continuously for routine operations
- **Routine night margin support** — Night margin is achieved through load reduction, not turbine generation

*Source: WP-4 Section 6, Doctrine 3*

### Rationale for Reduced Role

Per WP-7 BTU trade study, the same LPG burned in the boiler to displace electric heating provides +85 MWe better net benefit than burning it in turbines for generation:

| Path | Net Benefit | Mechanism |
|------|-------------|-----------|
| LPG + O₂ Boiler | **120.7 MWe** | Thermal displacement of electric heaters |
| LPG Turbines | 35.8 MWe | Direct generation at ~35% efficiency |
| **Delta** | **+85 MWe** | Boiler path superior |

## 2.3 Tail Gas Turbine — Process Byproduct Power

| Parameter | Value |
|-----------|-------|
| Output | 100 MWe |
| Fuel | FT tail gas (unreacted syngas, light hydrocarbons) |
| Availability | 24/7 (continuous process byproduct) |
| Dispatch | Always on — baseload from refinery operations |
| CO₂ | Captured and recycled to FT synthesis |

The tail gas turbine converts refinery byproduct gases that would otherwise be flared into useful electricity. This is not optional capacity — it runs whenever the refinery operates.

## 2.4 Solar Array — Daytime Supplementation

| Parameter | Phase 1 | Phase 2 | Phase 3 (Full) |
|-----------|---------|---------|----------------|
| Capacity | 1 GW | 3 GW | 5 GW |
| Technology | Bifacial mono-Si | Bifacial mono-Si | Bifacial mono-Si |
| Tracking | Single-axis | Single-axis | Single-axis |
| Capacity Factor | ~25% | ~25% | ~25% |
| Average Output (day) | ~400 MWe/PFT | ~400 MWe/PFT | ~830 MWe/PFT |
| Land Area | 2,500 acres | 7,500 acres | 12,500 acres |

Solar provides significant daytime power, enabling:
- BESS charging for night reserves
- O₂ handling at full capacity (Mode A)
- DAC at maximum capture rate
- Export to grid when campus loads satisfied

## 2.5 Biomass Plant — Dispatchable Renewable

| Parameter | Value |
|-----------|-------|
| Capacity | 1 GW (campus-wide shared) |
| Per-PFT Share | ~167 MWe |
| Technology | Oxy-combustion with CO₂ capture |
| CO₂ Capture Rate | >95% |
| Fuel | Forest residue, agricultural waste |
| Dispatch | Swing/backup — fills gaps between nuclear and solar |

### Role in Thermal Cascade

Beyond electrical generation, biomass provides **temperature lift** to Loop B via HX-BIOMASS (50-80 MWth). This is critical for:
- Raising Loop B temperature when DC waste heat alone is insufficient
- Maintaining DAC regeneration temperature
- Stabilizing Loop B during transitions (Priority 3 in constraint hierarchy)

## 2.6 Three-Tier BESS Architecture ◄━━ LOCKED

*Integrated from WP-5 ASG-PFT-WP5-ICD-001 Rev B*

### 2.6.1 Architecture Philosophy

The campus employs a **three-tier battery strategy** that separates:
- Process stability (Tier 1 — PFT)
- Data center protection (Tier 2 — DC)
- Campus-wide energy shifting (Tier 3 — Campus)

> **These tiers shall NOT be electrically combined except through controlled interfaces.**

### 2.6.2 Tier Definitions

| Tier | Name | Purpose | Isolation |
|------|------|---------|-----------|
| **Tier 1** | PFT BESS | Process continuity, heater ride-through, SOEC protection | Electrically isolated to each PFT train |
| **Tier 2** | DC BESS | UPS-class ride-through and power quality | Electrically isolated from campus and PFT |
| **Tier 3** | Campus BESS | Bulk energy shifting, solar smoothing, contingency reserve | Modular blocks added by phase |

### 2.6.3 Bible-Level Constants ◄━━ CANON

| Parameter | Value | Notes |
|-----------|-------|-------|
| Usable Depth of Discharge (DoD) | 0.80 | 80% of nameplate is usable |
| Round-Trip Efficiency (RTE) | 0.90 | 90% charge-discharge efficiency |
| Minimum Reserve SOC | 0.10 | 10% always retained |
| Usable Energy Factor | 0.648 | DoD × (1 - reserve) × RTE |

### 2.6.4 Tier Ratings ◄━━ CANON

#### Tier 1: PFT BESS (Per PFT)

| Parameter | Value |
|-----------|-------|
| Energy (nameplate) | **175 MWh** |
| Power | **300 MW** |
| Nominal C-rate | 1.7C |
| Guaranteed Ride-through | 30+ minutes at 219 MW heater load |
| Function | Full heater ride-through with reserves and losses included |

**Sizing Basis:** 175 MWh × 0.648 (usable) = 113 MWh usable. At 219 MW heater load, this provides 31 minutes of ride-through — sufficient for generation switchover or controlled shutdown.

#### Tier 2: Data Center BESS (Per PFT)

| Parameter | Value |
|-----------|-------|
| Energy (nameplate) | **50 MWh** |
| Power | **120 MW** |
| Nominal C-rate | 2.4C |
| Function | 15-17 minute UPS-class ride-through at full IT load |

**Design Intent:** Tier 2 accepts the hard cycling and power quality events that would degrade Tier 1 and Tier 3 batteries. It acts as a buffer, preserving the cycle life of larger campus batteries.

#### Tier 3: Campus BESS (Per Phase Block)

| Parameter | Value |
|-----------|-------|
| Energy | **500 MWh** |
| Power | **250 MW** |
| Nominal C-rate | 0.5C |
| Phase 1 | 1 block |
| Expansion | Each additional phase adds +1 block |

**Function:** Bulk energy shifting (store solar, discharge at night), solar smoothing (absorb variability), contingency reserve (deep backup after Tier 1/2 exhausted).

### 2.6.5 Dispatch Doctrine ◄━━ LOCKED

**Tier Roles:**

| Tier | Primary Role | What It Protects |
|------|--------------|------------------|
| Tier 2 (DC) | Takes fast transients, poor power quality | Preserves Tier 1 and Tier 3 cycle life |
| Tier 1 (PFT) | Buffers heaters and SOEC | Prevents thermal cycling, first line of defense |
| Tier 3 (Campus) | Bulk shifting, contingency buffer | NOT used as UPS or primary ride-through |

**Load Shed Priority Order:**

1. Discharge PFT BESS (Tier 1)
2. Discharge Campus BESS (Tier 3)
3. Shed O₂ handling loads
4. Reduce DAC
5. Curtail SOEC banks (last resort)

### 2.6.6 BESS Use Constraints

- **PFT BESS shall not be used for steady-state load balancing** — transient support only
- **Campus BESS shall not act as UPS** — that's Tier 2's job
- **BESS discharge beyond defined durations** requires active ramp of generation or load reduction

### 2.6.7 Black Start Sequence

In the event of complete grid loss, the campus can self-start using BESS and combustion assets:

| Step | Action |
|------|--------|
| 1 | Campus BESS energizes campus MV bus in grid-forming mode |
| 2 | Control power, communications, cooling, and safety systems come online |
| 3 | PFT BESS energizes PFT auxiliaries and heater warm-standby |
| 4 | LPG turbines start and synchronize |
| 5 | System transitions to islanded operation |
| 6 | Nuclear restart procedures initiated (if applicable) |

## 2.7 Power Stack Summary (Per PFT)

| Source | Capacity | Availability | Dispatch Priority |
|--------|----------|--------------|-------------------|
| AP1000 Nuclear | 1,100 MWe | 24/7 baseload | 1 (always on) |
| Tail Gas Turbine | 100 MWe | 24/7 (process byproduct) | 2 (always on) |
| Biomass (PFT share) | 167 MWe | Dispatchable | 3 (swing) |
| LPG Turbines + HRSG | 105 MWe | Emergency only | 4 (emergency/grid) |
| Solar (PFT share) | ~830 MWe peak | Daytime only | 5 (when available) |
| **FIRM DISPATCHABLE** | **1,472 MWe** | — | AP1000 + Tail + Biomass + LPG |
| **PEAK AVAILABLE** | **~2,300 MWe** | — | All sources |

## 2.8 SOEC Power Electronics ICD

*Integrated from WP-2 ASG-PFT-WP2-PE-001 Rev A*

### 2.8.1 Design Intent

> - Deliver stable DC power to SOEC stacks within vendor-defined voltage and current limits
> - Prevent fast power swings that induce thermal cycling
> - Support hot-hold and warm-standby modes
> - Allow graceful curtailment without stack damage
> - Isolate electrical faults to the smallest possible block
> - **Never rely on SOEC load for grid stabilization**

### 2.8.2 Electrical Architecture

**Conversion Chain:**
```
AC (MV Campus Bus)
    ↓
Step-down Transformer
    ↓
Active Front-End Rectifier (AFE)
    ↓
DC Bus
    ↓
DC/DC Converters (if required by stack voltage)
    ↓
SOEC Stack Modules
```

### 2.8.3 AC Side Specifications

| Parameter | Specification |
|-----------|---------------|
| AC Voltage at POI | Per campus MV standard |
| Frequency | 60 Hz |
| Short-Circuit Duty | Defined by campus fault study |
| Power Factor | Unity or near-unity (AFE requirement) |

### 2.8.4 DC Side Specifications

| Parameter | Specification |
|-----------|---------------|
| DC Voltage Range | Vendor-defined (stack dependent) |
| DC Current | Controlled per stack rating |
| DC Ripple Limits | Enforced by rectifier and filtering design |
| Ramp Rate Limits | Per SOEC vendor thermal specifications |

### 2.8.5 Modular Segmentation ◄━━ LOCKED

The SOEC plant is divided into **multiple independent electrical blocks**. Each block includes:
- Dedicated transformer
- Dedicated rectifier
- DC protection
- Stack group

> **Failure of one block shall NOT trip adjacent blocks.**

> **Segmentation is mandatory to avoid single-point failure.**

> **Faults must isolate locally without collapsing the SOEC plant bus.**

### 2.8.6 Rectifier Requirements

| Requirement | Specification |
|-------------|---------------|
| Topology | **Active Front-End (AFE) required** |
| Passive Diode Rectifiers | **PROHIBITED** |
| Power Factor | Unity or near-unity |
| Harmonic Distortion | Low THD per IEEE 519 |
| Soft-Start | Required (avoid inrush) |
| Soft-Stop | Required (avoid transients) |
| Hot-Hold Mode | Reduced power maintains stack temperature |

### 2.8.7 Critical Constraint

> **SOEC shall NEVER be used for grid regulation or frequency response.**

SOEC stacks are thermal devices. Rapid power changes cause thermal cycling that degrades stack life. Grid regulation requires second-by-second power adjustments — SOEC cannot provide this without damage.

---

# VOLUME III: THERMAL CASCADE

## 3.1 Three-Loop Architecture ◄━━ LOCKED

*Source: ATLAS_CORE_Memory_v20.md Section 3 — Verbatim*

The thermal system consists of three physically isolated loops:

> **Fluids never mix. Heat transfer occurs only across heat exchanger surfaces.**

### 3.1.1 Loop Definitions

| Loop | Purpose | Fluid | Temperature Range |
|------|---------|-------|-------------------|
| **A** | Data Center Internal Cooling | Vendor-controlled | 30-45°C supply, 50-65°C return |
| **B** | Campus Heat Recovery | Treated water | 30°C → 70-110°C → 30°C |
| **C** | Boiler Feedwater/Steam | High-purity, deaerated | 25°C → 800°C |

### 3.1.2 Heat Exchanger Cascade

| HX | Function | Heat Transfer | Notes |
|----|----------|---------------|-------|
| HX-DC | Loop A → Loop B | 120 MWth | DC waste heat recovery |
| HX-BIOMASS | Biomass → Loop B | 50-80 MWth | Temperature lift |
| HX-DAC | Loop B → DAC | ~80 MWth | Sorbent regeneration |
| HX-ECO | Loop B → Loop C | ~12 MWth | BFW preheat |

## 3.2 Steam Generation Stages ◄━━ CANON

*Integrated from WP-1 ASG-PFT-WP1-ESG-001 Rev A*

Rev 4.1 replaces the all-electric steam generation with a **three-stage approach**:

| Stage | Temperature Range | Heat Source | Duty | Electric Load |
|-------|-------------------|-------------|------|---------------|
| **Stage 1: Economizer** | 25°C → 80°C | Loop B (HX-ECO) | ~12 MWth | 0 MWe |
| **Stage 2: Evap + SH1** | 80°C → 350°C | LPG + O₂ Boiler | ~64 MWth | 0 MWe |
| **Stage 3: Electric Trim** | 350°C → 800°C | Electric superheaters | — | **140 MWe** |

### Stage 1 — Feedwater Preheat (Recovered Heat)

| Parameter | Specification |
|-----------|---------------|
| Source | Loop B economizer (HX-ECO) |
| Temperature Rise | 25°C to approximately 80°C |
| Heat Recovered | ~12 MWth |
| Purpose | Reduce low-grade electric heater duty |
| Control | Continuous modulation based on Loop B temperature |

### Stage 2 — LPG + O₂ Boiler (Mid-Grade Enthalpy)

| Parameter | Specification |
|-----------|---------------|
| Source | LPG + O₂ fired boiler |
| Temperature Rise | Approximately 80°C to 350°C |
| Process | Evaporation + intermediate superheat |
| Fuel | LPG from FT process or contracted supply |
| Oxidizer | O₂ from SOEC (enriched combustion) |
| Purpose | Primary night mode heat source |

**O₂-enriched combustion** increases flame temperature, improves efficiency, and produces a concentrated CO₂ stream for capture and recycling to FT synthesis.

### Stage 3 — Electric Trim Heating

| Parameter | Specification |
|-----------|---------------|
| Source | Electric resistance or induction heaters |
| Temperature Rise | Approximately 350°C to 800°C |
| Electric Power | **~140 MWe** (reduced from 219 MWe) |
| Function | Final superheat only |
| Control | Precision temperature control to SOEC inlet |

### Power Comparison: Rev 4.0 vs Rev 4.1

| Scenario | Rev 4.0 (All-Electric) | Rev 4.1 (Three-Stage) | Reduction |
|----------|------------------------|------------------------|-----------|
| Full heating 25°C → 800°C | 219 MWe | — | — |
| With economizer | — | -12 MWe | — |
| With LPG boiler | — | -60 to -70 MWe | — |
| **Electric trim only** | — | **~140 MWe** | **-79 MWe** |

## 3.3 Steam Flow and Conditions ◄━━ LOCKED

| Parameter | Value |
|-----------|-------|
| Steam Mass Flow | 52.1 kg/s (per PFT) |
| Steam Outlet Temperature | 800°C |
| Steam Pressure | Per SOEC vendor requirement (TBD) |
| Feedwater Inlet Temperature | 25°C (nominal, prior to preheat) |
| Steam Quality at SOEC Inlet | Dry, superheated |

## 3.4 Electric Heater Architecture

| Parameter | Specification |
|-----------|---------------|
| Heater Type | Industrial-grade electric superheaters |
| Construction | Modular with N+1 redundancy |
| Control | Individually controllable heater banks |
| Ramp Capability | Gradual ramping, warm standby |

### Design Constraints

> **Heater banks shall be capable of holding steam at intermediate temperature without cycling to ambient.**

> **Sudden heater shutdowns are PROHIBITED except in safety events.**

**Rationale:** SOEC stacks are sensitive to thermal shock. Sudden temperature changes cause mechanical stress and degradation. Heaters must be capable of controlled ramp-down to warm standby, not just on/off operation.

## 3.5 Operating Modes

*Cross-reference: Section 0.7 Operating Mode Framework*

### Day Mode

- Electric trim permitted at higher duty (solar margin available)
- LPG boiler may idle (fuel preserved)
- O₂ capture enabled (Mode A)
- Full flexibility in steam generation source mix

### Evening Transition

- Electric trim ramps down (following solar decline)
- LPG boiler ramps up (smooth handover)
- BESS buffers short transients during transition
- No step changes — continuous controlled transfer

### Night Mode

- LPG boiler at planned duty (primary mid-grade heat)
- Electric trim minimized (140 MWe)
- Steam temperature stabilized for SOEC
- Loop B temperature maintained by biomass

### Contingency Mode

- Immediate PFT BESS discharge (cover transient)
- Electric trim reduced to warm standby (preserve power)
- SOEC curtailed only if reserves threatened
- **Steam temperature maintained above minimum throughout**

---

# VOLUME IV: CARBON CAPTURE

## 4.1 CO₂ Requirements

Fischer-Tropsch synthesis requires massive CO₂ input:

| Metric | Per PFT | Phase 3 (6 PFT) | Full Build (12 PFT) |
|--------|---------|-----------------|---------------------|
| CO₂ Required | ~6,200 t/day | ~37,200 t/day | ~74,400 t/day |
| From DAC | ~90% | Primary source | Primary source |
| From Biomass | ~10% | Biogenic carbon | Biogenic carbon |
| From LPG Turbine Exhaust | Recycled | Closed loop | Closed loop |

## 4.2 Direct Air Capture (DAC)

| Parameter | Value | Notes |
|-----------|-------|-------|
| Technology | Solid sorbent | Temperature-swing regeneration |
| Regeneration Heat | 80-120°C | Low-grade thermal |
| Heat Source | Data center waste heat | 60-80°C boosted via Loop B |
| Electrical Load | ~100-109 MWe per PFT | Fans, compressors, pumps |
| CO₂ Output | ~6,200 t/day per PFT | 90% of synthesis requirement |
| Land Area | ~85 acres per PFT | Modular contactor arrays |

### Thermal Integration

DAC is thermally integrated with the campus heat recovery system:

1. **Data centers** reject ~114 MWth of waste heat at 60-80°C
2. **Loop B** collects this heat via HX-DC
3. **Biomass** provides temperature lift when needed (HX-BIOMASS)
4. **DAC** receives heat from Loop B via HX-DAC (~80 MWth)
5. **Sorbent regeneration** releases captured CO₂ for compression and synthesis

This integration makes data centers a **thermal asset** rather than a cooling burden.

## 4.3 DAC and Constraint Hierarchy

DAC is **Priority 5** in the constraint hierarchy:

```
...
4. O₂ HANDLING SHED
5. DAC REDUCTION       ◄── DAC reduced before touching SOEC
6. SOEC CURTAILMENT
```

During power shortfall:
- DAC electrical load (fans, compressors) is reduced
- DAC thermal load (regeneration heat) continues as long as Loop B operates
- CO₂ production decreases but does not stop completely

## 4.4 Carbon Loop Closure

The campus operates a closed carbon loop:

```
DAC ──→ CO₂ ──→ FT Synthesis ──→ Fuels
                     ↑              │
                     │              ↓
              CO₂ Capture ←── Combustion (LPG Turbines, Biomass)
```

**Net Carbon Impact: NEGATIVE**

- DAC captures atmospheric CO₂
- FT synthesis converts CO₂ to fuels
- Combustion releases CO₂
- Exhaust CO₂ is captured and recycled
- DAC captures more than combustion emits

---

# VOLUME V: HYDROGEN & OXYGEN PRODUCTION

## 5.1 SOEC System Overview

Solid Oxide Electrolysis Cells (SOEC) produce hydrogen from high-temperature steam:

| Parameter | Value | Notes |
|-----------|-------|-------|
| H₂ Production Target | 500 t/day per PFT | Phase 3: 3,000 t/day |
| Operating Temperature | 800°C | Optimal efficiency point |
| Steam Flow | 52.1 kg/s | ~9 kg steam per kg H₂ |
| Electrical Consumption | 708 MWe | 34 kWh/kg H₂ (system level) |
| Efficiency | ~82% LHV | With heat integration |
| O₂ Co-product | ~4,000 t/day per PFT | ~8 kg O₂ per kg H₂ |

## 5.2 Steam Generation for SOEC

*Cross-reference: Volume III Section 3.2*

| Stage | Equipment | Electric Load |
|-------|-----------|---------------|
| Economizer | Loop B HX-ECO | 0 MWe (recovered heat) |
| Evap + SH1 | LPG + O₂ Boiler | 0 MWe (LPG fuel) |
| SH2 Trim | Electric superheaters | **140 MWe** |
| **TOTAL** | — | **140 MWe** |

**Reduction from Rev 4.0:** 219 MWe → 140 MWe = **-79 MWe**

## 5.3 SOEC Redundancy

SOEC banks are designed with N+1 redundancy:

| Feature | Implementation |
|---------|----------------|
| Parallel Stacks | Single stack failure does not halt production |
| Hot Standby | Spare stacks maintained at operating temperature |
| Integral Heaters | SOEC trim heaters compensate for steam temperature variations |
| Modular Blocks | Electrical and thermal isolation per WP-2 |

## 5.4 Oxygen System ICD

*Integrated from WP-6 ASG-PFT-WP6-ICD-001 Rev A*

### 5.4.1 System Overview

Oxygen is produced as a co-product of SOEC operation at approximately 8 kg O₂ per kg H₂, yielding 4,000 t/day per PFT. The system includes:

- Product compression to pipeline or process pressure
- Drying and polishing
- Optional liquefaction or bulk storage
- Export to downstream consumers
- Controlled venting during shed or emergency modes

### 5.4.2 Oxygen Utilization

| Consumer | Application | Priority |
|----------|-------------|----------|
| Biomass Oxy-Combustion | Primary consumer, enables >95% CO₂ capture | 1 |
| LPG + O₂ Boiler | Steam generation enrichment | 2 |
| Process Burners | Refinery heaters, higher flame temperatures | 3 |
| LOX Storage | Cryogenic tanks for peak demand | 4 |
| Medical/Industrial Sale | Revenue stream for excess | 5 |

### 5.4.3 O₂ Operating Modes ◄━━ LOCKED

| Mode | Name | Description | Load |
|------|------|-------------|------|
| **A** | Day Capture | O₂ handling plant enabled; compress, condition, store or export | **40 MWe** |
| **B** | Evening Transition | Scheduled ramp-down; stop liquefaction, reduce compression | Reducing |
| **C** | Night Shed | O₂ handling off by default; route to vent header | **5 MWe** |
| **D** | Emergency Shed | Immediate trip; forced venting to safe state | Minimum |

### 5.4.4 Mode D Triggers

Mode D (Emergency Shed) is triggered by:
- Underfrequency event
- BESS reserve SOC below threshold
- Generator trip
- Fire or gas detection in O₂ area
- Any safety interlock event

> **Any interlock event shall place the system into Mode D.**

### 5.4.5 O₂ and Constraint Hierarchy

O₂ handling is **Priority 4** in the constraint hierarchy:

> **O₂ handling loads shall be shed before DAC reduction or SOEC curtailment.**

> **O₂ handling shall NEVER block Loop B circulation or freeze protection logic.**

### 5.4.6 Venting System Requirements

| Requirement | Specification |
|-------------|---------------|
| Vent Header | Dedicated oxygen-rated piping |
| Vent Stack | High-point discharge, away from occupied areas |
| Materials | Compatible with high-purity oxygen |
| Dispersion | Analysis required to ensure safe dilution |
| Exclusion | No air intakes, ignition sources, electrical yards in vent plume |

---

# VOLUME VI: FUEL SYNTHESIS

## 6.1 Process Overview

The Fischer-Tropsch refinery converts H₂ and CO₂ into drop-in synthetic fuels:

```
H₂ + CO₂ ──→ [RWGS] ──→ Syngas (CO + H₂) ──→ [FT Reactor] ──→ Wax ──→ [Hydrocracker] ──→ Products
```

### Process Units

| Unit | Function | Temperature | Notes |
|------|----------|-------------|-------|
| RWGS Reactor | CO₂ + H₂ → CO + H₂O | 700°C | Endothermic, electric heat |
| FT Reactor | CO + H₂ → –CH₂– + H₂O | 200-240°C | Exothermic, cobalt catalyst |
| Hydrocracker | Break long chains | 350-400°C | 100+ bar, H₂ consumption |
| Fractionation | Separate products | Various | Atmospheric distillation |

## 6.2 Production Targets

| Product | Fraction | Per PFT (BPD) | Phase 3 (BPD) | Phase 4 (BPD) | Full Build (BPD) |
|---------|----------|---------------|---------------|---------------|------------------|
| Diesel (ULSD) | 66% | 9,116 | 54,694 | 72,930 | 109,395 |
| Jet-A / SAF | 22% | 3,039 | 18,231 | 24,310 | 36,465 |
| LPG | 12% | 1,657 | 9,945 | 13,260 | 19,890 |
| **TOTAL** | **100%** | **13,812** | **82,870** | **110,500** | **165,750** |

**100,000 BPD milestone achieved at Phase 4 (8 PFT)**

## 6.3 Product Quality

| Property | FT Diesel | Conventional ULSD | Improvement |
|----------|-----------|-------------------|-------------|
| Cetane Number | >70 | 45-55 | +15-25 points |
| Sulfur | <1 ppm | <15 ppm | Near zero |
| Aromatics | ~0% | 20-30% | None |
| Cold Flow | Excellent | Variable | Superior |
| Carbon Intensity | Near zero | ~95 g CO₂/MJ | Carbon neutral |

## 6.4 LPG Fuel Closure

*Integrated from WP-4 ASG-PFT-WP4-FC-001 Rev A*

### LPG Use Priority ◄━━ LOCKED

| Priority | Use | Notes |
|----------|-----|-------|
| **1** | LPG + O₂ Boiler | Steady-state thermal displacement |
| **2** | LPG Turbines | Emergency, grid services, black start only |
| **3** | Export or Sale | Only after onsite needs satisfied |

> **Turbines are NOT relied upon for continuous night margin.**

## 6.5 LPG BTU Trade Study Findings

*Integrated from WP-7 ASG-PFT-WP7-TS-001 Rev A*

### Decision Principle ◄━━ CANON

> **LPG burned to create kW and LPG burned to save kW are equivalent at the grid boundary.**

### Comparison Results

| Path | Net Benefit | Notes |
|------|-------------|-------|
| LPG + O₂ Boiler | **120.7 MWe** | Thermal displacement of electric heaters |
| LPG Turbines | 35.8 MWe | Direct generation |
| **Delta** | **+85 MWe** | Boiler path superior |

---

# VOLUME VII: LOGISTICS

## 7.1 Tank Farm Infrastructure

| Product | Tank Type | Capacity | Days Supply |
|---------|-----------|----------|-------------|
| Diesel | Cone-roof tanks | 500,000 bbl | ~5 days |
| Jet-A | Floating roof tanks | 200,000 bbl | ~5 days |
| LPG | Horton spheres | 100,000 bbl | ~5 days |

## 7.2 Rail Terminal

| Parameter | Specification |
|-----------|---------------|
| Location | 80 acres |
| Receiving | Biomass (forest residue, agricultural waste) |
| Shipping | Diesel, jet, LPG unit trains |
| Rail Corridor | BNSF mainline access |

## 7.3 Biomass Supply Chain

| Parameter | Specification |
|-----------|---------------|
| Fuel Types | Forest residue, agricultural waste |
| Delivery Mode | Rail (primary), truck (supplemental) |
| Storage | Covered bins with conveyor feed |
| Consumption | ~15,000 t/day at full build (1 GW plant) |

---

# VOLUME VIII: DATA CENTERS

## 8.1 Facility Configuration

| Parameter | Per PFT | Phase 3 (6 PFT) | Full Build (12 PFT) |
|-----------|---------|-----------------|---------------------|
| Buildings | 2 | 12 | 24 |
| IT Load per Building | 60 MWe | 60 MWe | 60 MWe |
| Total IT Load | 120 MWe | 720 MWe | 1,440 MWe |
| Rack Density | Up to 50 kW/rack | — | — |
| Cooling | Liquid + air hybrid | — | — |
| PUE Target | <1.20 | — | — |

## 8.2 Power Architecture

| Component | Specification |
|-----------|---------------|
| Primary Power | AP1000 via medium-voltage distribution |
| Backup | LPG turbines (seamless transfer, no diesel generators) |
| UPS | Tier 2 DC BESS (50 MWh / 120 MW per PFT) |
| Ride-through | 15-17 minutes at full IT load |
| Reliability Tier | III+ (99.982% uptime) |

## 8.3 Thermal Integration

Data centers are **heat sources**, not just loads:

| Parameter | Value |
|-----------|-------|
| Waste Heat | ~114-120 MWth per PFT at 60-80°C |
| Transfer Path | HX-DC (Loop A → Loop B) |
| Primary Use | DAC sorbent regeneration (80-120°C) |

> **This symbiosis makes data centers a thermal asset rather than a cooling burden.**

---

# VOLUME IX: CONTROL SYSTEMS & INTELLIGENCE

## 9.1 Control Hierarchy

| Level | Function | Scope |
|-------|----------|-------|
| **L4 - MECSAI** | Campus optimization | All PFTs, grid interface |
| **L3 - PFT Controller** | Train coordination | Single PFT subsystems |
| **L2 - Unit Controller** | Equipment control | Individual process units |
| **L1 - Field Devices** | Sensing/actuation | Instruments, valves, motors |

## 9.2 MECSAI Functions

| Function | Description |
|----------|-------------|
| Energy Dispatch | Optimize power flow between sources and loads |
| Load Forecasting | Predict solar availability, demand patterns |
| Process Optimization | Tune SOEC, FT reactor, refinery parameters |
| Thermal Balancing | Coordinate waste heat flows to DAC |
| Constraint Enforcement | Ensure hierarchy is never violated |

## 9.3 Load-Shed Priority Table ◄━━ CANON

*Source: ATLAS_CORE_Memory_v20.md Section 6*

| Priority | Action | Relief (MWe) | Cumulative |
|----------|--------|--------------|------------|
| 0 | PFT BESS discharge | 300 | 300 |
| 1 | Campus BESS discharge | 125 | 425 |
| 2 | O₂ compression shed | 35 | 460 |
| 3 | DAC to minimum | 74 | 534 |
| 4 | H₂ compression curtail | 10 | 544 |
| 5 | Non-critical DC curtail | 30 | 574 |
| 6 | SOEC bank curtailment | 347 | 921 |
| 7 | Heater to warm standby | 154 | 1,075 |
| 8 | DC to minimum | 60 | 1,135 |

## 9.4 Safety Systems

| System | Description |
|--------|-------------|
| AP1000 | Native passive safety systems (NRC-certified) |
| Refinery ESD | Emergency shutdown system, SIL-2/SIL-3 rated |
| Fire & Gas | Detection and automatic response |
| H₂/O₂ | Leak detection and automatic isolation |
| Cybersecurity | Air-gapped safety systems, NERC CIP compliance |

## 9.5 Athena AEGIS — Regulatory Compliance

| Domain | Key Regulations |
|--------|-----------------|
| Nuclear | 10 CFR 50/52, DOE 10 CFR 830 |
| H₂/O₂ | NFPA 2, NFPA 55 |
| Refinery | OSHA PSM, EPA RMP, ASME B31.3 |
| Electrical | NEC, IEEE, NERC CIP |
| Environmental | NEPA, EPA air/water permits |

---

# VOLUME X: SITE INFRASTRUCTURE

## 10.1 Location

Heber Industrial Campus is located north of Heber, Arizona in Navajo County.

| Criterion | Heber Advantage |
|-----------|-----------------|
| Land Area | 36 square miles (23,040 acres) available |
| Rail Access | BNSF mainline proximity |
| Water | Coconino Aquifer access |
| Solar | Excellent irradiance (~5.5 kWh/m²/day) |
| Transmission | Existing APS 345 kV corridor |
| Population | Low density, suitable for nuclear exclusion zones |

## 10.2 Campus Layout

| Zone | Acreage | Function |
|------|---------|----------|
| PFT Footprint (each) | 80-100 acres | AP1000 + refinery + SOEC + data centers |
| PFT Total (12 units) | 1,200 acres | Full buildout capacity |
| Solar Array | 12,500 acres | 5 GW bifacial tracking |
| Biomass Facility | 100 acres | 1 GW oxy-combustion plant |
| DAC Array | 500 acres | Direct air capture modules |
| Central Tank Farm | 50 acres | Product storage |
| Rail Terminal | 80 acres | Biomass receiving, product shipping |
| Water Treatment | 50 acres | Central treatment + ZLD |
| Administration | 50 acres | Offices, maintenance, emergency services |

## 10.3 Safety Separations

| Requirement | Distance |
|-------------|----------|
| Hydrocarbon from nuclear | >1,000 ft |
| LPG from occupied buildings | >500 ft |
| O₂ from fuel storage | >1,000 ft |

## 10.4 Underground Distribution Standard

*Cross-reference: Volume I Section 1.8*

| Parameter | Specification |
|-----------|---------------|
| Minimum Burial | 36 inches to top of jacket |
| Pipe System | Pre-insulated, factory-jacketed |
| Leak Detection | Integrated conductors |
| Valve Vaults | At branches and intervals |

---

# APPENDICES

## Appendix A: Phased Deployment Schedule

| Phase | PFT Units | H₂ (t/day) | Fuel (BPD) | Solar | Timeline |
|-------|-----------|------------|------------|-------|----------|
| Phase 1 | 2 | 1,000 | 27,624 | 1 GW | Year 0-4 |
| Phase 2 | 4 | 2,000 | 55,248 | 3 GW | Year 4-8 |
| Phase 3 | 6 | 3,000 | 82,870 | 5 GW | Year 8-12 |
| **Phase 4** | **8** | **4,000** | **110,500** | 5 GW | Year 12-16 |
| Phase 5 | 10 | 5,000 | 138,120 | 5 GW | Year 14-18 |
| Phase 6 | 12 | 6,000 | 165,750 | 5 GW | Year 16-20 |

**100,000 BPD milestone achieved at Phase 4 (8 PFT)**

## Appendix B: Night Power Balance (Rev 4.1)

### Supply

| Source | Capacity (MWe) |
|--------|----------------|
| AP1000 | 1,100 |
| Tail Gas Turbine | 100 |
| Biomass (PFT share) | 167 |
| Boiler Steam Turbine | 20 |
| **TOTAL** | **1,387** |

### Load

| Component | Rev 4.0 | Rev 4.1 | Delta |
|-----------|---------|---------|-------|
| Steam generation | 219 | **140** | -79 |
| O₂ handling | 40 | **5** | -35 |
| All other loads | 1,049 | 1,049 | 0 |
| **TOTAL** | **1,308** | **1,194** | **-114** |

### Margin

| Metric | Rev 4.0 | Rev 4.1 | Improvement |
|--------|---------|---------|-------------|
| **Night Margin** | +79 MWe | **+193 MWe** | **+144%** |

## Appendix C: PFT Electrical Load Summary (Rev 4.1)

| Consumer | Load (MWe) | % of Total |
|----------|------------|------------|
| SOEC Electrolysis | 708 | 59.3% |
| Electric Steam Generation | **140** | **11.7%** |
| Data Centers | 120 | 10.0% |
| DAC Electrical | 109 | 9.1% |
| Refinery Process Heat | 77 | 6.4% |
| Refinery + BOP | 35 | 2.9% |
| O₂ Handling (night) | **5** | **0.4%** |
| **TOTAL (Night)** | **1,194** | **100%** |

## Appendix D: Glossary

| Term | Definition |
|------|------------|
| AFE | Active Front-End (rectifier topology) |
| AP1000 | Westinghouse Advanced Passive 1000 MWe PWR |
| BESS | Battery Energy Storage System |
| BFW | Boiler Feedwater |
| BPD | Barrels per day |
| DAC | Direct Air Capture (atmospheric CO₂) |
| FT | Fischer-Tropsch synthesis |
| HX | Heat Exchanger |
| ICD | Interface Control Document |
| LPG | Liquefied Petroleum Gas |
| MECSAI | Master Energy Control System AI |
| MGD | Million gallons per day |
| PFT | Power-Fuels Train |
| SOEC | Solid Oxide Electrolysis Cell |
| ZLD | Zero Liquid Discharge |

## Appendix E: Work Package Reference

| WP | Title | Doc ID | Rev |
|----|-------|--------|-----|
| WP-1 | Electric Steam Generation Module | ASG-PFT-WP1-ESG-001 | A |
| WP-2 | SOEC Power Electronics ICD | ASG-PFT-WP2-PE-001 | A |
| WP-3 | Firm Margin Rewrite | ASG-PFT-WP3-OM-001 | A |
| WP-4 | LPG Fuel Closure | ASG-PFT-WP4-FC-001 | A |
| WP-5 | BESS ICD | ASG-PFT-WP5-ICD-001 | B |
| WP-6 | Oxygen System ICD | ASG-PFT-WP6-ICD-001 | A |
| WP-7 | LPG BTU Trade Study Framework | ASG-PFT-WP7-TS-001 | A |
| WP-8 | Water and Heat Routing ICD | ASG-PFT-WP8-ICD-001 | B |

## Appendix F: Document Control

### Approval Signatures

| Role | Name | Date | Signature |
|------|------|------|-----------|
| Prepared By | Agent B (Claude) | 2026-01-30 | _________________ |
| Technical Review | Agent A | Pending | _________________ |
| Approved By | Commander Gary Spear | Pending | _________________ |

### Classification

**INTERNAL / PROPRIETARY**

This document contains proprietary information of Atlas Systems Group.

### Document Supersession

This document (Rev 4.1) supersedes all prior revisions:
- ASG-MEB-AGENTB-001 Rev 4.0 — SUPERSEDED
- ASG-MEB-AGENTB-001 Rev 3.0 — SUPERSEDED
- ASG-MEB-AGENTB-001 Rev 2.1 — SUPERSEDED
- ASG-MEB-AGENTB-001 Rev 2.0 — SUPERSEDED
- ASG-MEB-AGENTB-001 Rev 1.0 — SUPERSEDED

---

**END OF DOCUMENT**

---

*Document: ASG-MEB-AGENTB-001*  
*Revision: 4.1*  
*Date: 2026-01-30*  
*Prepared By: Agent B (Claude) — Validation Authority*  
*Approved By: Commander Gary Spear (pending)*
