# Astra Dental SEO Landing Pages

Private repository for Astra Dental Centre local SEO landing pages, service-area
page drafts, page templates, and optimization notes.

Website: https://astradentalcentre.com/

## Purpose

This repository organizes local SEO landing page work for Astra Dental Centre, including:

- Service-area ("dentist in {location}") landing pages
- A reusable location page template with SEO meta + local schema
- SEO title and meta description drafts
- On-page heading structure and FAQ blocks
- Internal linking plans
- Local business (Dentist) schema notes
- Content backups before publishing

## Folder Structure

```text
/service-pages              # Reusable templates (_location-template.html)
/langley                    # Langley landing page(s)
/murrayville                # Murrayville landing page(s)
/meta-titles-descriptions   # SEO title + meta description drafts
/faqs                       # Reusable FAQ blocks for location pages
/internal-links             # Internal linking strategy + cluster maps
/schema-notes               # LocalBusiness/Dentist + FAQPage JSON-LD notes
/published-backups          # Snapshots of pages before publishing
```

Additional location folders (e.g. /fort-langley, /cloverdale, /ocean-park) can be
added as those pages are drafted.

## Workflow

1. Copy `service-pages/_location-template.html` into the target location folder.
2. Replace every `{{TOKEN}}` (location, slug, intro, distance, schema fields).
3. Draft the SEO title + meta description in `meta-titles-descriptions/`.
4. Pull FAQs from `faqs/location-faqs.md` and vary at least one per page.
5. Validate JSON-LD with Google's Rich Results Test (see `schema-notes/`).
6. Add internal links per `internal-links/linking-plan.md`.
7. Back up the final HTML in `/published-backups` before it goes live.

## Conventions

- One `<h1>` per page; keep NAP identical to the Google Business Profile.
- Title ~50-60 chars, meta description ~150-160 chars.
- Keep each page's content unique to avoid thin/duplicate-content penalties.

## Security Note

This is a private repository, but please **do not commit secrets** (API keys,
analytics/tracking IDs, access tokens). Keep real values in a secure secrets manager.
