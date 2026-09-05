# HawaiiMainlandMoving.com implementation plan

Work on hawaii-build-v1 only. Deliver through a draft pull request to main; do not merge or launch.

1. Build the homepage first using static HTML, shared assets/site.css and assets/site.js, with an original Pacific visual identity.
2. Implement accessible Route / Move Details / Contact steps with back/next state retention, per-step validation, visible consent and clear submission status. Preserve the supplied Web3Forms key and exact backend field names. Append packing and vehicle selections to notes.
3. Preserve GA4 and supplied UTM/referrer detection; retain entry attribution across internal navigation with guarded session storage. Track quote clicks, form start, step completion, submission attempts, guides and outbound links. Fire generate_lead only after Web3Forms confirms success. Do not send contact information to analytics.
4. Add a responsive journey animation respecting reduced motion, route explorer, qualitative cost explorer and planning timeline without fabricated prices or transit guarantees.
5. Build substantial primary/reverse direction guides, cost guide, Oahu/Maui/Big Island guides, shipping process and vehicle guides, How It Works, About, Privacy and Terms. Each page has unique metadata, one H1, contextual links and appropriate WebSite/WebPage schema; FAQPage only for corresponding visible FAQs.
6. Add sitemap.xml, robots.txt and 404.html. Use https://hawaiimainlandmoving.com/ canonicals. Keep ModelMoving operator disclosures clear; invent no carrier assets, statistics or reviews.
7. Verify form success/error paths with mocked submissions, analytics event conditions, attribution, links, metadata/schema and mobile behavior. Human launch review covers provider coverage, consent/privacy/terms, GA4 and live CRM delivery.
