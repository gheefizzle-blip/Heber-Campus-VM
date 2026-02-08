# CHAT_HCV-VM-EXTRACT-002_20260208-1148

**Snapshot Timestamp:** 2026-02-08 11:48 UTC  
**Source:** ChatGPT Extraction (HCV-VM-EXTRACT-002)  
**Thread:** HCV-VM-EXTRACT-002  
**VM_VERSION:** 20260208-1148  
**Immutable:** Yes

---

## DC Fault Protection Autonomy, Hardware-Enforced Clearing & Software Prohibition Policy

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
   - SMR reactor DC output : SSCB before main bus coupling
   - **Purpose:** Protect entire campus power system and external grid connection

#### Autonomous Detection Hardware

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

### Software System Constraints: MECSAI & SCADA as Read-Only Observers

#### MECSAI Functional Redesignation (Formal Policy)

**Former Authority (Pre-Delta 17)**
- MECSAI issued dispatch commands to generation sources
- MECSAI controlled breaker state (open/close commands)
- MECSAI participated in real-time peak shaving via equipment shutdown

**New Authority (Post-Delta 17 - Formal Constraint)**

**Permitted Functions:**
1. **Monitoring:** Real-time observation of all fault events (SSCB trip signals, arc detection triggers)
2. **Analytics:** Aggregation of fault statistics (fault rate per zone, seasonal trends, correlation with load patterns)
3. **Reporting:** Dashboard visualization of protection device health, predicted maintenance scheduling
4. **Trend Analysis:** Machine learning on historical fault data to identify emerging failure patterns (arc frequency increase = aging equipment signal)

**Explicitly Prohibited Functions:**
1. **Breaker Commands:** MECSAI cannot issue "close breaker" or "open breaker" commands to any protection device
2. **Override Authority:** MECSAI cannot override hardware fault lockouts (e.g., "allow SSCB to re-close even though fault signature detected")
3. **Reset Functions:** Cannot reset protection device latches or clear fault memory without manual technician action
4. **Automatic Reclosure:** Cannot initiate automatic breaker re-closure after fault clearing (prevents repeated arc formation if fault persists)

**Operational Consequence:**
- After SSCB clears fault, zone/device remains de-energized until manual field technician inspects and resets breaker
- Data center cannot automatically restart rack after fault (requires ticket + physical visit)
- Electrolyzer cannot auto-restart module after high-current event (requires technician diagnosis)
- Site remains in "safe" de-energized state until human verification of fault resolution

#### SCADA Role Redesignation (Formal Policy)

**SCADA Authority Shift:**
- **Old Role:** SCADA issued load-shedding commands, breaker controls, generator start/stop sequencing
- **New Role:** SCADA is strictly read-only for fault event status

**SCADA Permitted Functions:**
1. **Fault Event Logging:** Capture timestamp, device location, fault type, SSCB clearing time from protection relay telemetry
2. **Status Indication:** Display breaker state (open/closed) and fault counter from devices (not state command authority)
3. **Alarms:** Generate operator notifications when fault rate exceeds threshold (e.g., >5 faults/hour indicates equipment degradation)
4. **Historical Data:** Archive all fault events for compliance logging and equipment warranty analysis

**SCADA Explicitly Prohibited:**
1. **Automatic Resets:** Cannot command protection device to re-close breaker
2. **Voltage/Frequency Control:** Cannot adjust setpoints on analog protection circuits
3. **Load Shedding:** Cannot shed customer loads in response to fault events (previously SCADA capability)
4. **Generation Control:** Cannot ramp generators up/down in reaction to detected faults

**Consequence:** Faults are logged and reported in real-time to operators, but system response is passive (no automated mitigation). Operators must manually intervene for recovery.

### Fault Scenario Examples: Hardware vs. Software Clearing

#### Scenario 1: Solar String Short-Circuit (Low-Voltage DC)

**Fault:** 1,000 VDC solar array string experiences internal breakdown (panel delamination, moisture ingress)

**With Hardware-Only Protection (Delta 17 - Compliant):**
1. **T=0 μs:** Fault inception; current begins rising
2. **T=5 μs:** Differential current sensor sampled by comparator; fault current detected (100 A vs. normal 20 A)
3. **T=8 μs:** Analog comparator output triggers SSCB gate drive cutoff
4. **T=10 μs:** MOSFET gate charge depleted; device blocks; current interrupted
5. **T=10-100 μs:** Arc voltage oscillations damped by suppression network
6. **T=100 μs:** Fault contained; adjacent strings unaffected
7. **T=1 ms - onward:** MECSAI observes fault event (via telemetry from SSCB relay), logs in analytics database, generates operator notification
8. **T=5 minutes:** Technician receives alert, locates failed string, inspects for arc damage
9. **T=15 minutes:** Technician manually resets SSCB; string re-energized after clearance

**With Software-Participated Clearing (Pre-Delta 17 - Non-Compliant):**
1. **T=0 μs:** Fault inception
2. **T=100 μs:** MECSAI microprocessor samples ADC input, detects overcurrent signal
3. **T=500 μs:** MECSAI logic executes, calculates fault location, issues breaker command via CAN bus
4. **T=1000 μs:** Communication delay; command reaches breaker control module
5. **T=1200 μs:** Breaker gate drive receives command, begins switching off
6. **T=1500 μs:** Gate charge depletion; arc initiation
7. **T=1500-3000 μs:** Arc burns; energy released; adjacent strings experience voltage transient stress
8. **T=3000+ μs:** Fault finally interrupted; collateral damage to neighboring equipment
9. **Outcome:** Primary fault + secondary cascading failures; higher repair cost; longer outage

