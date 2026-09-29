# Warren Township website rebuild

Working brief prepared September 27, 2026 (America/New_York).

## Purpose and status

Build a professional, modern, accessible official website for Warren Township, Trumbull County, Ohio. Serve residents, property owners, businesses, developers, and township staff with clear paths to public information and services. Use the [current website](https://www.warrentwptrumbull.gov/) as the starting content source. The new site's visual design and content-publishing workflow remain to be selected.

The repository is in early planning and prototyping, with project guidance, website planning documentation, and a plain HTML/CSS prototype. Production application implementation has not begun. Preserve existing files, local changes, and useful research. The eight top-level navigation sections and the intended production architecture below are approved. Page groupings, final URLs, homepage layout, feature details, launch scope, and implementation milestones below remain proposals pending review. Verify existing published content before migration.

## Website and portal boundaries

The main website includes Zoning & Property information, approved public zoning documents and forms, and contacts. The Zoning & Property portal is part of the main Warren Township website experience, with the Zoning & Property landing page serving as its public entry point.

The separate private `warren-township-zoning-portal` repository remains responsible for future portal implementation, spatial datasets, GIS configuration, and QGIS project assets. This source and data boundary is distinct from the shared public website experience. Interactive portal mapping will use Leaflet. Parcel/property lookup, zoning district information, digital zoning requests, and AI-assisted help using township-approved sources remain future possibilities, not an approved feature list. Portal delivery is not a prerequisite for the main website's launch.

The source repository's privacy is separate from the portal's public experience. The public portal URL, launch date, deployment arrangement, and integration details remain to be planned. Publish a portal link only when a public destination is available and approved; maintain useful zoning information and contacts on the main website in the meantime.

Keep public information separate from internal township systems and nonpublic records. A future AI assistant would need source citations, clear limits, and referral to township staff for official determinations. Provider selection, data access, and workflow design belong to a later, separately approved portal decision.

## Intended production architecture

The approved intended production architecture for the website and zoning portal is:

- **Application/server layer:** Go.
- **Page rendering:** server-rendered HTML templates.
- **Progressive interactivity:** HTMX, used selectively where it provides a clear user benefit.
- **Interactive portal mapping:** Leaflet for the Zoning & Property portal.
- **Public experience:** the portal is part of the main Warren Township website experience, entered through the Zoning & Property landing page.

The current plain HTML/CSS prototype remains the design and information-architecture scaffold while navigation, page hierarchy, and visual structure are being settled.

These are planning decisions only. Do not begin converting the prototype to Go or adding HTMX or Leaflet yet. Migration and implementation will happen only after the prototype structure is approved. This architecture decision does not authorize implementation work or dependency changes.

## Intended production hosting and domain

- **Public domain:** the township intends to keep using its current public website domain, `warrentwptrumbull.gov`. It should remain the public-facing address after migration.
- **Production hosting:** the production website is expected to be hosted in Microsoft Azure.
- **Future DNS cutover:** when the new site is ready for production and the cutover is separately authorized, DNS can be updated to point `warrentwptrumbull.gov` to the new Azure-hosted site while retaining the same public address.
- **Decisions still open:** final Azure service selection and deployment architecture must be determined before production migration. No specific Azure service is selected by this plan; make that decision separately later.
- **No changes now:** do not change DNS, hosting, or production cutover settings as part of this planning update.
- **Prototype continuity:** the current prototype work continues locally, unaffected by the hosting decision.

## Resident priorities

Make these tasks easy on a phone and with a keyboard:

- Find the next township meeting, its location, agenda, and available minutes.
- Read current public notices.
- Find zoning and permit instructions and contact the correct office.
- Reach police, fire, road, cemetery, and administration contacts.
- Report a non-emergency concern.
- Find community-center information and request a rental.

## Existing content inventory and proposed page groupings

This inventory covers the homepage and its primary linked pages. It is not a complete crawl or an inventory of private submissions, uploaded files, or unpublished content. The groupings below align with the approved navigation; final subpages and URLs remain undecided.

| Existing page | Observed content or function | Proposed location in the new site |
| --- | --- | --- |
| [Home](https://www.warrentwptrumbull.gov/) | Resident quick links and a concern form | Home; concern reporting under Residents, with a homepage quick link |
| [Administration](https://www.warrentwptrumbull.gov/admin-landing-page) | Links to trustees, fiscal office, zoning, and notices | Government, with links to Zoning & Property and News & Notices |
| [Trustees](https://www.warrentwptrumbull.gov/trustees) | Officials, regular meeting dates, and special meeting notices | Government: trustees and meeting records; link current notices from News & Notices |
| [Fiscal office](https://www.warrentwptrumbull.gov/fiscal-office) | Officeholders and responsibilities | Government: fiscal office |
| [Zoning office](https://www.warrentwptrumbull.gov/zoning-office) | Inspector contact and role description | Zoning & Property, cross-linked from Departments and Contact |
| [Police](https://www.warrentwptrumbull.gov/police-department) | Department information and dispatch, report, and employment actions | Departments: police |
| [Fire](https://www.warrentwptrumbull.gov/fire-department) | Department information, stations, and contact actions | Departments: fire |
| [Road](https://www.warrentwptrumbull.gov/road-department) | Road maintenance, cleanup information, and cemetery information | Departments: roads; resident service and cemetery information under Residents |
| [Recreation / Community center](https://www.warrentwptrumbull.gov/community-center) | Park and facility information, contact details, and rental request form | Community & Development: community center and recreation, cross-linked from Residents |
| [Public notices](https://www.warrentwptrumbull.gov/public-notices) | Notices landing page; no active notices displayed in the retrieved page | News & Notices |

Keep an old-to-new redirect map as routes are finalized. Where one existing page is split, its old URL should redirect to the most relevant landing page, which links to the separated content.

## Approved navigation and proposed homepage

Approved top-level navigation: Home; Government; Departments; Zoning & Property; Residents; Community & Development; News & Notices; Contact. Preserve these sections unless the user approves a change. Subpages and final URLs remain open for planning.

Working descriptions for review:

| Section | Proposed purpose |
| --- | --- |
| Home | Quick access to common tasks, urgent alerts, upcoming meetings, and current updates |
| Government | Township leadership, governance, meetings, agendas, minutes, and public-records information |
| Departments | Department responsibilities, services, and verified contacts |
| Zoning & Property | Public zoning guidance, documents, forms, property resources, and future portal access |
| Residents | Everyday services, concern reporting, and practical help |
| Community & Development | Community facilities, recreation, and verified planning and development resources |
| News & Notices | Dated news, public notices, and clearly labeled archives |
| Contact | A verified contact directory, office hours, locations, and directions to the right office |

Group pages around the tasks people need to complete. Cross-link related information instead of maintaining conflicting copies. The existing site's inventory is a migration starting point, not a limit on the approved structure. Collect suitable content for all eight sections before confirming launch coverage.

Proposed homepage order:

1. Township identity, location, and clear navigation.
2. Important notice banner when an active notice warrants it.
3. Resident quick links: zoning, meetings, report a concern, community center, cemeteries, and contacts.
4. Next confirmed meeting, with time, location, and available documents.
5. Current notices and dated community updates.
6. Department links and a consistent contact footer.

Use the township seal and local photography once original assets and reuse rights are confirmed. Aim for a consistent, trustworthy civic identity and clear page layouts. Design for readable text, clear focus states, sufficient contrast, accessible forms, and mobile navigation from the first prototype. Avoid image-only notices and essential information available only in PDFs. Visual references may inform the design; no reference site, visual style, or template has been selected.

Before approving a prototype, review keyboard navigation, headings and landmarks, text resizing and zoom, mobile layout, meaningful link labels and alternative text, and form labels and errors. Establish the formal accessibility acceptance standard during requirements review; do not claim conformance from a visual review alone.

## Content to verify or collect

The initial public-page review recorded the following observations. Retrieved pages may be cached; these are leads for township verification, not a claim that every detail is current or correct.

- **Zoning email:** the [retrieved zoning page](https://www.warrentwptrumbull.gov/zoning-office) shows `twilson@warrentwptrumbull.go` as the email destination. Intended address will be zoning@warrentwptrumbull.gov. Verify before publishing.
- **Meeting schedule:** the [retrieved trustees page](https://www.warrentwptrumbull.gov/trustees) describes meetings on the last Tuesday of the month but lists September 22, 2026. Confirm the actual schedule, locations, cancellations, and special meetings; do not generate dates solely from the recurring rule.
- **Fire stations:** the [retrieved fire page](https://www.warrentwptrumbull.gov/fire-department) lists the same street address for Stations 47, 48, and 49. Confirm each station's public contact/location details.
- **Dated updates:** the [retrieved road page](https://www.warrentwptrumbull.gov/road-department) includes a May 2026 cleanup and the trustees page includes August 2026 special meetings. Establish current and archived views so past events are not presented as upcoming.
- **Documents:** request the authoritative agendas, minutes, zoning forms/resolution, fee schedules, rental terms, and records-request instructions. Their completeness was not established by this review.
- **Contacts:** confirm officeholders, titles, public phone numbers, dispatch numbers, office hours, addresses, and a content owner for each department.
- **Assets:** obtain original seal files, usable local photos, and relevant captions or alternative text.

These are verification items, not corrections authorized for the existing live website.

## Workflows that must survive migration

### Report a concern

The homepage exposes a form with contact information, a department/category selection, and comments. Confirm recipients and staff handling before implementation. Provide clear non-emergency guidance, accessible validation, spam protection, and accurate success/failure feedback. A confirmation must reflect an accepted submission, not merely a button click. Keep resident submissions out of the public repository and public content API.

### Community-center rental request

The community-center page exposes contact fields, room choices, and a requested date/time. Confirm the current options, routing, fees, and approval process. Treat submission as a rental request unless staff confirms an actual booking workflow. Acknowledgment must not imply that the facility is reserved.

The public review did not submit either form or verify its backend delivery. Identify current form storage, recipients, and any necessary historical export with the site administrator. Test the replacements with designated staff before launch.

## Publishing and remaining platform decisions

Open decision: will township staff publish through a simple editor, will a developer maintain content in GitHub, or will both participate?

- If staff will edit content, evaluate an editing workflow with drafts, preview, document uploads, and appropriate publishing access.
- Developer maintenance can use structured content in the repository, rendered through the planned Go application and HTML templates.
- Either approach should separate design from content and support reusable department pages, meeting records, dated notices, and document metadata.

The application language, rendering approach, selective interactivity, mapping library, and intended hosting direction are recorded above. Microsoft Azure is the expected production hosting platform; final Azure service selection and deployment architecture remain open and must be determined before production migration. Any Go framework, content system, database, and form service remain open until editing responsibilities, maintenance needs, budget, and requirements are understood. No specific Azure service, form-service vendor, or ongoing cost is selected by these planning decisions.

The intended production architecture above records the approved direction. Record the remaining platform and publishing choices and their maintenance implications after approval.

## Decisions still needed

- Launch content and priority resident tasks, including the proposed subpage groupings and section descriptions.
- Who edits, reviews, publishes, and maintains content; who owns each department's information.
- Budget, final Azure service selection and deployment architecture before production migration, hosting and maintenance responsibility, publishing workflow, and form routing.
- Approved visual assets, design direction, and accessibility acceptance criteria.

## Authorization and review

The build sequence is provisional. Work within the user's current authorization; an explicit request to make specified edits or commit and push them is approval for that scope. Obtain approval for substantial work outside it, application scaffolding, dependency installation, or architecture decisions. Publishing or changing the live site or domain requires explicit authorization. Committing or pushing these planning documents does not authorize a live-site cutover.

Approval of the prototype structure is required before production migration or implementation. Until then, keep the prototype in plain HTML/CSS; do not convert it to Go or add HTMX or Leaflet.

## Build sequence

1. **Planning foundation:** review launch scope, proposed section descriptions and page groupings, editors, content owners, source material, and remaining platform choices. Record approved decisions before implementation.
2. **Prototype preview and structure review:** continue the plain HTML/CSS prototype with the shared header/footer, homepage, Residents page, Departments page, and a proposed Zoning & Property landing page only within the authorized prototype scope. Establish the design and content structure using real, verified content and identify preview placeholders explicitly. Settle navigation, page hierarchy, and visual structure, then obtain approval of the prototype structure before production migration or implementation.
3. **Production implementation, after prototype structure approval:** migrate to the intended production architecture and provide agreed content across the eight navigation sections, including government and department pages, zoning resources, resident services, community and development resources, contact information, meetings, news, notices, available documents, and approved forms.
4. **Verify and launch:** review mobile and keyboard use, accessibility, links and downloads, form delivery, content accuracy, redirects, metadata, and publishing workflow. Prepare the domain cutover and rollback steps.

Current prototype work remains local/development work. A future deployed preview should use a separate preview URL. When the Azure-hosted site is ready for production and cutover is authorized, update DNS for `warrentwptrumbull.gov` to the new site while retaining that public address. No DNS, hosting, or production cutover changes are authorized now. At the future cutover, preserve email-related DNS records and verify both the `www` and bare-domain behavior.

## Immediate planning milestone

- Approved top-level navigation is reflected consistently in the project documents.
- Proposed subpage groupings, launch scope, section descriptions, and content gaps are ready for user review.
- Editing responsibilities, maintenance needs, budget, remaining platform choices, and accessibility acceptance criteria are identified for decision.
- Website and portal source/data responsibilities remain distinct within the shared public website experience, and existing research is preserved.

## Prototype approval milestone

- Approved in-scope page prototypes listed below are built with consistent navigation and responsive layout.
- Current prototype scope includes the homepage, Residents, Departments, and proposed Zoning & Property landing pages.
- Verified content is clearly distinguished from placeholders and information still requiring verification.
- Basic keyboard navigation, mobile layout, headings, landmarks, link labels, focus states, and readable contrast are reviewed.
- Major page structure, navigation, and content groupings are reviewed and approved.
- Proposed URLs and remaining content gaps are documented.
- No production migration or implementation begins until the prototype structure is approved.

## First production implementation milestone, after prototype approval

- Scaffold the production website using Go with server-rendered HTML templates.
- Convert the approved prototype structure into reusable templates for the shared header, navigation, footer, and page layouts while preserving the approved design and information architecture.
- Establish production routes for the approved website pages and begin replacing prototype placeholders with verified township content.
- Introduce HTMX selectively only where an approved feature clearly benefits from progressive interactivity; do not add it where ordinary server-rendered HTML is sufficient.
- Introduce Leaflet when implementation reaches the approved public-facing interactive mapping scope. Portal-specific GIS data, application processing, and backend integration remain separately scoped and are not authorized by this milestone.
- Confirm the publishing and content-maintenance approach before building staff editing or content-management features.
- Continue accessibility, mobile, keyboard, content-accuracy, and link testing throughout implementation.
- Production deployment, Azure configuration, DNS changes, and public cutover remain separate later steps requiring explicit approval.

## Review limits and verification boundaries

- Public-site research and prototype review do not establish full accessibility conformance, backend form behavior, administrator workflows, analytics, or production readiness.
- Prototype review covers structure, navigation, responsive behavior, basic keyboard use, content organization, and visible accessibility issues only.
- Township facts, contacts, schedules, forms, fees, policies, and documents must be verified from authoritative sources before publication.
- Production implementation will require separate testing of forms, integrations, security, accessibility, redirects, deployment, and content accuracy.
- A successful prototype review does not authorize production deployment or DNS cutover.

The initial review used public page text and browser inspection of the community-center and zoning pages. It did not assess administrator access, analytics, all downloadable files, full accessibility conformance, or backend form processing. A later documentation review rechecked retrieved homepage, zoning, trustees, fire, road, and notices text; the community-center page could not be retrieved again, so its initial findings remain unverified for migration. Retrieved pages may be cached. Retrieval failures were not treated as proof of a public outage.
