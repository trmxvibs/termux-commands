# Security Policy

## Supported Versions

This project mainly contains documentation and command references.

Security updates will generally apply to the latest version of the repository.

| Version | Supported |
|--------|-----------|
| Latest | ✅ Yes |
| Older versions | ❌ No |

---

# Reporting a Security Issue

If you discover a security vulnerability related to this repository, please report it responsibly.

Do NOT open a public issue if the vulnerability could expose users to risk.

Instead:

1. Contact the repository maintainer.
2. Provide a detailed explanation of the issue.
3. Include steps to reproduce the problem if possible.

---

# What to Include in a Security Report

Please include:

- Description of the vulnerability
- Steps to reproduce the issue
- Possible impact
- Suggested fix (if known)

Example:

```
Command: curl example
Problem: unsafe example command
Impact: could execute malicious script
```

---

# Responsible Disclosure

We request that security researchers:

- Give maintainers time to fix the issue
- Avoid publishing exploits before a fix is available
- Work with maintainers to improve project security

---

# Security Best Practices

When using commands from this repository:

• Only run commands from trusted sources  
• Review scripts before executing them  
• Avoid running unknown scripts with root privileges  

Example of risky command:

```
curl example.com/script.sh | bash
```

Always inspect scripts before executing them.

---

# Acknowledgements

We appreciate responsible security disclosures that help improve this project.
