# Draft review — HawaiiMainlandMoving.com

## Delivered
13 indexable static pages (homepage plus all 12 named supporting routes), custom 404, shared CSS/vanilla JavaScript, sitemap, robots file and optimized Oahu photo. No framework, runtime build dependency, custom-domain configuration or deployment was added.

The homepage includes a three-step quote flow in either direction, an animated/selectable six-stage journey, island route explorer, qualitative cost explorer and date-based preparation reminders. Reduced-motion CSS stops the ship animation. Root-relative links target a domain-root deployment, as requested.

## Form and attribution
The supplied Web3Forms access-key implementation, GA4 property and exact backend field names are preserved. Vehicle/packing selections are appended to notes. Provider success must be explicitly true and the HTTP response successful before generate_lead fires. Duplicate submissions are blocked while pending; failures retain entered values; success resets the form and step.

UTMs take priority over referrer classification. Entry attribution is retained through internal navigation with guarded session storage. Analytics events cover primary CTAs, form start, step completion, attempt, successful lead, guide links and ModelMoving/MoveReady links. Contact details and free-text route addresses are omitted from custom analytics events; the complete route remains in the form payload.

## Verification
`tools/verify.cjs` uses jsdom with mocked fetch (no real leads or GA traffic). It passed 626 assertions covering source detection, UTMs and entry persistence, route validation, step/back retention, reverse direction, payload keys, duplicate prevention, confirmed success, HTTP/provider/network/JSON failures, reset behavior, navigation, explorers, 13 page metadata/canonicals/H1s, schema/visible FAQs, links and anchors. JavaScript syntax passes Node checking.

Browser visual and viewport verification was not performed: the provided Sites preview environment does not support plain static assets. Responsive CSS is implemented for narrow phones through desktop, with 16px inputs, generous controls and reduced motion, but this is not a claim of tested rendering at every viewport. Complete phone/desktop visual review before launch.

## Human review before launch
- Verify the privacy notice, consent, terms, business contact route and retention practices against the actual ModelMoving operation; these are draft website disclosures, not a legal compliance certification.
- Confirm selected-provider coverage for islands and both directions, and vehicle/commercial requests.
- Confirm this domain belongs under the supplied GA4 property and configure any analytics-consent requirements appropriate to the operation.
- Perform one authorized end-to-end Web3Forms → automation → CRM test; no real request was sent during this build. Check Web3Forms domain restrictions if enabled.
- Approve visual rendering on target devices, then choose the launch configuration. No CNAME or DNS changes were made. If GitHub Pages custom-domain setup is later used, CNAME must contain only hawaiimainlandmoving.com.
- Review and merge only when ready. This deliverable is a draft PR, not a launch.

## Sources and asset
- Ocean-provider background: https://www.matson.com/hhg-personal/index.html
- Vehicle preparation resource: https://www.pashahawaii.com/resources/vehicles/ship-vehicle-shipping-checklists
These links are explicitly independent resources, not partnership claims.
- Hero: Michael Olsen, Pele’s Chair, Honolulu. https://unsplash.com/photos/aerial-view-of-body-of-water-during-daytime-93B6TiJlk5Y — Unsplash License: https://unsplash.com/license . Optimized WebP; credit in footer.

## Maintenance
Edit shared behavior in assets/site.js and styling in assets/site.css. Content sources are tools/build.py and tools/home.html; run python3 tools/build.py to regenerate static HTML. The generator reuses the key from the existing index.html when the original attachment is unavailable. It never prints the key. The tools directory is maintenance source, not a runtime dependency. A jsdom installation is needed only for tools/verify.cjs, not the website.
