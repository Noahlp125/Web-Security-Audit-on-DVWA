# PoC: Cross-Site Scripting (Reflected XSS) — DVWA (Level: Low)

## Description
Educational PoC demonstrating a reflected XSS in DVWA. The goal is to show
how insufficient output encoding allows JavaScript injection that runs in the victim's browser.

## Environment
- DVWA in Docker inside a VM (Kali Linux)  
- DVWA Security: `low`  
- Tools: Browser (Firefox), OWASP ZAP / Burp Suite (optional)

## Target endpoint
/vulnerabilities/xss_r/


## Reproduction steps (manual)
1. Start DVWA (e.g., `docker compose up -d` using the repo's `docker-compose.yml`).  
2. Open: `http://localhost:<PORT>/vulnerabilities/xss_r/`.  
3. Ensure DVWA Security is set to `low`.  
4. In the **Enter your name:** field input the test payload:
   ```html
   <script>alert('XSS Exploited!');</script>
5.Click Submit.
6.Observe the alert('XSS Exploited!') popup — this confirms script execution.

Expected evidence

JavaScript alert in the browser (popup) or other visible JS execution.

In ZAP/Burp: the request containing the payload and the response reflecting it.

Mitigation

Validate and sanitize input (prefer whitelists).

Apply proper output encoding (HTML-encode user data before rendering).

Implement a strict Content-Security-Policy.

Use templating engines that escape output by default.

Notes

More complex payloads may require different encodings or browser settings.

Run these tests only in your lab (DVWA).


---

## `poc/sql_injection_poc.md`
```md
# PoC: SQL Injection — DVWA (Level: Low)

## Description
Educational PoC demonstrating a basic SQL Injection in DVWA. Shows how untrusted input
can manipulate SQL queries to expose or alter data.

## Environment
- DVWA in Docker inside a VM (Kali Linux)  
- DVWA Security: `low`  
- Tools: Burp Suite / ZAP / Browser

## Target endpoint (example)
/vulnerabilities/sqli/


## Reproduction steps (manual)
1. Start DVWA and navigate to the SQL Injection section.  
2. In the input field (e.g., `User ID`) enter: 1' OR '1'='1
3. Submit the form.  
4. If vulnerable, the application may return more rows than expected or behave incorrectly depending on the original query.

## Expected evidence
- Response contains data that should not be accessible for the given input.  
- In Burp/ZAP: the request with the payload and the response showing extra results.

## Mitigation
- Use parameterized queries / prepared statements.  
- Validate and sanitize user input.  
- Apply least-privilege DB accounts.

## Notes
- Don’t automate exploitation against systems you don’t own.  
- In DVWA `medium`/`high` levels, protections make these simple payloads ineffective.

