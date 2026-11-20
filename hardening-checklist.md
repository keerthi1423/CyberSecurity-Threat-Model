# Security Hardening Checklist

## Authentication
- [ ] Store passwords using a secure password hashing algorithm such as Argon2id or bcrypt.
- [ ] Implement appropriate multi-factor authentication.
- [ ] Apply login rate limiting.

## Application Security
- [ ] Validate input on the server.
- [ ] Use parameterized SQL queries.
- [ ] Implement role-based access control.
- [ ] Return generic error messages.

## Session Security
- [ ] Set HttpOnly on session cookies.
- [ ] Set Secure on cookies when using HTTPS.
- [ ] Set an appropriate SameSite policy.
- [ ] Expire sessions after inactivity.
- [ ] Invalidate sessions on logout.

## Database Security
- [ ] Restrict database permissions.
- [ ] Protect sensitive information.
- [ ] Use encrypted connections where supported.

## Monitoring and Verification
- [ ] Record security events without logging passwords or session tokens.
- [ ] Verify rate limiting using controlled local tests.
- [ ] Verify access controls with test accounts and roles.
- [ ] Review error responses for sensitive information.

## Final Review
- [ ] Threat model diagram added.
- [ ] Risk register completed.
- [ ] Security recommendations documented.
- [ ] All supporting files uploaded to GitHub.
