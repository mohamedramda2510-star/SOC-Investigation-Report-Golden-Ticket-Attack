# SOC-Investigation-Report-Golden-Ticket-Attack

SOC Investigation Report – Golden Ticket Attack

Platform: LetsDefend
Lab: Golden Ticket
Category: Active Directory / Kerberos Attack Investigation
Status: Completed

---

1. Investigation Overview

Investigated suspicious activity targeting an Active Directory Domain Controller (DC). The investigation focused on identifying the attacker's initial access to a service account, analyzing Kerberos authentication events, and tracing the AS-REP Roasting and Golden Ticket attack activities.

2. Investigation Findings

Investigation Item| Findings
First Service Account Access (UTC)| "2024-10-05 16:50:29"
Compromised Service Account| "SQLService"
Attacker IP and Port| "192.168.110.129:48858"
AS-REP Roasting Target| "Corrado"
AS-REP TGT Request (UTC)| "2024-10-05 14:42:44"
Golden Ticket Target| "Administrator"
Time using the Golden Ticket? 2024-10-05 17:57:03 UTC
3. Analysis & Investigation

- Analyzed Windows Security Event Logs to investigate suspicious Kerberos activity.
- Identified Event ID 4768 (Kerberos Authentication Service) and Event ID 4769 (Kerberos Service Ticket Operations).
- Identified the compromised service account and the attacker's source IP and port.
- Correlated authentication events to reconstruct the attack timeline.
- Identified the Administrator account as the target of the Golden Ticket attack.

4. Evidence

Evidence 01: Initial service account access timestamp.

<img width="627" height="433" alt="Screenshot 2026-11-18 154100" src="https://github.com/user-attachments/assets/474dc9a2-7c99-4b27-aca6-79fde0b97afb" />


Evidence 02: Compromised service account identification.

<img width="827" height="431" alt="Screenshot 2026-11-18 153028" src="https://github.com/user-attachments/assets/aeda0c9d-044e-4019-b8b4-ea612ad74658" />


Evidence 03: Attacker source IP and port.

<img width="622" height="414" alt="Screenshot 2026-11-18 153249" src="https://github.com/user-attachments/assets/c2ec8742-54e6-4f1a-9874-b30badda2ad5" />

Evidence 04: AS-REP Roasting target account.

<img width="610" height="401" alt="Screenshot 2026-11-18 153431" src="https://github.com/user-attachments/assets/cdfada4b-6c4f-439b-83cf-2f1ff3a50f0b" />


Evidence 05: AS-REP TGT request timestamp.
<img width="614" height="420" alt="Screenshot 2026-11-18 153456" src="https://github.com/user-attachments/assets/fddd0075-5114-4eb7-be7d-e52a0fddacd0" />


Evidence 06: Golden Ticket target account (Administrator).
<img width="612" height="439" alt="Screenshot 2026-11-18 153912" src="https://github.com/user-attachments/assets/9b714005-5d39-4f84-8ded-75c746a15081" />

Evidence 07:At what time did the attacker try to log in using the Golden Ticket?
Answer Format: (YYYY-MM-DD HH:MM:SS UTC)

<img width="621" height="428" alt="Screenshot 2026-11-18 153853" src="https://github.com/user-attachments/assets/191ea4ac-4c36-485e-907a-a252b8b09082" />



5. Conclusion

Successfully investigated the simulated Kerberos attack scenario, identified the compromised service account, traced the attacker's activity, and determined the targeted Domain Administrator account.

Key Skills: Windows Event Log Analysis | Active Directory | Kerberos | AS-REP Roasting | Golden Ticket Detection | Incident Investigation

Result: Lab Successfully Completed
