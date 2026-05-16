# Buyer Marketplace App - lux-buyer

Canonical repo location
- `/Users/jon/Desktop/lux-market/lux-buyer`

What it appears to be
- The buyer-facing marketplace application.
- This is the front end where buyers can monitor inventory, log in, view products, and move toward direct purchase behavior.

What the current repo snapshot shows
- The source tree is not currently present in the checked-in workspace snapshot.
- The folder currently contains build artifacts and dependencies, but not the underlying source files.
- Built route manifests indicate:
  - storefront home
  - products listing
  - login flow
  - profile API
  - email OTP auth routes
  - Stripe customer route

What the shared schema suggests
- The buyer app is tied to `buyer_user`, `cart`, `order`, `order_item`, and shared `property` inventory records.
- This supports the idea that Lux is building a real buyer marketplace, not just a hidden seller-only CRM.

Current note quality rule
- Treat this as a real platform surface, but note clearly that the source code is missing from the current repo snapshot and should be re-documented when restored.
