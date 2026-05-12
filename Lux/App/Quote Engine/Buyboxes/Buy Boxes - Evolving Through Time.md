## Overview

Buy boxes evolve over time as more data enters the platform.

The goal is to:
- Improve pricing accuracy
- Improve buyer matching
- Improve quote confidence
- Better reflect real market behavior

This primarily affects:
- Dirt price per sqft ranges
- Buyer acquisition confidence
- Area-specific pricing assumptions

---
# Independent Evolution

System buy boxes and buyer buy boxes evolve independently.

Buyer buy boxes evolve:
- Per buyer
- Based on that buyer’s behavior only

System buy boxes evolve:
- Per market/area
- Based on aggregate market behavior across all buyers

This separation is important because:
- Buyer buy boxes represent actual buyer behavior and preferences
- System buy boxes represent shared market intelligence

---
# Data Sources

Buy boxes are influenced by:
- Offers
- Sold listings from Properties
- [[Comps System (Separate from Buyers)]]

This relationship is used in real time by the [[Quote Engine]] when generating quotes.

---
# Buyer Buy Box Evolution

Buyer buy boxes evolve independently per buyer.

## Rule 1 — Buyer Drift

A buyer’s historical quote behavior slowly shifts their effective buy box pricing range over time.

Example:
- A buyer consistently quotes above expected dirt values
- That buyer’s effective pricing range slowly drifts upward

This adjustment only affects:
- That buyer
- That buyer’s pricing behavior
- That buyer’s future quote calculations

It does not affect:
- Other buyers
- System buy boxes
- Market-wide pricing assumptions

---

# System Buy Box Evolution

System buy boxes evolve independently from buyer buy boxes.
## Rule 2 — Market Correction

System buy boxes evolve using:
- Aggregate buyer behavior
- Sold listings
- Market comps
- Historical acquisition activity

Example:
- Multiple buyers in Dilworth consistently quote above the starting range
- The Dilworth default system buy box gradually shifts upward

This adjustment affects:
- Future starting pricing assumptions
- System-generated buy boxes in that area
- Buyers inheriting those defaults

It does not directly modify:
- Existing buyer buy boxes
- Buyer-specific acquisition criteria

---

# Long-Term Goal

Over time, the platform becomes:
- A self-improving acquisition intelligence engine
- A real-time pricing engine
- A buyer behavior prediction system