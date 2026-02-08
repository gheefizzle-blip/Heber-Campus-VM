# CHAT_Heber_Global_Roadmap_20260208-0030

**Snapshot Timestamp:** 2026-02-08 00:30 UTC  
**Source:** ChatGPT Extraction (HCV-VM-EXTRACT-002)  
**Thread:** Heber_Global_Roadmap  
**VM_VERSION:** 20260208-0030  
**Immutable:** Yes

---

## Data Center Cooling, Heat Recovery, Phase 2/3 Doctrine, & Global Strategic Roadmap

### Data Center Cooling Architecture

#### Primary System: Closed-Loop Geothermal Borefield
- **Technology:** Ground-source heat pump with depth-drilled wells (~300-500 m boreholes in northern Arizona geology)
- **Thermal Capacity:** Modeled for Phase 1 data center cluster cooling demand (estimated 50-100 MW thermal extraction)
- **Operational Profile:** Year-round baseload cooling source with relatively constant ~50-55°F ground temperature at depth
- **Advantage:** Eliminates seasonal swings; highly efficient vs. air-cooled or tower-cooled systems in Arizona high-temperature summers

#### Secondary System: Modular Central Ammonia (NH3) Cooling Plant
- **Refrigerant:** Ammonia selected for high thermodynamic efficiency and low GWP (no ozone/climate impact)
- **Redundancy:** N+1 configuration (multiple compressor trains; loss of one unit does not degrade DC SLAs)
- **Modularity:** Central plant sized for Phase 1; additional NH3 modules added in Phase 2/3 without redesign
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

3. **Compressors Last** (NH3 Plant Active)
   - Daytime peak cooling demand or geothermal capacity exceeded → NH3 compressors activated
   - Estimated 10-20% of annual hours; primarily summer daytime

#### Net Effect
- **Energy Efficiency:** Annual cooling energy reduced 20-30% vs. all-air or all-tower-cooled systems
- **Cost Reduction:** Lower operational electricity cost for DC climate control
- **Thermal Stability:** Constant geothermal source temperature improves server reliability vs. fluctuating ambient

### Heat Recovery Water Loop (HRWL) Doctrine

#### Formalized Policy
- **Governance Document:** HC-MGD-001 Appendix (heat recovery management)
- **Adoption Date:** 2026-02-08
- **Authority:** Binding operational and design constraint for all Heber Campus thermal systems

#### HRWL Architecture

**Isolated Loop: HX-Only Design**
- Dedicated closed-loop circuit carrying hot condensate from refrigeration plant and reject heat from electrical equipment
- No direct integration or cross-flow between HRWL and process loops
- All heat transfer through isolated heat exchangers (HX) only; prevents contamination and operational coupling

**Thermal Buffer Tank**
- Intermediate storage vessel (estimated 500-1,000 m³ volume) at HRWL circuit midpoint
- Purpose: Smooth mismatch between heat generation (compressor operation, IT equipment) and heat demand cycles
- Allows short-duration peak loads without requiring simultaneous downstream consumption
- Reduces cycling on compressors and process equipment

#### Heat Sink Registry & Allocation Control

**Heat Sink Registry Concept**
- Formal list of all approved thermal loads that may consume HRWL heat:
  - SOEC feed water preheating (primary industrial heat sink)
  - Biomass plant steam conditioning (secondary)
  - Campus space heating (minimal in Arizona climate; winter-only)
  - Process water heating (if applicable; e.g., washdown water at fuels facility)

**Allocation Rules**
- MECSAI (Multi-Energy Campus Supervisory Architecture Intelligence) system manages HRWL dispatch
- MECSAI may only distribute recovered heat to sinks on approved registry
- Heat allocation among registered sinks performed dynamically based on demand signals
- **Transaction Prohibition:** MECSAI cannot unilaterally alter loop topology, add new sinks, or bypass registry

**Rationale:** Prevents ad-hoc thermal connections that could:
- Introduce contamination from untested fluids
- Create uncontrolled feedback coupling (e.g., heating SOEC too much → electrolyzer efficiency loss → negative loop)
- Violate insurance liability underwriting (unvetted thermal interfaces)

### Phase 2 Operating & Financial Doctrine (HC-PH2-001 Rev A)

