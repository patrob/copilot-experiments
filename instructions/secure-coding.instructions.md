# Secure Coding Instructions

Follow these security-focused guidelines when writing, reviewing, or refactoring code.

## Input Validation & Sanitization

### Always Validate Input
- Validate all user input on both client and server side
- Use allowlists (permitted values) rather than blocklists when possible
- Implement proper type checking and format validation
- Set reasonable limits on input length and size

### Sanitize Data
- Escape output data appropriate to the context (HTML, SQL, etc.)
- Use parameterized queries or prepared statements for database operations
- Validate and sanitize file uploads (type, size, content)
- Implement Content Security Policy (CSP) headers

## Authentication & Authorization

### Strong Authentication
- Implement multi-factor authentication where possible
- Use secure password requirements and storage (bcrypt, scrypt, or Argon2)
- Implement account lockout mechanisms after failed attempts
- Use secure session management with proper timeout

### Proper Authorization
- Implement principle of least privilege
- Validate permissions on every protected resource access
- Use role-based access control (RBAC) or attribute-based access control (ABAC)
- Never rely on client-side security checks alone

## Data Protection

### Encryption
- Use HTTPS/TLS for all data transmission
- Encrypt sensitive data at rest using strong encryption algorithms
- Implement proper key management and rotation
- Use secure random number generation for cryptographic operations

### Sensitive Information
- Never log sensitive data (passwords, tokens, personal information)
- Remove or mask sensitive data in error messages
- Implement secure data disposal when data is no longer needed
- Use environment variables for secrets, never hardcode them

## Error Handling & Logging

### Secure Error Handling
- Never expose system internals in error messages
- Log security events (failed logins, permission violations)
- Implement proper exception handling to prevent information leakage
- Use generic error messages for user-facing applications

### Security Logging
- Log authentication and authorization events
- Include relevant context (user ID, IP address, timestamp)
- Monitor for suspicious patterns and anomalies
- Ensure logs are protected from tampering

## Code Security Practices

### Dependency Management
- Keep all dependencies up to date
- Regularly scan for known vulnerabilities
- Use dependency lock files to ensure consistent builds
- Remove unused dependencies

### Secure Configuration
- Change default passwords and configurations
- Disable unnecessary features and services
- Use secure communication protocols
- Implement proper CORS policies

## Common Vulnerabilities to Avoid

### OWASP Top 10
1. **Injection**: Use parameterized queries, input validation
2. **Broken Authentication**: Implement secure session management
3. **Sensitive Data Exposure**: Encrypt data, use HTTPS
4. **XML External Entities (XXE)**: Disable external entity processing
5. **Broken Access Control**: Implement proper authorization checks
6. **Security Misconfiguration**: Use secure defaults, regular updates
7. **Cross-Site Scripting (XSS)**: Sanitize output, use CSP
8. **Insecure Deserialization**: Validate serialized data
9. **Using Components with Known Vulnerabilities**: Regular security updates
10. **Insufficient Logging & Monitoring**: Implement comprehensive logging

## Security Testing

### Regular Testing
- Perform static application security testing (SAST)
- Implement dynamic application security testing (DAST)
- Conduct regular penetration testing
- Use automated security scanning in CI/CD pipelines

### Code Review Focus
- Review all security-critical code paths
- Check for proper input validation and output encoding
- Verify authentication and authorization logic
- Ensure secrets are not exposed

## Compliance Considerations

### Data Privacy
- Implement GDPR, CCPA compliance where applicable
- Provide data portability and deletion capabilities
- Maintain audit trails for data access and modifications
- Implement privacy by design principles

When implementing these security measures, always consider the specific requirements and threat model of your application. Security is not one-size-fits-all, and measures should be proportionate to the risk level.