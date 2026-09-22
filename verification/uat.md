# UAT Runbook — Product-7 (System Telemetry & Metrics Aggregation)

## Feature
Operational telemetry recording and Prometheus metric scraping

## Preconditions
- Service is configured with valid environment (`.env.local` or `.env.example`).
- Database migrations have been applied via `make migrate`.
- Required port is free and accessible.

## Steps
1. Start Product-7 on port 8087
2. Record telemetry event via POST /api/v1/telemetry
3. Query GET /metrics and inspect Prometheus formatted counters

## Expected Results
- Telemetry event accepted and persisted
- /metrics output includes valid Prometheus exposition lines

---
*Author: QA & Primary Owner (MasterSpec Section 31.1, Section 33.1)*
*Verification Contract: `verification/contract.yaml`*
