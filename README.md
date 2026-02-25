# FUTURE_CS_03 - API Security Risk Analysis

## Task Overview
This repository contains my completed **Task 3** for the Future Interns Cyber Security program: API Security Risk Analysis on OWASP Juice Shop.

## Objective
Perform a security risk analysis on a target API (OWASP Juice Shop), identify vulnerabilities aligned with the OWASP API Security Top 10, and deliver a professional report documenting findings, business impact, and remediation recommendations.

## Tools Used
- **Burp Suite Community Edition** - Intercepting proxy, request modification, manual testing
- **OWASP ZAP** - Automated and passive scanning
- **Browser DevTools** - API discovery and network traffic analysis
- **Postman** - Manual API testing and request organization
- **Kali Linux** - Testing environment

## Testing Methodology
The assessment followed the OWASP API Security Testing Guide:

1. **API Reconnaissance** - Endpoint enumeration via DevTools and API docs
2. **Automated Scanning** - Passive and active scanning with OWASP ZAP
3. **Manual Testing** - Intercepting and modifying requests to test for logic flaws
4. **Exploitation** - Developing proof-of-concept exploits for each finding
5. **Risk Rating** - CVSS-based classification (Critical/High/Medium/Low)

## Key Findings Summary

| ID | Finding | API Endpoint | Risk Level |
|----|---------|--------------|------------|
| **API-01** | SQL Injection - Authentication Bypass | `/rest/user/login` | Critical |
| **API-02** | Broken Object Level Authorization (BOLA) | `/rest/basket/{id}` | High |
| **API-03** | Excessive Data Exposure - Metrics | `/metrics` | High |
| **API-04** | Unauthenticated Admin API Access | `/api/Users`, `/api-docs` | High |
| **API-05** | Missing Rate Limiting | `/rest/user/login` | Medium |
| **API-06** | Stored Cross-Site Scripting (XSS) | `/api/Feedbacks` | High |

## Files Included
- `API_Security_Risk_Analysis_Report.pdf` - Complete professional report with:
  - Executive summary
  - Detailed findings (6 vulnerabilities)
  - Proof of concept methodologies
  - Business impact analysis
  - Remediation recommendations
  - CVSS risk scoring

## Target Application
- **Name**: OWASP Juice Shop
- **Type**: Intentionally vulnerable web application
- **API Base Paths**: `/api`, `/rest`
- **Environment**: Hosted demo instance / Local Docker deployment


