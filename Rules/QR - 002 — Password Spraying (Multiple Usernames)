# QR - 002 — Password Spraying (Multiple Usernames)

**Description:** Detects ≥10 failed logins across ≥5 distinct usernames from the same source IP within 5 minutes. This pattern is typical of password spraying (few common passwords tried against many accounts to avoid lockouts).

**Miter Attack Framework:** 
- **Tactic:** Credential Access (TA0006)
- **Technique:** T1110 – Brute Force
- **Sub-technique:** T1110.003 – Password Spraying
- **Data Source:** AAuthentication logs (failed logon events)

**Rule Description:** 
- Apply QRCE - 002 - Password Spraying - Multiple Usernames on events which are detected by the Local system
- and when an event matches any of the following BB:CategoryDefinition: Authentication Failures
- and when at least 10 events are seen with the same Source IP and different Username in 5 minutes
- and NOT when the Source IP is contained in Authorized Auth Sources (Reference Set) (optional tuning)
- and NOT when the Username matches ^svc_|^srv_|^bot_|^test (adjust to your environment)

**Rule Actions:**
- Force the detected Event to create a NEW offense, select the offense using Source IP
- Annotate this offense with: QRCE - 002 - Password Spraying - Multiple Usernames
- Add Source IP to Reference Set: Password Spraying Sources (TTL: 24h) (helps follow-on correlation)

Rule Responses
- Dispatch New Event
- Event Name: Password Spraying – Multiple Usernames
- Event Description: This rule detects multiple authentication failures targeting many different usernames from a single source in a short time window—strong indicator of password spraying.
- Severity: 6 Credibility: 10 Relevance: 10
- High-Level Category: Authentication
- Low-Level Category: User Login Failure
- Annotate the offense with: QRCE - 002 - Password Spraying - Multiple Usernames
- Force the dispatched event to create a NEW offense, select the offense using Source IP
