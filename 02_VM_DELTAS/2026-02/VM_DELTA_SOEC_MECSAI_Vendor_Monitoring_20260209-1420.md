## DELTA BEGIN

[2026-02-09] Decision: SOEC vendor-supplied instrumentation is treated as minimum safe-operability; MECSAI requires additional observability beyond typical OEM scope.
[2026-02-09] Constraint: MECSAI observability must not modify the SOEC stack or OEM safety loops; OEM PLC remains safety authority; MECSAI operates as read-only supervisory monitoring with upstream setpoint requests.
[2026-02-09] Decision: Additional monitoring sensors should be specified as OEM-installed or OEM-approved where possible to avoid warranty impact; vendor integration into build spec is pursued for large-volume orders.
[2026-02-09] Definition: Two-tier vendor deliverable created for MECSAI monitoring - (1) Minimal option sheet mandatory for bid qualification and (2) Desired option sheet for preferred partnership configuration.
[2026-02-09] Requirement: Minimal option sheet includes OEM-installed/approved sensors for stack inlet/outlet temperatures and pressures (H2 and O2 sides), stack average temperature, DC bus voltage/current, and hydrogen purity or crossover indication.
[2026-02-09] Requirement: Minimal option sheet requires read-only raw data access (not alarm-only), minimum 1 Hz sampling, and standard industrial protocols (Modbus TCP, OPC-UA, EtherNet/IP acceptable).
[2026-02-09] Requirement: Minimal option sheet includes explicit warranty carve-outs permitting external monitoring, logging/analytics, and upstream derating commands without voiding OEM warranty.
[2026-02-09] Requirement: Desired option sheet requests enhanced OEM-installed instrumentation for thermal gradients (multi-point thermocouples), stack-level electrical sense (voltage taps and high-resolution current), gas quality (H2 moisture ppm, O2 humidity, DP decay ports), and non-intrusive mechanical sensing (vibration; optional acoustic).
[2026-02-09] Requirement: Desired option sheet requests higher-rate data streams (electrical >=10 Hz; thermal >=2 Hz), synchronized timestamps, and exposure of diagnostic flags as variables.
[2026-02-09] Governance: Vendor interface support requested via an Interface Control Document (ICD) defining allowable external command envelope and data mapping for MECSAI integration.
[2026-02-09] Partnership path: MECSAI compatibility and compliance positioning to be offered as a co-marketing option for vendors (MECSAI-Compatible SOEC Platform) without exclusivity.

## DELTA END
