# Provenance

Externally sourced information must retain enough metadata to show provider, source, retrieval date, original update date when available, freshness and authoritative URL where appropriate. Unknown source update dates remain unknown; do not substitute fetched_at.

Proposed sources record: id, provider, name, base_url, licence and attribution. Individual items may need specific source URLs beyond a provider home page.

Proposed snapshots: id, source_id, resource_type, resource_key, payload, fetched_at, source_updated_at, expires_at, etag, content_hash, status and error_message. Implement fields needed by the first provider rather than treating this illustrative schema as a completed migration.

Separate successful payload provenance from refresh failures. Briefing component status is computed from retrieval/cache policy; provider errors should be observable without exposing internal secrets. Preserve the last valid snapshot on failed refresh.

Editorial facts retain source references and as-of dates separately from external refresh timestamps. User records are not external facts. Third-party licensing is independent of the application MIT licence.
