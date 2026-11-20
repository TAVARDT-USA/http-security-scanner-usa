# HTTP Security Headers Scanner | TAVARDT USA

[![Auditoria de Segurança](https://img.shields.io/badge/TAVARDT-Diagn%C3%B3stico%20T%C3%A9cnico-5b3cf5.svg)](https://tools.tavardt.com/security-headers-check/)
[![Conformidade](https://img.shields.io/badge/Jurisdi%C3%A7%C3%A3o-United States-00C853.svg)](https://ag.tavardt.com/cybersecurity/)

Automated technical audit of HTTP security headers aligned with CIS Benchmark Level 1 and NIST Cybersecurity Framework 2.0 standards in the United States.

Desenvolvido e mantido pela divisão de cibersegurança e proteção de infraestruturas da **[TAVARDT USA](https://ag.tavardt.com/)**.

---

## 1. Scope of Perimeter Verification

This command-line utility audits critical browser protection directives and secure transport configurations:

* **Strict-Transport-Security (HSTS):** Força comunicações encriptadas via HTTPS e impede ataques de downgrade e interceptação SSL.
* **Content-Security-Policy (CSP):** Mitiga ataques de injeção de scripts (XSS) e restringe as origens autorizadas para carregamento de recursos.
* **X-Frame-Options:** Previne ataques de clickjacking regulando as permissões de incorporação em frames e iframes.
* **X-Content-Type-Options:** Impede a execução indevida de ficheiros derivados de vulnerabilidades de MIME-sniffing.
* **Referrer-Policy:** Protege dados sensíveis contidos em URLs de referência contra fuga para domínios terceiros.
* **Permissions-Policy:** Aplica o princípio do menor privilégio sobre APIs de hardware do navegador (câmara, microfone e geolocalização).

---

## 2. Quick Start Guide

Execute a ferramenta diretamente via Python sem necessidade de instalar dependências externas:

```bash
python scanner.py exemplo.com
```

---

## 3. Online Diagnostic Tools (United States)

Audite a infraestrutura pública das suas aplicações utilizando a suíte de diagnósticos da TAVARDT:

* [HTTP Security Headers Checker](https://tools.tavardt.com/security-headers-check/)
* [Consent Mode v2 & Privacy Validator](https://tools.tavardt.com/consent-mode-v2-checker/)
* [DMARC & Anti-Spoofing Verifier](https://tools.tavardt.com/dmarc-checker/)
* [Exposed Credentials & Secret Scanner](https://tools.tavardt.com/exposed-files-scanner/)
* [Full Technical Tools Portal](https://tools.tavardt.com/)

---

## 4. Technical Advisory & Remediation

For enterprise cybersecurity consulting, incident response, and zero-trust infrastructure hardening in the United States, contact **[TAVARDT USA](https://ag.tavardt.com/contact/)**.
