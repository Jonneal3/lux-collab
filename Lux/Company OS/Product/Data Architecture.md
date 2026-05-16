# Data Architecture

Core entities
- Markets
- Neighborhoods
- Buyers
- Buy boxes
- Properties
- Quotes
- Comps
- Contacts
- Communication events

What the system needs to remember
- Which neighborhoods Lux actively cares about
- Which buyers want what, where, and at what price range
- Which properties were evaluated, quoted, and marketed
- Which comps informed pricing
- Which communication events changed buyer or property understanding

Critical relationships
- Buyers can have system-inherited and buyer-specific buy boxes
- Properties can have attached comps and attached quote history
- Market intelligence should improve both system buy boxes and future pricing assumptions
- Communication events should enrich contacts, buyers, properties, and tasks, not sit in isolation

Design rule
- Raw communication is not the product. Structured memory is the product.
