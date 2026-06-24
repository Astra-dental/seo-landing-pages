# Local Business / Dentist Schema Notes

Reference for the structured data used on Astra Dental Centre location pages.
Each location page should embed a `Dentist` (a subtype of LocalBusiness) JSON-LD
block in the `<head>`. Keep NAP (Name, Address, Phone) identical to Google Business
Profile and the website footer to avoid local-SEO inconsistencies.

## Canonical NAP

- **Name:** Astra Dental Centre
- **Address:** Unit 120, 20061 Fraser Hwy, Langley, BC, CA
- **Phone:** +1-604-533-8806
- **Email:** reception@astradentalcentre.com
- **Hours:** Mon & Fri 10:00-19:00; Tue-Thu & Sat 09:00-17:00; Sun closed

## Base JSON-LD Block

Replace the slug and areaServed per location. Use one block per page.

```json
{
  "@context": "https://schema.org",
  "@type": "Dentist",
  "name": "Astra Dental Centre",
  "url": "https://astradentalcentre.com/dentist-LOCATION-SLUG/",
  "telephone": "+1-604-533-8806",
  "email": "reception@astradentalcentre.com",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Unit 120, 20061 Fraser Hwy",
    "addressLocality": "Langley",
    "addressRegion": "BC",
    "addressCountry": "CA"
  },
  "areaServed": "LOCATION NAME",
  "openingHoursSpecification": [
    { "@type": "OpeningHoursSpecification", "dayOfWeek": ["Monday","Friday"], "opens": "10:00", "closes": "19:00" },
    { "@type": "OpeningHoursSpecification", "dayOfWeek": ["Tuesday","Wednesday","Thursday","Saturday"], "opens": "09:00", "closes": "17:00" }
  ],
  "aggregateRating": { "@type": "AggregateRating", "ratingValue": "4.9", "reviewCount": "100" }
}
```

## Checklist Before Publishing

- [ ] NAP matches Google Business Profile exactly
- [ ] Canonical URL and schema `url` match the live slug
- [ ] `areaServed` reflects the page's target location
- [ ] aggregateRating reviewCount is current (do not inflate)
- [ ] Validate with Google Rich Results Test before publishing
- [ ] Add FAQPage schema if the page has a visible FAQ section

## FAQPage Schema (optional, when FAQs are present)

Add a separate `FAQPage` JSON-LD block listing the on-page questions/answers so
they remain eligible for FAQ rich results. Mirror the visible Q&A text exactly.
