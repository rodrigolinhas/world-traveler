# Security policy

There is no released application or supported production version yet. Security requirements apply from M0; releases will define their support windows.

## Reporting a vulnerability

Use the repository's private vulnerability reporting option if enabled: https://github.com/rodrigolinhas/world-traveler/security/advisories/new.

Private reporting availability has not been verified. If the option is unavailable, ask the maintainer to enable a private reporting channel without disclosing exploit details. Do not put credentials, private user data or exploit details in public issues. No response-time commitment is established yet.

## Engineering requirements

Validate input at trust boundaries, parameterize SQL, use restricted database permissions, protect provider credentials, avoid arbitrary user-supplied provider URLs, validate file paths and never render external HTML unsafely.

Use Argon2id passwords and server-side sessions with random tokens stored as hashes. Cookies must be HttpOnly, Secure in production, and use a deployment-appropriate SameSite policy. Evaluate CSRF protection for authenticated mutations; SameSite alone is not a universal substitute. Same-origin web/API deployment is preferred.

Apply appropriate security headers, request/provider deadlines and justified rate limits. Logs must exclude credentials, tokens and sensitive profile information. Collect only personal data required for a current feature; initial functionality does not need passport scans/numbers or continuous location history.

M0 must establish actionable dependency and secret scanning. Authentication-specific controls arrive with M3, before authentication is exposed. See [security baseline](docs/security/baseline.md).
