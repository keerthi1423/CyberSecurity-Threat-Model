# Threat Modeling and Secure Configuration Assessment

## 1. Project Overview

This project presents a defensive threat model for a fictional Student Portal Web Application. The portal allows students to register, log in, view profiles, access course materials, and submit assignments.

## 2. Objective

To identify potential security threats, evaluate their likelihood and impact, and recommend appropriate security controls to protect application data and services.

## 3. Application Components

- Student: Uses a browser to access the portal.
- Web Application: Receives and processes user requests.
- Authentication Service: Verifies user credentials and manages sessions.
- Database: Stores student profiles and assignment records.
- Email Service: Sends account notifications.

## 4. Assets to Protect

| Asset | Security Requirement |
|---|---|
| Student credentials | Confidentiality |
| Student profiles | Confidentiality and integrity |
| Assignment records | Integrity and availability |
| Session tokens | Confidentiality |
| Application service | Availability |

## 5. Trust Boundaries

1. User device to web application: External user requests enter the application.
2. Web application to database: Application accesses stored records.
3. Application to email provider: Data is sent to an external service.

## 6. STRIDE Threat Analysis

| STRIDE Category | Example Threat | Recommended Control |
|---|---|---|
| Spoofing | An attacker impersonates a student account | Strong authentication and MFA |
| Tampering | Unauthorized modification of assignment records | Server-side authorization and input validation |
| Repudiation | A user denies performing an important action | Secure audit logging |
| Information Disclosure | Student information is exposed | Encryption and access controls |
| Denial of Service | Excessive requests affect availability | Rate limiting and monitoring |
| Elevation of Privilege | A student accesses administrator functions | Role-based access control |

## 7. Risk Register

Likelihood and impact are rated Low, Medium, or High. Priority is based on the combined assessment.

| ID | Risk | Likelihood | Impact | Priority |
|---|---|---|---|---|
| R1 | Unauthorized account access | High | High | Critical |
| R2 | SQL injection | Medium | High | High |
| R3 | Unauthorized access to student records | Medium | High | High |
| R4 | Session management weaknesses | Medium | High | High |
| R5 | Information leakage through errors | Medium | Medium | Medium |
| R6 | Service disruption from excessive requests | Medium | Medium | Medium |

These are hypothetical risks for the fictional application, not confirmed vulnerabilities.

## 8. Prioritized Hardening Plan

### Priority 1 – Critical
- Enforce strong password hashing.
- Implement multi-factor authentication where appropriate.
- Apply account and session protections.

### Priority 2 – High
- Use parameterized database queries.
- Implement role-based access control.
- Validate all input on the server.
- Secure session cookies and use HTTPS.

### Priority 3 – Medium
- Implement rate limiting.
- Avoid displaying sensitive technical errors.
- Monitor security events and maintain audit logs.

## 9. Conclusion

This threat model identifies potential security risks in a fictional Student Portal Web Application. STRIDE analysis helps organize threats, while the risk register helps prioritize defensive improvements. Applying the recommended controls can improve confidentiality, integrity, and availability.

## 10. Scope and Limitations

This is a theoretical defensive assessment of a fictional application. No real application or third-party system was tested. Risk ratings are illustrative and should be validated against an actual system before implementation.
