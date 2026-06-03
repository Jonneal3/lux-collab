#### Contacts & Buyers

- Smarter contact intake workflow.
- ~~Require **City** and **State** when creating buyers.~~
    - ~~Make both dropdowns.~~
    - ~~Pull options from Active Markets.~~
    - ~~Keep database values standardized.~~
- Contact/Buyer/Property merge tool.
    - Detect duplicates.
    - Let user choose which record to keep.
    - Option to preserve all notes, activity, messages, and metadata by appending them to the surviving record.
- Improve contact naming conventions.
- Connect contacts to buyers automatically.
    - Create buyer if one doesn't already exist.
- Start annotating buyers.
- Merge existing duplicate buyers.
- Many builders currently have dummy contacts attached.
    - Audit and clean up builder/contact relationships.

---

#### Communications

- ~~Inbound SMS issue fixed.~~
- ~~SMS messages in conversations improved.~~
- Connect Twilio for inbound call forwarding.
- Forward inbound calls to personal cell phone.
- Pull phone calls into conversation history.
- Investigate Gmail APIs vs IMAP.
- Determine best approach for follow-ups inside CRM.
- Start warming notification email domain.
- Explore using iMessage directly within conversations dashboard while retaining personal phone number usage.

---

#### Performance & UX

- App still feels slow throughout.
- Investigate why tabs and subtabs continue loading.
- Goal:
    - Load organization data into cache at login.
    - Navigation should be near-instant.
    - Minimize API requests after initial load.
- Audit all remaining loading states and unnecessary fetches.

---

#### Follow-Ups & Automation (n8n)

- Build follow-up system.
    - Scheduled emails.
    - Scheduled SMS.
    - Automated sequences.
    - Task reminders.
- Define starting architecture for outbound automation.

---

#### ~~Active Markets~~

- ~~Active Markets settings page.~~
    - ~~Display markets on a map.~~
    - ~~Pull associated ZIP codes automatically.~~
    - ~~Leverage existing market data already stored in DB.~~
    - ~~Provide visual coverage of operating areas.~~

---

#### Buyer Intelligence

- Review existing buyer conversations.
- Extract:
    - Buy boxes.
    - Pricing quotes.
    - Acquisition criteria.
- Add editable Buy Box management.
- Add lot size requirements to Buy Boxes.
- Import Nick's Buy Box criteria from Scott.
- Build AI buyer scoring system.
    - Interest level.
    - Responsiveness.
    - Activity score.
    - "Strength" / likelihood to transact.
- Connect buyer quotes and outcomes to existing properties.

---

#### Property & Comp Data

- Reference addresses can create multiple comp datapoints.
    - If owner purchased and later sold:
        - Purchase price = comp datapoint.
        - Sale price = comp datapoint.
- Parcel size data not being found consistently.
    - Fix parcel lookup.
    - Currently causing inaccurate calculations.

---

#### Documents

- Investigate document upload errors.
- Improve upload reliability and error reporting.

---

#### Integrations & Productivity

- Setup Mac Shortcuts integration.
- Determine how Gmail integration should function long-term.
- Determine how phone, SMS, email, and iMessage should unify inside conversations.

---

#### Data Cleanup

- Sweep through old backlog items and re-prioritize.
- Re-push unfinished historical tasks.

---

#### Admin Tools

- Build Admin Mode Grid View.

---

### Open Questions

- How should builders vs contacts be notified?
- What is the long-term communication architecture?
    - Gmail
    - SMS
    - Calls
    - iMessage
    - Automations
- What is the ideal buyer scoring model?
- How should follow-up sequences be structured across channels?