# RCFS hubs — Backend Foundation

This is the initial server-side foundation for RCFS hubs. It is intentionally safe to upload to a private GitHub repository because it contains no real API keys or payment secrets.

## Local setup

1. Install Node.js 20+.
2. Run `npm install`.
3. Create `.env` from `.env.example`.
4. Put secrets only in `.env` locally or in your hosting provider's secret/environment settings.
5. Run `npm run dev` for development.
6. Run `npm run build && npm start` for production.

## Render settings

For a Render Web Service:

- Runtime: Node
- Build Command: `npm install && npm run build`
- Start Command: `npm start`

Set the environment variables in Render, including `FIVESIM_API_KEY`. Do not put the real 5SIM key in GitHub.

## Important

This is a backend foundation, not the complete RCFS hubs production application. The next implementation stages should add authentication, PostgreSQL migrations/schema, wallet ledger transactions, orders, 5SIM server-side integration using the current official API documentation, payment webhooks, refund state machine, SMS polling, background worker, RBAC, audit logs, rate limiting, and production security controls.
