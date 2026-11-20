# Architecture

CEO → Executive AI policy oversight → n8n scheduler/orchestrator → specialist roles/workers → QA → authorization gate → official external tools → recorded receipts → metrics/CEO reporting.

Local Mac setup: Docker Compose n8n and PostgreSQL; Ollama if editorial tests succeed; Node/TypeScript workers for schema validation; Remotion + FFmpeg for rendering; Piper optional. Canva is for approved manual design/export; no assumed automation API. n8n internal state and business records must remain separate. Optional Laravel/Inertia/React CEO console later, only if necessary.

Business records: Job{id, department, role, input, status, idempotency_key, timestamps}; Step{job, attempt, result}; Artifact{path, checksum, rights, media metadata}; Approval{action, actor, decision, expiry}; Publication{platform, account, unique key, platform_post_id}; AuditEvent{actor, action, time}. Validate JSON boundaries; use UTC.

Permission levels: observe, create, execute within previously approved policy, CEO-approval required for publication policies, outreach, spending, contracts, pricing, deployments and destructive operations. Research and model outputs are untrusted data. Secure credentials locally; no secrets committed.

Handle retries, timeouts, reconciliation after ambiguous publishing failures, uniqueness constraints and a kill switch. Laptop sleep/offline pauses scheduled operations. No cloud expenses or paid API requests silently.
