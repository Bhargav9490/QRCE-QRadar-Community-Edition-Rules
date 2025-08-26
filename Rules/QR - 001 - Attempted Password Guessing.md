# QR - 001 — Attempted Password Guessing (Single Username)

**Description:** Detects ≥5 failed logins for the same username within 1 minute. This is a high-signal indicator of brute-force attempts against an account. (Based on your uploaded rule content.)

**ATT&CK:** 
- **Tactic:** Credential Access (TA0006)
- **Technique:** T1110 – Brute Force
- **Sub-technique:** T1110.001 – Password Guessing
- **Data Source:** Authentication logs (failed logon events)
