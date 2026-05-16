# Quote Engine - Overview

Goal
- Help Lux produce fast, defensible pricing guidance on teardown and infill opportunities.

Main inputs
- Buyer buy boxes
- System buy boxes
- Buyer quote history
- Attached teardown comps
- New-construction exit signals
- Property and parcel data

Desired output
- A practical offer range
- A best-number sweet spot
- A confidence score
- A list of likely buyers and important parcel risks

Design principles
- Buyer quotes are the strongest truth when recent and nearby
- Comps help seed and triangulate, but should not blindly override behavior
- System intelligence should improve over time without corrupting true buyer-specific preferences
- Operators should be able to see where the number came from

Core process
1. Pull property location and lot details
2. Find all matching buy boxes and system-generated defaults
3. Read nearby buyer quote gradients
4. Apply lot-size and parcel-level adjustments
5. Blend buyer behavior with attached comps and market signals
6. Return floor, ceiling, sweet spot, confidence, and likely buyers

Gradient logic
- Recent and nearby buyer quotes should pull the estimate hardest
- Farther quotes should matter less
- If quote coverage is weak, fall back toward buy-box midpoint and comp-backed defaults

Illustrative estimate structure
- Floor: low executable number based on available buyer reality
- Ceiling: high-end plausible number from the current buyer set
- Sweet spot: best single estimate after blending quote behavior, comp context, and lot logic
- Offer range: practical seller-facing spread below the sweet spot

Confidence model
- High confidence when there are enough nearby quotes and supporting comps
- Medium confidence when some buyer evidence exists but the sample is thin
- Low confidence when the system is leaning mostly on defaults or sparse references

UI direction retained from legacy drafts
- Show buyer quote clustering on the map and in the estimate flow
- Make it obvious which buyers overlap the property
- Let operators manually attach or add comps during estimate review
- Surface parcel risks and exclusions next to the number, not after the fact
