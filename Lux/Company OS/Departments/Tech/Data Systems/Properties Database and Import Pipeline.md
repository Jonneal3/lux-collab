# Properties Database and Import Pipeline

Core rule
- The properties database belongs under shared app infrastructure, not under market notes.

Why
- In the schema, `property` is the shared CRM and marketplace parcel / listing / deal record.
- A property row can serve as:
  - a seller-side CRM lead
  - a tracked parcel under review
  - active inventory in the buyer marketplace
  - a record connected to quotes, comps, contacts, and orders

Canonical import path in the repo
- `/Users/jon/Desktop/lux-market/packages/database/prisma/import-records-properties-csv.ts`
- package script: `db:import:records-properties`

What the import script does
- Imports Records CSV rows into `properties`
- Upserts on `external_record_id`
- Maps contract value into `seller_contract_price`
- Maps target sales price into `target_asking_price`
- Resolves organization and seller-user ownership before insert/update
- Creates the property rows before they are pinned and worked inside the app

Operational implication
- The app should be treated as the immediate home for operational property data.
- Market playbooks and deal notes in the vault are context and intelligence layers, not the source-of-truth database for properties.
