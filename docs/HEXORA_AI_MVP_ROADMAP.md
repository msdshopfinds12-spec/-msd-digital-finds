# HEXORA AI — MVP Roadmap

## Architecture direction
Use the existing repository stack only after confirming its actual package and runtime configuration. Proposed target architecture for the MVP:
- Frontend: React/Next.js UI consistent with the existing repository
- Backend: server-side routes/actions with strict validation
- Data: PostgreSQL/Supabase only after credentials and schema are configured
- Authentication: managed auth; no custom password storage
- AI: provider adapter with mock mode as the default in development
- Billing: defer live billing; use a verified Philippine-compatible provider only after account and webhook setup are confirmed
- Hosting: existing deployment platform, subject to a verified build/deploy workflow

Do not add dependencies or replace the current stack until the repository has been audited.

## Phase 0 — Repository and product baseline
- [x] Record product direction and target customers
- [x] Define a narrow first release
- [x] Define privacy, approval, and cost-control requirements
- [ ] Audit existing source tree, scripts, dependencies, and deployment configuration
- [ ] Confirm the current build and test commands

## Phase 1 — Working content workspace
- [ ] Business profile form (business name, niche, audience, products, tone)
- [ ] Content generator interface with deterministic mock provider
- [ ] Post editor with save, duplicate, and delete
- [ ] 7-day content calendar
- [ ] Export to Markdown/CSV
- [ ] Input validation, empty states, loading states, and error handling
- [ ] Unit and integration tests

Release gate: all core flows work in mock mode; build and tests pass; no secrets committed.

## Phase 2 — Accounts and persistence
- [ ] Authentication and protected routes
- [ ] User-owned business profiles and content records
- [ ] Row-level access control and authorization tests
- [ ] Data export and account deletion process
- [ ] Database migration and backup plan

Release gate: users cannot access another user's data; access-control tests pass.

## Phase 3 — Controlled AI integration
- [ ] Provider adapter interface
- [ ] Mock provider remains available
- [ ] Server-side secret handling
- [ ] Request validation and output length limits
- [ ] Per-user quotas, rate limits, and cost tracking
- [ ] Safe fallback and provider error handling

Release gate: provider calls are server-side, usage is bounded, and no API key is exposed to the browser or repository.

## Phase 4 — Pilot and payments
- [ ] Recruit pilot businesses and collect feedback
- [ ] Publish clear plan limits and terms
- [ ] Select a supported payment provider after eligibility/KYC review
- [ ] Implement server-verified webhook handling with signature checks and idempotency
- [ ] Test payment success, failure, cancellation, refund, and duplicate webhook cases
- [ ] Grant/revoke entitlements from verified server-side subscription state

Release gate: test-mode payment lifecycle passes; production mode remains disabled until business and provider requirements are met.

## Phase 5 — Controlled integrations
- [ ] Canva workflow as export/manual handoff first
- [ ] Official social platform OAuth/API review
- [ ] Explicit user approval before publishing
- [ ] Integration disconnect and token revocation
- [ ] Audit logs for every external action

Release gate: no social publishing without explicit account authorization and final user approval.

## Definition of done
A feature is complete only when its implementation exists, relevant tests pass, errors are handled, security boundaries are checked, and the result is verified in the target environment. A checklist item or mock screen alone is not proof of completion.
