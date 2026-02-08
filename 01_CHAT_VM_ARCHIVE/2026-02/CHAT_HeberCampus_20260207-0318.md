# CHAT_HeberCampus_20260207-0318

**Snapshot Timestamp:** 2026-02-07 03:18 UTC  
**Source:** ChatGPT Extraction (HCV-VM-EXTRACT-002)  
**Thread:** HeberCampus  
**VM_VERSION:** 20260207-0318  
**Immutable:** Yes

---

## Heber Campus Phase 1/Phase 2 Expansion Planning & Governance Framework

### Phase 2 Expansion Capacity Target
- **Ultimate Solar Capacity:** Approximately 5 GW (Phase 1 + Phase 2 combined)
- **Phase 1 Planning Assumption:** Interim baseline (1.5 GW documented in prior deltas)
- **Phase 2 Growth:** Approximately 3.5 GW additional solar capacity
- **Data Center Expansion:** Beyond Phase 1 baseline (current footprint unspecified but reserved)
- **Constraint:** Phase 1 design must NOT require rework to accommodate Phase 2

### Export Substation Location & MVAC Infrastructure
- **Fixed Location:** Northwest quadrant of Heber Campus
- **Siting Rationale:** Shortest MVAC transmission line tie-in distance to regional transmission corridors
- **Cost Driver:** Grid interconnection distance minimizes tie-in cost — fixed endpoint constraints site
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
- **No Rework Allowed:** Phase 1 coridor placement governs Phase 2 connection points
- **Planning Impact:** Utility routing analyzed for Phase 1 + Phase 2 loads simultaneously; Phase 1 construction includes oversized capacity in corridors to accommodate Phase 2 without relocating pipes/cables

### Architectural & Governance Alignment

#### AO Design Output Governance Review
- **Review Standard:** HC-MGD-001 (Heber Campus Management Governance Document 001 — assumed to define expansion doctrine)
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