**Key Difference:** 1.5 ms vs. 10 μs clearing time = 150× more energy released in arc. Hardware autonomy prevents cascade.

#### Scenario 2: Battery Pack Shunt Fault (Medium-Voltage DC)

**Fault:** 480 VDC battery pack internal cell short develops during discharge (dendrite formation in lithium cell)

**With Hardware-Only (Delta 17 - Compliant):**
1. **T=5 μs:** SSCB detects 100 kA inrush (normal charge current: 20 kA)
2. **T=15 μs:** Gate drive actuation begins
3. **T=20 μs:** SSCB blocks; arc suppression network absorbs transient
4. **T=100 μs:** Fault cleared; BESS isolated from main bus
5. **T=500 μs+:** MECSAI reads fault telemetry, alerts operator to battery degradation
6. **T=5 minutes:** Operator inspects battery state-of-health logs; determines cell failure imminent
7. **T=24 hours:** Battery pack scheduled for capacity test; cell diagnosed failed; replacement ordered

**Outcome:** Rapid isolation prevents HVDC backbone from experiencing voltage sag. Timely detection of cell failing before catastrophic failure.

**With Software Clearing (Non-Compliant):**
1. **T=0-1000 μs:** Fault energy released; arc burns across bus connectors
2. **T=1000-2000 μs:** Arc temperature vaporizes copper; two adjacent protection relays damage their sensing coils
3. **T=2000 μs:** Finally cleared by software command
4. **T=1-2 hours:** Technicians discover secondary damage to backup relays; require replacement
5. **T=24 hours:** Only one protection relay operating in that zone; redundancy lost

**Outcome:** Software delay caused secondary hardware damage and loss of protective redundancy.

### Cross-System Operational Consequences

#### Data Center Availability Impact

**Rack Fault Scenario (48 VDC Distribution):**
- 1,000-server data center rack experiences PDU short circuit
- **Hardware-protected outcome:** SSCB clears in 20 μs; rack de-energized; adjacent racks unaffected; cold shutdown graceful; tenant data safe
- **Software-cleared outcome:** 2-5 ms arc; voltage sag propagated to adjacent racks; soft errors in CPU caches; data corruption possible; loss of redundancy; recovery lengthy

**Policy Compliance:** Delta 17 prohibits software override of hardware protection, meaning data center rack **cannot** auto-restart after fault. Tenant receives ticket for technician-initiated recovery. SLA penalty imposed until manual inspection clears fault.

#### Electrolyzer Stack Protection

**Module Internal Arc (400 V DC Input):**
- SOEC stack experiences electrode breakdown (thermal shock; ice crystal formation in electrolyte)
- **Hardware clearing:** SSCB blocks <20 μs; arc contained within module compartment; adjacent modules continue operation; plant output reduced by 1/N but not halted
- **Software clearing:** Arc sustained 2-3 ms; thermal propagation to adjacent stack; oxygen compartment pressurization risk; potential rupture; plant emergency shutdown

**Policy Implication:** Electrolyzer plant cannot be "soft restarted" by MECSAI after fault. Must be manually powered-down, inspected, and reset by technician.

#### Reactor Secondary Power Loss

**Loss of Instrument & Control Power (480 VDC bus supplying reactor SCRAM system):**
- Fault on reactor aux bus
- **Hardware protection:** SSCB clears; SCRAM bus voltage supported by UPS backup; reactor continues stable operation on SMR #2 until repair completed
- **Software clearing:** Delay in fault clearing; voltage sag on SCRAM bus; SCRAM solenoid valve coils experience reduced holding current; risk of unintended insertion if mechanical vibration encountered

**Policy Requirement:** Delta 17 mandates hardware-only clearing for all reactor auxiliary systems. Software has no authority to delay or manage fault response.

### Fault Clearing Interaction with Load-Shedding (Clarification)

#### Previous Load-Shedding Strategy (Obsolete)

**Pre-Delta 17 Design:** When solar + battery insufficient to cover night load, MECSAI would:
1. Issue command to shed non-critical loads (e.g., electrolyzer ramp from 400 MW to 100 MW)
2. Defer data center computational workloads (delay batch jobs, pause non-critical services)
3. Temporarily disable HVDC export (fold power back to campus)

**Why No Longer Applicable:**
- Load shedding is a control action (MECSAI command -> equipment response)
- Fault clearing must be autonomous (hardware-only, no software commands)
- These are now orthogonal: Faults interrupt power immediately via protection devices; load management operates on uninterrupted power

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

### Fault Isolation Architecture: Zones & Cascading Protection

#### Three-Level Protection Hierarchy

**Level 1: Device Protection (Microsecond Scale)**
- Fault confined to single device (inverter, battery pack, electrolyzer module)
- SSCB clears; only that device de-energized
- Rest of system unaffected
- Example: Solar string fault → only that one combiner de-energized; other 99 strings continue

**Level 2: Zone Protection (Microsecond Scale, Higher Current Rating)**
- Device-level protection fails (SSCB stuck ON due to gate drive failure)
- Zone protection picks up; higher current SSCB actuates
- Entire zone (e.g., solar farm) isolated; backup zones (battery, reactor) supply campus
- Example: Combiner stuck closed, arc propagates to feeder line → zone SSCB clears feeder; solar farm isolated but site continues operation

**Level 3: Backbone Protection (>10 ms Timescale, Highest Current Rating)**
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

