# Warren Township website — project guidance

This repository contains the new official website for Warren Township, Trumbull County, Ohio.

The goal is a professional, modern, accessible local-government website that helps residents find information, services, documents, and the correct township contacts.

## Project boundaries

The separate private `warren-township-zoning-portal` repository is reserved for future zoning, property, GIS, and QGIS work. Keep its implementation and data separate from this website.

The main website needs a public-facing Zoning & Property section with information, approved public documents and forms, and contacts. The Zoning & Property portal is part of the main Warren Township website experience, with the Zoning & Property landing page serving as its public entry point. The separate source/data boundary does not define a separate public experience. Portal implementation is not currently authorized or a prerequisite for launch. Do not confuse the private source repository with a public portal URL.

Keep internal township systems, nonpublic records, resident submissions, and credentials out of public website content and the public repository. A future portal integration requires its own scope and approval.

## Intended top-level navigation

Preserve these sections unless the user approves a change:

- Home
- Government
- Departments
- Zoning & Property
- Residents
- Community & Development
- News & Notices
- Contact

Subpages and final URLs remain open for planning.

## Current phase and existing work

We are in early planning and prototyping. The plain HTML/CSS prototype remains the design and information-architecture scaffold while navigation, page hierarchy, and visual structure are being settled. Preserve existing files, local changes, and useful research.

Use [README.md](README.md) for the project overview and [docs/website-plan.md](docs/website-plan.md) when planning content, navigation, migration, or implementation. The top-level navigation above is approved; proposed subpages, page groupings, features, and URLs remain provisional. Keep these documents consistent when an approved decision changes.

The intended production architecture is Go for the application/server layer, server-rendered HTML templates, selective HTMX for progressive interactivity where it provides a clear user benefit, and Leaflet for interactive Zoning & Property portal mapping. Do not begin converting the prototype to Go or adding HTMX or Leaflet yet. Production migration and implementation will happen only after the prototype structure is approved; recording the architecture does not authorize implementation or dependency changes.

The township intends to retain `warrentwptrumbull.gov` as its public-facing domain, with production hosting expected in Microsoft Azure. Final Azure service selection and deployment architecture must be decided separately before production migration; do not lock the plan to a specific Azure service now. DNS may point the retained domain to the new Azure-hosted site only when it is ready for production and cutover is authorized. Do not make DNS, hosting, or production cutover changes now. Current prototype work continues locally, unaffected by this decision.

Keep any Go framework, CMS, database, and form-service decisions open until editing responsibilities, maintenance needs, budget, and requirements are understood.

## Content and design expectations

Prioritize clear language, mobile usability, keyboard navigation, visible focus, readable contrast, semantic structure, and accessible forms and documents.

Use the existing township website as a content source, with verification before reuse. Do not invent officials, contacts, meeting dates, fees, policies, or zoning requirements. Identify missing information clearly.

## Working approach

Confirm the target repository and inspect the files and local changes relevant to the task before editing. Preserve unrelated work and existing research. Explain material conflicts with the approved goals, and distinguish confirmed requirements from proposals and missing information.

Work within the user's current authorization; an explicit request to make specified edits or commit and push them is approval for that scope. Obtain approval before substantial work outside it, application scaffolding, dependency installation, or architecture decisions. Publishing and changes to the live website or domain require explicit authorization; pushing planning documents is not permission for a live-site cutover.
