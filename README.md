<p align="center">
  <a href="https://ag.tavardt.com/">
    <img src="https://ag.tavardt.com/img/tavardt-banner.png" alt="TAVARDT" width="1024" />
  </a>
</p>

# HTTP Security Headers Scanner

[![Scope of Perimeter Verification](https://img.shields.io/badge/TAVARDT-Technical%20Audit-5b3cf5.svg)](https://tools.tavardt.com/security-headers-check/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Automated technical audit of HTTP security headers aligned with CIS Benchmark Level 1 and NIST Cybersecurity Framework 2.0 standards in the United States.

Engineered and maintained by the cyber defence practice at **TAVARDT** for North American infrastructure.

***

## 1. Scope of Perimeter Verification

This command-line tool audits essential browser protection directives and secure transport configurations for United States systems:

* **Strict-Transport-Security (HSTS):** Enforces HTTPS encryption and prevents SSL-stripping and downgrade attacks.
* **Content-Security-Policy (CSP):** Restricts unauthorized script execution and mitigates Cross-Site Scripting (XSS).
* **X-Frame-Options:** Prevents clickjacking by controlling framing and iframe permissions.
* **X-Content-Type-Options:** Blocks MIME-sniffing vulnerabilities in client web browsers.
* **Referrer-Policy:** Protects sensitive URL path parameters from leaking to external origins.
* **Permissions-Policy:** Applies least-privilege control to browser hardware interfaces and sensors.

***

## 2. Defensive Baseline & Risk Mitigation Matrix

<table>
  <thead>
    <tr>
      <th>Security Header</th>
      <th>Risk Vector Mitigated</th>
      <th>Default Missing State</th>
      <th>Defensive Baseline</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Strict-Transport-Security</strong></td>
      <td>SSL-stripping and protocol downgrade</td>
      <td>Initial connection via unencrypted HTTP</td>
      <td><code>max-age=31536000; includeSubDomains; preload</code></td>
    </tr>
    <tr>
      <td><strong>Content-Security-Policy</strong></td>
      <td>Cross-Site Scripting (XSS) and data injection</td>
      <td>Unrestricted script execution from any domain</td>
      <td>Explicit source whitelisting for scripts and objects</td>
    </tr>
    <tr>
      <td><strong>X-Frame-Options</strong></td>
      <td>UI redressing and clickjacking</td>
      <td>Page embeddable in third-party iframes</td>
      <td><code>DENY</code> or <code>SAMEORIGIN</code></td>
    </tr>
    <tr>
      <td><strong>X-Content-Type-Options</strong></td>
      <td>MIME type confusion and sniffing</td>
      <td>Browser interprets non-executable files as code</td>
      <td><code>nosniff</code></td>
    </tr>
    <tr>
      <td><strong>Referrer-Policy</strong></td>
      <td>Sensitive URL token leakage</td>
      <td>Full URL path transmitted across origins</td>
      <td><code>strict-origin-when-cross-origin</code></td>
    </tr>
    <tr>
      <td><strong>Permissions-Policy</strong></td>
      <td>Unauthorized hardware sensor access</td>
      <td>Browser grants access based on basic prompts</td>
      <td>Restricted access to camera, microphone, and geolocation</td>
    </tr>
  </tbody>
</table>

***

## 3. Quick Start Guide & CLI Automation

Run this tool directly via Python without installing third-party packages:

```bash
python scanner.py example.com
```

The auditing engine evaluates perimeter responses deterministically:

* **Native Standard Library:** Operates purely via Python standard libraries (`urllib.request`), requiring zero third-party dependencies.
* **Deterministic Scoring:** Tests all six foundational headers case-insensitively and returns an integer score out of six.
* **CI/CD Pipeline Compatibility:** Integrates into automated pre-deployment testing and compliance verification workflows.

***

## 4. Frequently Asked Questions (Technical FAQ)

### 1. How does missing HSTS expose web visitors to SSL-stripping and downgrade attacks?
Without Strict-Transport-Security, browsers initiate connections via plaintext HTTP before receiving an HTTPS redirect. Attackers positioned along the network route can intercept this initial request, strip encryption, and proxy communications in cleartext.

### 2. What is the primary defensive role of Content-Security-Policy (CSP)?
Content-Security-Policy acts as a defense-in-depth layer against Cross-Site Scripting (XSS) and data injection. It explicitly declares trusted source domains for scripts, styles, images, and framing objects, preventing unauthorized code execution.

### 3. How does X-Frame-Options protect applications against clickjacking attacks?
X-Frame-Options instructs client web browsers whether a page may be embedded within frames, iframes, or objects. Configuring this directive to DENY or SAMEORIGIN prevents malicious third-party websites from rendering transparent UI overlays to hijack user clicks.

### 4. Why is Permissions-Policy critical for client device privacy and least privilege?
Permissions-Policy restricts browser access to sensitive hardware interfaces including microphones, webcams, geolocation, and USB devices. Enforcing this header ensures third-party scripts or embedded elements cannot silently access device sensors without explicit permission.

### 5. Can this HTTP security headers scanner be integrated into automated CI/CD pipelines?
Yes, `scanner.py` runs natively using Python standard libraries without external dependencies. It computes deterministic audit scores and exit statuses, making it ideal for integration into pre-deployment verification steps in GitHub Actions and automated build pipelines.

***

## 5. Online Diagnostic Tools (United States)

Audit your public infrastructure using the TAVARDT diagnostic suite:

* [Consent Mode v2 & Privacy Validator](https://tools.tavardt.com/consent-mode-v2-checker/)
* [DMARC & Anti-Spoofing Verifier](https://tools.tavardt.com/dmarc-checker/)
* [Exposed Credentials & Secret Scanner](https://tools.tavardt.com/exposed-files-scanner/)
* [Full Technical Tools Portal](https://tools.tavardt.com/)

***

## 6. Technical Advisory & Perimeter Defence in the United States

For advanced NIST SP 800-53 and CSF 2.0 alignment, offensive penetration testing, and incident response across North America, contact **TAVARDT**.

***

## Useful Links

* **Corporate Portal:** https://ag.tavardt.com/
* **Diagnostic Suite:** https://tools.tavardt.com/
* **Technical Contact:** https://ag.tavardt.com/contact/

***

### License
Released under the MIT License.

***

© 2026 TAVARDT. All rights reserved.
