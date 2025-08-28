# QR - 003 — MFA Push Bombing (Single Username)

**Description:** Detects ≥8 MFA push challenges/denials for the same username within 5 minutes (optionally from multiple IPs/devices). This pattern is typical of “MFA fatigue/push bombing,” where an attacker spams prompts hoping the user will accept one.

**Miter Attack Framework:** 
- **Tactic:** Credential Access (TA0006)
- **Technique:** T1621 – Multi-Factor Authentication Request Generation
- **Sub-technique:** T1111 – Multi-Factor Authentication Interception
- **Data Source:** Identity provider authentication logs (Okta, Microsoft Entra ID/Azure AD Sign-in, Duo, Google, etc.)

**Rule Description:** 
- Apply QRCE - 003 - MFA Push Bombing - Single Username on events which are detected by the Local system
- and when an event matches any of the following BB:CategoryDefinition: Authentication MFA Challenge, BB:CategoryDefinition: Authentication MFA Denied (map your IdP DSM fields)
- and when at least 8 events are seen with the same Username in 5 minutes
- and NOT when the Source IP is contained in Authorized Auth Sources (Reference Set) (optional tuning)
- and NOT when the Username matches ^svc_|^srv_|^bot_|^test (adjust to your environment)
- (optional) and when Device/Client differs across ≥3 events in the same window (helps surface bombardment from multiple hosts/VPN exits)

**Rule Actions:**
- Force the detected Event to create a NEW offense, select the offense using Username
- Annotate this offense with: QRCE - 003 - MFA Push Bombing - Single Username
- Add Username to Reference Set: MFA Fatigue Users (TTL: 24h) (enables follow-on correlation & temporary suppression/tuning)

Rule Responses
- Dispatch New Event
- Event Name: MFA Push Bombing – Single Username
- Event Description: This rule detects repeated MFA prompts/denials for a single account in a short time window—strong indicator of MFA push-bombing.
- Severity: 7 Credibility: 10 Relevance: 10
- High-Level Category: Authentication
- Low-Level Category: MFA Challenge/Deny
- Annotate the offense with: QRCE - 003 - MFA Push Bombing - Single Username
- Force the dispatched event to create a NEW offense, select the offense using Username
