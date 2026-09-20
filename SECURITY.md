# Security Policy

## Supported Versions

Until `1.0.0`, only the latest commit on `main` and the latest tagged release receive security fixes.

| Version | Supported          |
| ------- | ------------------ |
| < 1.0.0 | :white_check_mark: |
| ≥ 1.0.0 | :white_check_mark: (see release notes) |

## Reporting a Vulnerability

We take security seriously. If you discover a vulnerability in CodeKavach, please **report it privately** so we can investigate and fix it before it is disclosed publicly.

### How to Report

1. **GitHub Private Advisory (preferred)**: Use [GitHub Security Advisories](../../security/advisories/new) to submit a private report. This is the fastest way to reach us.
2. **Email**: If GitHub advisories are not suitable, contact us at the email listed in our profile.

### What to Include

- **Description**: A clear description of the vulnerability
- **Steps to Reproduce**: How to trigger the issue (proof of concept if possible)
- **Impact**: What an attacker could achieve by exploiting this vulnerability
- **Suggested Fix (optional)**: If you have ideas for how to fix it

### What Happens Next

1. We will acknowledge your report within **48 hours**
2. We will investigate and confirm the vulnerability within **7 days**
3. We will work on a fix and coordinate disclosure with you
4. You will be credited in the security advisory (unless you prefer to remain anonymous)

## Scope

Security reports should relate to issues that could:

- **Expose secrets or PII** sent to CodeKavach for review
- **Allow bypass of redaction or privacy guards**
- **Enable prompt injection or exfiltration via malicious repository content**
- **Compromise the sandboxing of analysis engines**
- **Allow unauthorized access to scan results or the audit ledger

### Out of Scope

The following are generally out of scope (but we still appreciate reports):

- Issues in dependencies that we do not directly control (please report upstream)
- Theoretical concerns without a practical exploit path
- UI/UX issues that do not have security implications
- Reports based on automated scanning without manual verification

For details on our threat model and what we defend against, see [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) section 6.4 and [`docs/THREAT_MODEL.md`](docs/THREAT_MODEL.md).

## Security Best Practices for Users

- Always run CodeKavach with the latest version
- Review the privacy configuration before scanning sensitive repositories
- Use local LLM providers (Ollama, vLLM) when possible to minimize data exposure
- Enable ledger auditing to track what data leaves your environment

## Security Updates

Security fixes will be released as patch versions and announced in the [release notes](../../releases). Users are encouraged to update as soon as possible when a security release is available.

---

*Last updated: 2026-09-21*
