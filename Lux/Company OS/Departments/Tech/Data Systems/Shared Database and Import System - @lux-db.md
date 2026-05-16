# Shared Database and Import System - @lux-db

Canonical repo location
- `/Users/jon/Desktop/lux-market/packages/database`

What it is
- The shared Prisma schema, generated client, seed scripts, backfills, and import tooling used by both applications.

Monorepo role
- `@lux/db` is the single database layer for both `lux-seller` and `lux-buyer`.
- Both apps point at the same Supabase Postgres project.

Key shared entities visible in the schema
- `property`
- `buyer`
- `buy_box`
- `organization`
- `contact`
- `conversation`
- `order`

Operational importance
- This is not just a technical dependency. It is the system of record for Lux market data, buyer intelligence, CRM objects, marketplace inventory, and transaction flows.

Key import and maintenance capabilities already present
- buyers import
- contacts import
- properties import
- mbox and iPhone conversation import
- buyer/contact merge and cleanup
- active-market seeding
- system-generated buy-box seeding and backfills
- teardown comp backfills and enrichment
