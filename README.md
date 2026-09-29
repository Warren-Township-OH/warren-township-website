# Warren Township Website

Planning and development of the new official website for **Warren Township, Trumbull County, Ohio**.

The goal is a professional, modern, accessible website that helps residents, property owners, businesses, developers, and township staff find services, public information, documents, and the correct contacts.

## Project status

Early planning and prototyping. This repository contains documentation and a plain HTML/CSS prototype. The intended production architecture is Go for the application/server layer, server-rendered HTML templates, selective HTMX for progressive interactivity where it provides a clear user benefit, and Leaflet for interactive Zoning & Property portal mapping. The [current township website](https://www.warrentwptrumbull.gov/) remains the public site and a starting source for content that must be verified before reuse.

The prototype remains the design and information-architecture scaffold while navigation, page hierarchy, and visual structure are being settled. Do not convert it to Go or add HTMX or Leaflet yet; production migration and implementation will happen only after the prototype structure is approved.

## Intended hosting and domain

The township intends to retain `warrentwptrumbull.gov` as its public-facing website address after migration. Production hosting is expected to be in Microsoft Azure. When the new site is ready for production and cutover is separately authorized, DNS can be updated to point that domain to the new Azure-hosted site.

Final Azure service selection and deployment architecture remain undecided and must be determined before production migration. No specific Azure service is selected; that requires a separate later decision. Do not make DNS, hosting, or production cutover changes now. Current prototype work continues locally, unaffected by this decision.

## Approved top-level navigation

- Home
- Government
- Departments
- Zoning & Property
- Residents
- Community & Development
- News & Notices
- Contact

Subpages, final URLs, visual design, launch scope, editing workflow, and remaining platform choices remain open for planning.

## Website and zoning portal

This repository covers the main public website, including its Zoning & Property information, approved public documents, forms, and contacts.

The separate private `warren-township-zoning-portal` repository covers future zoning, property, GIS, mapping, and QGIS work. Interactive portal mapping will use Leaflet. Potential parcel lookup, digital zoning requests, and AI-assisted zoning tools remain subject to separate feature planning. Portal delivery is not a prerequisite for launching the main website.

The Zoning & Property portal is part of the main Warren Township website experience, with the Zoning & Property landing page serving as its public entry point. The separate source/data responsibilities do not make it a separate public experience. Its URL, integration details, deployment arrangement, and release timing remain open. Internal township systems and nonpublic records are outside the public site's scope.

## Project documentation

- [Website plan](docs/website-plan.md): content inventory, proposed page groupings, migration work, open decisions, and milestones.
- [Agent guidance](AGENTS.md): project boundaries and instructions for agents working in this repository.

Preserve the approved navigation, intended production architecture, and existing work. Verify public content, keep remaining technology choices open, and obtain approval for implementation or deployment beyond the current authorized task. A documentation commit does not authorize a change to the live site or domain.
