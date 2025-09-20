# Web-Security-Audit-on-DVWA
This project consists of a **web security audit** performed on **Damn Vulnerable Web Application (DVWA)** in a controlled environment using Docker and Kali Linux.   The goal was to practice vulnerability analysis techniques, get familiar with industry tools (**Burp Suite, OWASP ZAP**), and document the findings for educational purposes.

⚠️ **Warning:** This project was conducted in a controlled lab environment. It should not be applied in production environments without authorization.

## ⚙️ Test Environment
- **OS:** Kali Linux on VMware  
- **Vulnerable Application:** DVWA in Docker  
- **Tools:**
  - OWASP ZAP
  - Burp Suite Community Edition
  - Firefox

## 🛠️ Methodology
1. Lab setup using Docker.  
2. Passive and active scanning with OWASP ZAP.  
3. Traffic interception and analysis with Burp Suite.  
4. Identification of vulnerabilities and proof-of-concept (PoC) testing.

## 🚨 Detected Vulnerabilities
- ❌ **Missing security headers:** CSP, X-Frame-Options, X-Content-Type-Options.  
- 🍪 **Insecure cookies:** no HttpOnly, no SameSite.  
- 🕵️ **Information leakage:** Apache server version exposed.  
- ⚡ **Reflected Cross-Site Scripting (XSS)** at `http://localhost/vulnerabilities/xss_r/`.

## ✅ Recommendations
- Configure security headers (**CSP, X-Frame-Options, X-Content-Type-Options**).  
- Set secure cookie flags (**HttpOnly, SameSite, Secure**).  
- Avoid exposing server version information.  
- Implement input validation, sanitization, and output encoding to prevent XSS.

## 📚 Lessons Learned
- Importance of professional tools (**Burp Suite, OWASP ZAP**).  
- Real impact of vulnerabilities such as XSS or insecure cookies.  
- Managing lab environments with Docker for safe pentesting.  
- Technical challenges (permissions, port conflicts) and how to solve them.

## 🚀 Next Steps
- Expand testing to DVWA **Medium** and **High** security levels.  
- Integrate additional Kali Linux tools (**Nmap, Nikto, Metasploit**).  
- Automate testing using scripts and APIs of ZAP and Burp Suite.

---

💡 **Author:** Ainhoa López Perelló  
📅 **Date:** 17/07/2025
