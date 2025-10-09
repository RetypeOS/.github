# Security Policy for RetypeOS

## Our Commitment to Security

The RetypeOS team and community take the security of our projects seriously. We appreciate the efforts of security researchers and the broader community in helping us maintain a high standard of security. The integrity and safety of our users' development environments are our top priority.

This document outlines our security policy and the process for responsibly reporting vulnerabilities. We are committed to working with you to verify and address any potential issues that are reported to us.

## Supported Versions

Security updates are a high priority. We provide security patches for the following versions of our projects (e.g., `axes`):

| Version | Supported          |
| ------- | ------------------ |
| `0.1.x` | :white_check_mark: |
| `< 0.1` | :x:                |

When a new major or minor version is released, we will provide security support for the previous minor version for a period of at least 3 months. Please ensure you are using a supported version to receive security updates.

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

We believe in responsible disclosure. To protect our users, we ask that you report potential vulnerabilities to us privately so that we have the opportunity to investigate and respond before the issue is made public.

### Method 1: GitHub Private Vulnerability Reporting (Preferred)

The most secure and preferred way to report a vulnerability is through **GitHub's private vulnerability reporting feature**. This ensures that your report is delivered directly to the repository maintainers in a secure and confidential manner.

1. Navigate to the main page of the repository (e.g., `RetypeOS/axes`).
2. Go to the **"Security"** tab.
3. Click on **"Report a vulnerability"** in the sidebar.
4. Fill out the form with as much detail as possible, including:
    * A clear description of the vulnerability.
    * The component or feature affected.
    * Steps to reproduce the vulnerability. Please provide a clear and concise proof of concept.
    * The potential impact of the vulnerability (e.g., remote code execution, file system corruption, information disclosure).
    * Any known workarounds or mitigations.

### Method 2: Email (Secondary)

If you are unable to use GitHub's private reporting feature, you can send an email to our security contact.

* **Email:** `reynierramos280@gmai.com`

Please use a clear subject line, such as `[SECURITY] Vulnerability in RetypeOS/axes`. If possible, please encrypt your email using PGP to protect the contents of the report.

<!-- Opcional: Si decides crear una clave PGP, puedes añadir esto -->
<!-- My PGP key can be found at [LINK TO KEYBASE OR PGP KEYSERVER]. -->

### What to Expect After Reporting

After you submit a report, you can expect the following process:

1. **Acknowledgement (within 48 hours):** We will provide an initial confirmation that we have received your report.
2. **Initial Triage (within 5 business days):** We will investigate the report to validate the vulnerability. We may ask for additional information during this phase.
3. **Coordinated Disclosure:** We will work with you to coordinate a disclosure timeline. Our goal is to release a patch and a security advisory simultaneously. We will not disclose the vulnerability publicly until a fix is available and users have had a reasonable amount of time to upgrade.
4. **Public Acknowledgement:** Once the vulnerability is fixed and disclosed, we are happy to publicly credit you for your discovery, unless you prefer to remain anonymous.

## Scope of Our Security Policy

This policy applies to the latest version of our projects hosted in the RetypeOS organization. We are primarily interested in vulnerabilities that could lead to:

* **Remote Code Execution (RCE):** A scenario where parsing a malicious `axes.toml` file or running a command could lead to arbitrary code execution outside the intended scope of the script.
* **Arbitrary File System Access:** A vulnerability that allows reading or writing files outside of the intended project directory without explicit user action.
* **Denial of Service (DoS):** A vulnerability that causes the `axes` binary to crash or become unresponsive due to a specially crafted input (e.g., a "zip bomb" style configuration file).
* **Privilege Escalation:** A scenario where `axes` could be used to gain higher privileges on the host system.

While we appreciate all reports, issues that are not considered security vulnerabilities (e.g., bugs that cause incorrect output but do not compromise the system) should be reported through our standard [GitHub Issues](https://github.com/RetypeOS/axes/issues).

Thank you for helping keep RetypeOS and its users safe.
