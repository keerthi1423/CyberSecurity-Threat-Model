# Risk Register – Student Portal Web Application

## Purpose
This register identifies hypothetical security risks in the fictional Student Portal Web Application and prioritizes them based on likelihood and impact.

## Risk Assessment

| ID | Threat | Likelihood | Impact | Priority | Recommended Mitigation |
|---|---|---|---|---|---|
| R1 | Unauthorized account access | High | High | Critical | Strong password hashing, MFA and login rate limiting |
| R2 | SQL injection | Medium | High | High | Parameterized queries and server-side validation |
| R3 | Unauthorized student data access | Medium | High | High | Role-based access control and database permissions |
| R4 | Session theft or misuse | Medium | High | High | Secure cookies, session expiry and logout invalidation |
| R5 | Sensitive information in error messages | Medium | Medium | Medium | Generic error responses and secure server-side logs |
| R6 | Excessive requests affecting availability | Medium | Medium | Medium | Rate limiting, monitoring and request controls |

## Risk Rating Method

- Likelihood: Low, Medium or High probability of occurrence.
- Impact: Low, Medium or High potential damage.
- Critical: Requires immediate attention.
- High: Should be addressed as a priority.
- Medium: Should be addressed through planned improvements.

## Review Notes

All risks and ratings are illustrative. They are based on the assumed design of a fictional student portal and are not findings from a real security test.

## Conclusion

The highest-priority risks involve account security, database protection, access control and session management. Implementing the recommended controls will reduce the likelihood and impact of these threats.
