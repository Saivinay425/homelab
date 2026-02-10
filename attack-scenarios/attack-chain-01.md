## Attack Chain 01 – Local Privilege Escalation and Post-Exploitation

### Timeline
1. Multiple failed authentication attempts observed (Event ID 4625)
2. New local user account created (Event ID 4720)
3. Newly created user added to Administrators group (Event ID 4732)
4. Encoded PowerShell execution detected (Sysmon Event ID 1)
5. DNS queries observed from system processes (Sysmon Event ID 22)

### Assessment
This activity indicates potential unauthorized access followed by
persistence, privilege escalation, and post-compromise execution.

### Severity
Critical

### MITRE ATT&CK
- T1078 – Valid Accounts
- T1136 – Create Account
- T1548 – Abuse Elevation Control Mechanism
- T1059.001 – PowerShell
- T1071 – Application Layer Protocol
