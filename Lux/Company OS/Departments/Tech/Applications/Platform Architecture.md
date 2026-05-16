# Platform Architecture

Current monorepo structure
- `lux-seller`: internal operator-facing Next.js app for acquisitions, dispo, CRM, maps, pricing, and workflow operations
- `lux-buyer`: external buyer-facing Next.js storefront / marketplace experience
- `@lux/db`: shared Prisma schema and import tooling over one Supabase Postgres database

Implication for the vault
- App notes should not sit as one generic `App` bucket.
- Lux really has a platform with two applications plus a shared data layer.
- Product thinking belongs close to Tech, while market and deal intelligence belong under Markets.
