# QR - 001 — Attempted Password Guessing (Single Username)

**Description:** Detects ≥5 failed logins for the same username within 1 minute. This is a high-signal indicator of brute-force attempts against an account. 

**Miter Attack Framework:** 
- **Tactic:** Credential Access (TA0006)
- **Technique:** T1110 – Brute Force
- **Sub-technique:** T1110.001 – Password Guessing
- **Data Source:** Authentication logs (failed logon events)

**Rule Description:** 
- Apply QRCE - 001 - Attempted Password Guessing - Single Username on events which are detected by the Local system
- and when an event matches any of the following BB:CategoryDefinition: Authentication Failures
- and when at least 5 events are seen with the same Username in 1 minutes

**Rule Actions:**
- Force the detected Event to create a NEW offense, select the offense using Username
- Annotate this offense with: QRCE - 001 - Attempted Password Guessing - Single Username

Rule Responses
- Dispatch New Event
- Event Name: Attempted Password Guessing - Single Username
- Event Description: This rule is designed to detect 5 failed authentication attempts in a 1 minute period. This type of activity could indicate a brute force attempt against an account is occurring.
- Severity: 6 Credibility: 10 Relevance: 10
- High-Level Category: Authentication
- Low-Level Category: User Login Failure
- Annotate the offense with QRCE - 001 - Attempted Password Guessing - Single Username
- Force the dispatched event to create a NEW offense, select the offense using Username
