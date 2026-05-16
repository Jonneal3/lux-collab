# Buy Box System - Product Rules

Product rules
- Users should not directly edit system-generated buy boxes as if they were buyer-owned records
- System-generated buy boxes should act as defaults and fallback logic, not editable user clutter
- Buyer-created buy boxes should always be treated as buyer-owned data
- Source type should not confuse the operator during normal buyer editing flows
- Users should not casually remove the market-default safety net that system buy boxes provide

Operational rules
- System-generated buy boxes should default to the right strategy assumptions for the market
- System and buyer buy boxes should evolve independently
- Market corrections should affect default logic, not rewrite buyer truth
- Buyer-given ranges should remain buyer truth and should not be silently rewritten
- System-generated defaults should behave like safety rails and starting intelligence
