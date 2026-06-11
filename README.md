 # jenkins-devsecops-pipeline

DevSecOps pipeline with security scanning integrated — Trivy (SCA) + OWASP ZAP (DAST) + Security Gate.

## Pipeline stages

| Stage | Description |
|-------|-------------|
| Checkout | Clone repository |
| Build | Build application |
| Test | Run Cypress E2E tests from [cypress-e2e-suite](https://github.com/Walle-1904/cypress-e2e-suite) |
| Security Scan - SCA | Trivy vulnerability scan on dependencies and images |
| Security Scan - DAST | OWASP ZAP baseline scan against target app |
| Security Gate | Fail pipeline if CVSS >= 7 vulnerabilities found |
| Deploy | Deploy application |

## Tech stack

![Jenkins](https://img.shields.io/badge
