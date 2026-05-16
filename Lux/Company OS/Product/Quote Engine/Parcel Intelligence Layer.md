# Parcel Intelligence Layer

Purpose
- Add parcel-specific buildability and desirability context that pure pricing data misses.

Fundamentals
- Lot size
- Lot dimensions
- Lot shape
- Slope
- Trees or other physical constraints where possible
- Directionality from nearby comps and street context where useful

Zoning and restriction signals
- Height limits
- Lot coverage
- Frontage and setbacks
- Historic district status
- Flood-zone status
- Buildable area implications where they can be derived
- Zoning use and density context

Buyer-preference signals
- Busy-road exposure
- Views
- Pool-market relevance
- Surrounding uses
- Neighborhood micro-location quality
- Corner-lot versus interior-lot preference
- Near-beach or near-school context where relevant

Data-source direction
- Parcel and county GIS data
- FEMA
- USGS or elevation APIs
- City zoning maps and bylaws
- Google or map-based contextual data where useful
- Traffic or road-class data for busy-road scoring

Operational rule
- Parcel intelligence should help explain why two similar lot sizes can deserve very different pricing.
