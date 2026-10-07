# Security and privacy baseline

Security applies from M0. Use trust-boundary input validation, parameterized SQL, explicit database permissions, secure headers, path validation, backend-only secrets, fixed approved provider endpoints and safe external-content rendering. Bound requests and provider concurrency. Add justified rate limiting where abusive traffic would affect authentication, quotas or availability.

M3 authentication uses email/password, Argon2id, random server-side session tokens with hashed storage, HttpOnly cookies, Secure production cookies and appropriate SameSite policy. Define expiry, rotation/invalidation and CSRF protection before exposing authenticated mutations. Prefer same-origin deployment; do not introduce JWTs without a concrete architectural requirement.

Personal resource operations enforce ownership. Logs and errors must not expose passwords, session tokens, keys or sensitive profile values. Minimize personal collection; passport scans/numbers, national IDs and continuous location tracking are unnecessary initially. Sensitive traveler preferences require explicit value, consent and retention design later.

M0 CI establishes actionable secret/dependency scanning; regular dependency updates continue thereafter. M6 validates deployment security, backup/restore, review procedures and production operation. Public user content later requires visibility, moderation and abuse handling alongside its release.

See [SECURITY.md](../../SECURITY.md) for the reporting path and its current availability limitation.
