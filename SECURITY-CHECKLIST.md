# Security Checklist

This document is the working checklist for our first pull-request security audit.
It lives on the `security-checklist` branch and is merged into `main` via a pull
request as part of the audit rehearsal.

## Pull Request Review Checklist

1. Confirm the PR author and reviewers are expected contributors.
2. Read the full diff — every changed file, not just the first screen.
3. Check that no secrets, tokens, keys, or credentials appear in the diff.
4. Check for suspicious or obfuscated code: base64 blobs, encoded strings, eval-style execution.
5. Verify no new dependencies are introduced without review.
6. Confirm CI checks pass and no checks were skipped or forced.
7. Look for changes to CI workflows, build scripts, or dependency manifests.
8. Look for typosquatted package or import names.
9. Confirm the changes match the stated purpose of the PR.
10. Approve, comment, or request changes with a written rationale.

## Repository-Level Checks

- Review open secret scanning alerts.
- Review open dependabot alerts.
- Review open code scanning alerts.
- Confirm branch protection on the default branch.

## Known Reference Vulnerability

- CVE-2024-3094 (xz-utils backdoor) — CVSS 3.1 base score 10.0, critical.
