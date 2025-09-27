# PoC — Proof of Concept (laboratory)

This directory contains Proofs of Concept (PoCs) documented from audits
performed on **DVWA** (lab environment inside a VM).

> ⚠️ Warning: These PoCs are for educational use only in controlled environments.
> Do not run payloads or scripts against systems you do not own or that you do not have explicit authorization to test.

## Structure
- `xss_poc.md` — Cross-Site Scripting (Reflected XSS) PoC.  
- `sql_injection_poc.md` — SQL Injection PoC (DVWA example).  
- `sanitized_payloads.txt` — example payloads (sanitized and commented).  
- `other_pocs/` — optional folder for additional PoCs (CSRF, RCE, etc.).

## Conventions
- Use clear filenames: `xss_poc.md`, `sqli_poc.md`, etc.  
- Each PoC should include: description, environment, reproducible steps, expected evidence, and mitigation.  
- Do NOT include automated exploits against third parties. If including scripts, keep them educational and well-commented.

## Best practices
1. State DVWA security level used (e.g., `low`, `medium`, `high`).  
2. Note tool versions when relevant (ZAP, Burp, DVWA).  
3. Keep `sanitized_payloads.txt` minimal and explained.  
4. If adding screenshots, store them in `poc/images/` and reference them from the PoC docs.
