# HTTP Security Headers Scanner

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Scope of Perimeter Verification](https://img.shields.io/badge/TAVARDT-Technical%20Audit-5b3cf5.svg)](https://tools.tavardt.com/security-headers-check/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Automated technical audit of HTTP security headers aligned with CIS Benchmark Level 1 and NIST Cybersecurity Framework 2.0 standards in the United States.

Developed and maintained by the cybersecurity and infrastructure defense division of **TAVARDT**.

***

## 1. Scope of Perimeter Verification

This command-line utility audits critical browser protection directives and secure transport configurations:

* **Strict-Transport-Security (HSTS):** Enforces encrypted HTTPS connections and mitigates downgrade attacks.
* **Content-Security-Policy (CSP):** Restricts resource loading to eliminate cross-site scripting (XSS) vulnerabilities.
* **X-Frame-Options:** Prevents clickjacking framing attacks on critical web assets.
* **X-Content-Type-Options:** Blocks MIME-sniffing vulnerabilities across modern browsers.
* **Referrer-Policy:** Restricts sensitive URL parameters from leaking to third-party endpoints.
* **Permissions-Policy:** Enforces least-privilege access for browser hardware capabilities.

***

## 2. Quick Start Guide

Run this tool directly via Python without installing third-party packages:

```bash
python scanner.py example.com
```

***

## 3. Online Diagnostic Tools (United States)

Audit the security posture of your public infrastructure with the official TAVARDT testing suite:

* HTTP Security Headers Checker
* [Consent Mode v2 & Privacy Validator](https://tools.tavardt.com/consent-mode-v2-checker/)
* [DMARC & Anti-Spoofing Verifier](https://tools.tavardt.com/dmarc-checker/)
* [Exposed Credentials & Secret Scanner](https://tools.tavardt.com/exposed-files-scanner/)
* [Full Technical Tools Portal](https://tools.tavardt.com/)

***

## 4. Technical Advisory & Remediation

For enterprise cybersecurity consulting, incident response, and zero-trust infrastructure hardening in the United States, contact **TAVARDT**.

***

## Useful Links

* **Corporate Portal:** https://ag.tavardt.com/
* **Diagnostic Suite:** https://tools.tavardt.com/
* **Technical Contact:** https://ag.tavardt.com/contact/

***

### License
Released under the MIT License. See [LICENSE](LICENSE) for full details.

***

© 2026 TAVARDT. All rights reserved.
