# CHAT_HEBER_OSYE_ORBITAL_LOGISTICS_20260207-2314

**Snapshot Timestamp:** 2026-02-07 23:14 UTC  
**Source:** ChatGPT Extraction (HCV-VM-EXTRACT-002)  
**Thread:** HEBER_OSYE_ORBITAL_LOGISTICS  
**VM_VERSION:** 20260207-2314  
**Immutable:** Yes

---

## OSYE Orbital Logistics - Orbital Mechanics & Operations

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