#### Governance Status
- **Document:** HC-PH2-001 Revision A (formal policy)
- **Scope:** Phase 2 site planning, construction, commissioning, and 25-year operations baseline
- **Authority Level:** Governance-binding (all projects must align or seek explicit variance approval)

#### Operational Philosophy

**DC + Solar-Led Expansion**
- Phase 2 growth prioritizes data center buildout (DC2 building) and solar PV expansion (~3.5 GW additional)
- SMR and SOEC follow to support expanded DC cooling and H₂ production
- Rationale: DC and PV both have predictable capital recovery economics; SMR/SOEC deployment follows after cash-flow accumulation

**Night Treated as Managed Scarcity Window**
- Definition: ~6-8 PM to ~6-8 AM (winter shorter, summer longer)
- Constraint: Night consumption must rely on battery (depleted by design) + firm generation (SMR/biomass at capacity limits)
- No automatic fuel startup for load balancing; instead, load shaping enforced to fit available supply

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
- Method: Current density modulation only (electrolyzer input voltage/current reduced but stack temperature kept stable)
- **Constraint:** No thermal cycling (avoid freeze-thaw damage in SOEC stacks)
- Result: Night H₂ production continues but at reduced rate; storage feeds daytime synfuel synthesis

**Shift 10-20 MW Chemical Compression/Transfer to Daylight**
- Hydrogen compression (gas→liquid or gas→high-pressure tank), CO2 liquefaction, synfuel product pumping—all high-power industrial operations
- Night approach: Run at daytime operating point only; minimize night operation
- Daytime approach: Accumulate daytime power availability (excess PV after DC/SOEC primary loads) into compression/transfer operations
- Result: ~10-20 MW aggregate load shifted from night to daytime peak windows

### Phase 2 Power Export Doctrine (Planning)

#### Firm Export Limit: 50 MW 24/7

**Definition:** Contractual obligation to deliver minimum 50 MW to regional grid at all hours, backed by guaranteed supply (SMR + biomass)
- SMR baseline: 320 MW (4 units × 80 MW) electric capacity (constrained to 25 MW reserve)
- Biomass baseline: ~100 MW electric output (constrained to 25 MW reserve)
- Available for firm export: 50 MW maximum at any hour

**Rationale:**
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

**Policy:** If maintaining 50 MW firm export requires:
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

**Data Center Growth**
- Phase 1: 1 DC building (200-300 MW IT electrical load)
- Phase 2: 2 DC buildings (400-600 MW total)
- Phase 3: 4 DC buildings (800-1,200 MW total)
- **Ultimate (Phase 3 buildout): 16 DC buildings possible** (3.2-4.8 GW IT electrical load infrastructure)

**Solar Expansion**
- Phase 1: ~1.5 GW
- Phase 2: ~1.5 +3.5 GW = 5 GW cumulative
- Phase 3: 5 GW + expansion → up to 5 GW sustained (land constraints limit further in Arizona, may shift to Southwest replication sites)

**Refinery Scaling**
- Phase 1-2: 18,000 bpd baseline
- Phase 3: scale toward 100,000 bpd via:
  - SOEC H₂ production scaling (457 t/day → 1,500 t/day)
  - CO₂ sourcing expansion (40,000 t/day required)
  - SMR/SOEC modular replication (additional reactors added, not monolithic expansion)

**SMR/SOEC Replication**
- Phase 1: 4 SMR units + 3-4 SOEC modules planned
- Phase 2: Replicate modular pattern (no new designs)
- Phase 3: Additional SMR/SOEC trains added if Phase 2 performance validates economics and regulatory approvals obtained

#### Gating Criteria: Phase 2 Performance Triggers

**Validation Requirements Before Phase 3 Commitment:**
1. SMR operability: >90% average availability over 3 years Phase 2 operation
2. SOEC uptime: >85% hydrogen production vs. target, <2% unplanned downtime
3. Data center PUE (Power Usage Effectiveness): <1.3 demonstrated over 2 high-cooling-demand seasons
4. H₂ cost competitiveness: Landed cost <$2.50/kg (all-in including capital recovery)
5. Synfuel production margin: >15% gross margin on Jet-A/Diesel sales
6. Regulatory: SMR licensing/operations approval + environmental permits for expanded scale

**Consequence of Trigger Failure:**
- Phase 3 expansion delayed or scaled back
- Alternative technology substitution evaluated (different SMR design, different thermal source, etc.)
- No automatic commitment to 100,000 bpd or 16-DC-building ultimate

