# OWASP ZAP — Artifacts (DVWA Lab)

This directory contains artifacts generated with **OWASP ZAP** during the practical audit performed on **DVWA** (lab environment inside a VM with Kali Linux).

> Note: All tests were conducted in a controlled environment (localhost / VM). The included reports and images are for **educational purposes**.

## 📂 Structure
- `images/` — key screenshots (ZAP alerts, request/response, context).  
- `reports/` — exports (HTML / JSON) of the ZAP scan.  
- `tools/` — helper scripts to sanitize/optimize images (optional).  

## 📄 Included Files (examples)
- `images/01_zap_finding_xss_reflected.png` — ZAP Alert: Reflected XSS.  
- `images/02_zap_request_response_example.png` — HTTP request/response of the finding.  
- `images/03_zap_context_scope.png` — ZAP context/scope configuration.  
- `images/04_zap_report_summary.png` — Fragment of the exported report.  
- `reports/zap_report_sanitized.html` — Exported report (without sensitive data).  
- `reports/zap_findings.json` — JSON export (optional).  

## 🖼️ How to reference these images in the main README
Example in your main README:

```md
### OWASP ZAP — Key Findings
![ZAP - XSS finding](zap/images/01_zap_finding_xss_reflected.png)
