# Environment and Shared Config

Shared env rule from the repo
- Shared variables live in `.env/.env.shared` or legacy `.env.shared` at the monorepo root.
- Per-app variables then layer on top for buyer and seller app specifics.

What is shared
- database URLs
- Supabase project keys
- parcel and comps provider config
- any cross-app infrastructure config

What is app-specific
- buyer-only auth and payment settings
- seller-only auth, SMS, AWS, and operator-facing integration settings

Why this matters for Lux
- The platform is one business system with two apps, not two disconnected products.
- Shared configuration is part of the platform architecture and should be documented as such.
