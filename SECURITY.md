# Security Policy

This policy applies to every repository of [dhondta](https://github.com/dhondta) that does not define its own `SECURITY.md`.

## Supported Versions

Only the latest release of each project (on [PyPI](https://pypi.org/), for the Python packages, or the `main` branch otherwise) receives security fixes. Archived repositories are no longer maintained and receive no fixes.

## Reporting a Vulnerability

Please do **not** report security vulnerabilities through public GitHub issues, discussions or pull requests.

Instead, report them privately through [GitHub's private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability): open the affected repository's *Security* tab, then click *Report a vulnerability*. Please include:

- the affected project and its version;
- the steps to reproduce the issue, and a proof of concept if relevant;
- the impact you expect.

You will get an answer as soon as possible. Once the issue is confirmed, a fix is released and the advisory is published.

## Scope

Several projects are offensive security tools by design (e.g. [Sploitkit](https://github.com/dhondta/python-sploitkit) consoles or [RPL Attacks](https://github.com/dhondta/rpl-attacks)): what they are meant to do is not a vulnerability. Vulnerabilities are, for instance, a crafted input that makes a tool execute code it should not (e.g. when decoding with [Codext](https://github.com/dhondta/python-codext) or parsing a Web page with [WebGrep](https://github.com/dhondta/webgrep)), or a dependency with a known vulnerability.
