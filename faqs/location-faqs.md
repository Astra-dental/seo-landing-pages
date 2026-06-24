# Location Page FAQ Library

Reusable FAQ blocks for service-area landing pages. Swap {{LOCATION}} for the
target area. Mix shared questions with 1-2 location-specific ones per page to keep
content unique and avoid thin/duplicate pages.

## Shared Questions (use on most pages)

**Are you accepting new patients from {{LOCATION}}?**  
Yes — we welcome new patients and families from {{LOCATION}} and across the Fraser Valley.

**Do you offer direct billing and accept the CDCP?**  
Yes, we provide direct billing to all major insurers and accept the Canadian Dental Care Plan.

**What dental services do you offer?**  
General, cosmetic, preventive, orthodontic (braces & Invisalign), endodontic, oral surgery, implants, and more.

**What ages do you treat?**  
We provide care for patients of all ages from 7 years and up, including teens, adults, and seniors.

**Do you offer emergency dental care?**  
Yes. Call us right away for severe pain, swelling, or a broken/knocked-out tooth — we prioritize same-day emergency visits.

## Location-Specific Questions (customize per page)

**How far is Astra Dental from {{LOCATION}}?**  
Astra Dental Centre is a short drive from {{LOCATION}}, at Unit 120, 20061 Fraser Hwy in Langley, with convenient parking behind the building.

**Is parking available when I visit from {{LOCATION}}?**  
Yes — the parkade entrance is behind the building, accessible from 20058 Industrial Ave, Langley.

## Implementation Notes

- Render visible FAQs as `<details>`/`<summary>` accordions for accessibility.
- Mirror the visible Q&A exactly in a `FAQPage` JSON-LD block (see schema-notes).
- Use 3-5 FAQs per page; too many can dilute focus.
- Vary at least one answer per location to keep pages distinct.