### Global 100-Year Roadmap (Conceptual, Non-Binding)

#### Strategic Vision (Timeframe: 2026-2126)

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
- Integrate desalination for water supply and export water as additional revenue
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

#### Fossil Fuel Role (Explicit Assumption)

**Key Statement:** Fossil fuels decline in dependence but are NOT assumed eliminated
- Backup SMR reactors provide firm power where solar insufficient (Phases 1-2 baseline)
- Biomass (renewable) replaces coal but **not assumed globally displaced**
- Synthetic fuels (H₂ + CO₂ → Jet-A/Diesel) themselves produced at Heber, **not fossil-free**—they require energy input (net zero only if production powered entirely by renewables)
- **Planning assumption:** Decarbonization path emphasizes intensity reduction, not elimination—civilization may still require chemical fuels for aviation/shipping even in 2100+

### Data Center Phasing & Load Variability

#### Sequential Commissioning Approach

**Phase 1-3 Building Rollout (Planning)**
- Phase 1: 1 DC building commissioned (2027-2028 estimated)
- Phase 2: Add 1 more (DC2), total 2 buildings (2030-2032 estimated)
- Phase 3-A: Add 2 more (DC3, DC4), total 4 buildings (2035-2037 estimated)
- Phase 3-B (Ultimate): Add up to 12 more buildings, total 16 (buildout by 2045+)

**Demand-Driven Commissioning**
- Each DC building commissioned only when anchor tenant contracts obtained
- No speculative buildout; each building financed by customer contracts before steel
- Delivers site scaling without stranded capacity risk

#### Data Center Load Modeling: Variable via PUE and Workload Shifting

**PUE (Power Usage Effectiveness) Modeling**
- Definition: Total campus power / IT electrical load = PUA / ITLoad
- Phase 1 Target: <1.25 PUE (cooling + overhead ~25% vs. IT workload)
- Phase 2 Target: <1.23 PUE (economies of scale in cooling/air handling)
- Phase 3 Target: <1.20 PUE (multiple DC buildings share cooling infrastructure)

**Workload Shifting Variability**
- Cloud tenants permitted to migrate workloads between Heber DC buildings and other regions
- Annual workload profile: 60-80% minimum (stable baseload), 20-40% variable (migrates seasonally or by demand)
- Campus planning assumes 70% utilization year-round (conservative) but models 40-100% operational range

**Impact:** Night load reduction strategies must account for workload variability; typical night reduction may vary 30-50% depending on customer demand patterns

### Biomass Feedstock Planning Basis (Phase 1-2)

#### Baseline Requirement

**Daily Dry Mass Input:** 7,000 tons/day dry biomass
- HRSG [Heat Recovery Steam Generator] conversion: ~7,000 tons/day → ~100 MW thermal output (assumed 6.5 GJ/ton feedstock × 0.85 boiler efficiency)
- Syngas/chemical production: ~2-3 MW thermal equivalent for drying, preprocessing, handling

**Supply Source:** External partnership (Navajo Nation initial target, plus regional forestry residue dealers)
- No on-site cultivation or farming
- Contract pricing baseline: ~$6/ton delivered (stress-test ranges: $4-8/ton)
- Annual biomass cost: 7,000 t/day × 365 days × $6/t = **$15.3M/year baseline**

#### Sustainability & Supply Risk

**Supply Resilience:** Multiple vendors contracted; no single-source dependency
- Primary: Navajo Nation agricultural/forestry partnership (estimated 4,000-5,000 t/day)
- Secondary: Regional biomass aggregators (Arizona, New Mexico) (estimated 2,000-3,000 t/day)
- Emergency: Purchased green waste / urban forestry (short-term only; higher cost)

**Carbon Accounting:** Biogenic CO₂ from biomass combustion counted as carbon-neutral (replanted/regrown feedstock assumption)
- Does not contribute to carbon footprint of synfuel products
- Allows H₂ + biomass-CO₂ → Jet-A/Diesel to claim ~50% carbon intensity reduction vs. conventional refining

### Coastal Deployment Option: Desalination Revenue

#### Seawater Desalination Integration (Future Sites)

**Technology:** Reverse osmosis (RO) or multi-effect distillation (MED) co-located with coastal Heber-class campus
- Process water demand: ~500-1,000 m³/day for cooling, industrial use
- If overbuilt (2,000-3,000 m³/day capacity), excess fresh water sold to local water authorities or industrial users

