# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | ✅ Yes             |

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please report it responsibly **DO NOT open a public GitHub issue**.

### How to Report

**Email**: ritacsolutions@gmail.com

Please include:
- Description of the vulnerability
- Steps to reproduce (if applicable)
- Potential impact
- Suggested fix (if available)
- Your contact information

### Response Timeline

- **Initial Response**: Within 24-48 hours
- **Investigation**: 3-5 business days
- **Fix & Release**: 1-2 weeks (depending on severity)
- **Public Disclosure**: After patch release

### Severity Levels

**Critical (CVSS 9.0-10.0)**
- Remote code execution
- Complete authentication bypass
- Direct API key exposure

**High (CVSS 7.0-8.9)**
- XSS vulnerabilities
- CSRF attacks
- Session hijacking

**Medium (CVSS 4.0-6.9)**
- Information disclosure
- Denial of service
- Privilege escalation

**Low (CVSS 0.1-3.9)**
- Minor issues
- Best practice violations

## Security Best Practices

When using this application:

- ✅ Never commit API keys to repositories
- ✅ Use HTTPS connections only
- ✅ Keep your browser and OS updated
- ✅ Use strong, unique passwords
- ✅ Enable two-factor authentication on GitHub
- ✅ Review search results carefully
- ✅ Follow legal and ethical guidelines

## Security Features

This application implements:

- **Client-side Processing**: No sensitive data sent to backend servers
- **API Key Security**: API keys only stored in current session memory
- **HTTPS Only**: All API communications encrypted
- **Input Validation**: Query validation and sanitization
- **Error Handling**: Secure error messages without data leakage
- **Rate Limiting**: Respects LeakCheck API rate limits

## Responsible Disclosure

We follow the principles of responsible disclosure:

1. **Do not publicly disclose** the vulnerability until we've had time to respond
2. **Provide detailed information** to help us understand and fix the issue
3. **Be patient** while we investigate and develop a fix
4. **Avoid accessing** more data than necessary to confirm the vulnerability
5. **Document your findings** clearly for our security team

## Acknowledgments

Security researchers who responsibly report vulnerabilities will be:
- Credited in the security advisory (if desired)
- Listed in the SECURITY.md contributors section
- Thanked publicly in release notes

## Contact

**Security Contact**: ritacsolutions@gmail.com

For non-security issues, please use GitHub Issues: https://github.com/ritacsolutionsllc/leak-checker-app/issues

---

**Thank you for helping keep Database Leak Checker secure!** 🔐
