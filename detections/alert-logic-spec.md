Rule A1 (4625)
Baseline observed: 0 events in 24h
Chosen threshold: 10 in 5 minutes
Reason: Baseline is 0; threshold avoids noise but detects brute force

Rule B1 (4720)
Baseline observed: 0 events in 24h
Chosen threshold: Any occurrence (1 event)
Reason: New user creation is high-impact and rare; every event must alert

Rule C1 (4732)
Baseline observed: 0 events in 24h
Chosen threshold: Any occurrence (1 event)
Reason: Privilege escalation event; extremely sensitive and rare

Rule D1 (1)
Baseline observed: 0 suspicious executions in 24h
Chosen threshold: Any occurrence (1 event)
Reason: Encoded/obfuscated PowerShell is high-risk execution behavior

Rule E1 (22)
Baseline observed: 10 events in 24h
Chosen threshold: 200 events within 10 minutes
Reason: Threshold is far above normal usage; detects beacon-like behavior

## Severity Classification
4625 Brute Force → Medium  
Reason: Authentication attack attempt; may be noise but indicates credential abuse risk.

4720 New User Created → High  
Reason: Persistence technique; rare and high-impact if unauthorized.

4732 Admin Group Add → Critical  
Reason: Direct privilege escalation; full system compromise risk.

Sysmon Encoded PowerShell → High  
Reason: Strong execution indicator; commonly used for malware or lateral movement.

High DNS Rate (Beacon-like) → Medium  
Reason: Possible C2 behavior but requires investigation to confirm malicious intent.