**Revenue Model:** Water sales as tertiary revenue stream (after power + fuels + data center)
- Desalinated water wholesale price: ~$0.50-1.00/m³ depending on region and contract terms
- 1,500 m³/day × $0.75/m³ × 365 days = **$410K/year additional revenue** (modest but non-trivial)

**Efficiency Coupling:** Campus waste heat from HRSG/SMR employed to drive thermal distillation or reduce RO energy consumption
- Estimate: 10-30% reduction in desal electricity demand via thermal integration

### Phase 3 Carbon Sourcing (Long-Horizon Variable)

#### CO₂ Supply Challenge: 40,000 t/day Required for 100,000 bpd

**Working Planning Split (Modeling Basis Only; Not Binding)**
- **40% Biogenic CO₂ Capture:** From biomass combustion HRSG exhaust (direct capture, minimal cost)
- **20% Fermentation CO₂:** From beer/ethanol production, agricultural facilities (regional partnership sourcing)
- **40% Direct Air Capture (DAC):** Atmospheric CO₂ via advanced separation (emerging technology; high energy cost)

**CO₂ Production Rate Modeling**
- Phase 1-2: 7,000-8,000 t/day biomass → ~2,500-3,000 t/day CO₂ captured (single HRSG stream)
- Phase 3: Add fermentation sources (regional ethanol producers) → +1,000 t/day
- Phase 3: Deploy DAC units → remaining 35,000+ t/day required (estimated 10-20 MW electrical equivalent for advanced separation)

**Long-Horizon Risk:** DAC technology not yet cost-competitive; Phase 3 CO₂ sourcing contingent on:
1. DAC cost reduction to <$150/ton CO₂ (vs. current $200-400/ton)
2. Availability of waste heat sources for DAC energy efficiency
3. Regulatory support for CO₂ utilization (tax credits, carbon accounting)

**Contingency:** If DAC infeasible, Phase 3 refinery capped at 50,000-60,000 bpd using biogenic + fermentation CO₂ only

### Revenue Strategy Doctrine (Clarified)

#### Primary Profit Engines

**1. Refined Fuels (Diesel, Jet-A, LPG)**
- Gross margin target: 15-20% (synfuel production cost vs. market price)
- Phase 1-2 capacity: 18,000 bpd → ~$30-40M annual revenue (at $50/barrel average)
- Phase 3 capacity: 100,000 bpd → ~$170-200M annual revenue
- Market position: Premium price for low-carbon/synthesized fuels (avoid commodity competition)

**2. Data Center Services**
- Lease rates: $6,000-8,000/kW annual commitment (IT equipment load, colocation service)
- Phase 1: 300 MW IT load → $1.8-2.4B annual revenue (at full utilization)
- Phase 2: 600 MW → $3.6-4.8B annual
- Phase 3: 1.2 GW → $7.2-9.6B annual (largest revenue stream)
- Margin: 40-50% gross (power + cooling + facilities cost ~50-60% of revenue)

#### Stabilizing Backbone

**Power Exports (Firm + Flexible)**
- Firm 50 MW @ $70/MWh = $307M annually
- Flexible daytime 400 MW average @ $40/MWh = $140M annually
- Total power revenue: ~$450M/year Phase 2 (modest vs. DC/fuels)
- Role: Provides revenue stability when customer demand fluctuates; smooths earnings

#### Financial Posture

**Firm Power Commitments: Keep Small with Optional Flexible Upside**
- Conservative approach: 50 MW firm committed (backed by SMR/biomass) only
- Additional capacity (up to 1.5 GW potential) kept flexible for:
  - Internal load growth (SOEC expansion, DC growth, VVLS demand)
  - Spot market sales (higher volatility but also higher marginal price)
  - Emergency/backup (reserve capacity not committed to customers)

**Rationale for Upside Structure:**
- Avoid locking in low-price long-term contracts that constrain operational flexibility
- Preserve ability to shift generation to internal high-value uses (H₂ production, DC cooling) when profitable
- Allow gradual market entry; reduce risk of unilateral contract default if SMR/biomass experience downtime

**Net Effect:** Phase 2 power revenue ~$450M + refined fuels $30-40M + data center $3.6-4.8B = **~$4.1-5.3B gross revenue**, driving strong project returns with modest firm export exposure
