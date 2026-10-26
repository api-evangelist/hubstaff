# Hubstaff (hubstaff)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Hubstaff is a time tracking and workforce analytics platform for remote, hybrid, and field teams. The Hubstaff API v2 (`https://api.hubstaff.com/v2`) provides read and write access to tracked time (10-minute activity blocks and daily aggregates), time entries, timesheets and approvals, time off, attendance schedules and shifts, organizations, members, teams, projects, tasks, clients, invoices, team payments, screenshots, app and URL usage, and webhooks.

The API is publicly documented at the [Hubstaff Developer Portal](https://developer.hubstaff.com/), with a live machine-readable definition published at [https://api.hubstaff.com/v2/docs](https://api.hubstaff.com/v2/docs). Access requires a Hubstaff account: authentication is OpenID Connect / OAuth 2.0 through Hubstaff Account (`https://account.hubstaff.com`), with scopes `hubstaff:read` and `hubstaff:write`. For server-side scripts, Hubstaff issues personal access tokens (created at [developer.hubstaff.com/personal_access_tokens](https://developer.hubstaff.com/personal_access_tokens)) that act as OAuth refresh tokens - they expire after 90 days and are exchanged for short-lived access tokens via the standard refresh-token grant at `https://account.hubstaff.com/access_tokens`. Authenticated users are allowed 1,000 requests per hour per application, and all requests must use HTTPS. API v1 is deprecated; v2 is the current version.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/hubstaff/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/hubstaff/refs/heads/main/apis.yml)

## Tags

- Time Tracking
- Timesheets
- Workforce Management
- Productivity
- Employee Monitoring
- Project Management
- Payroll

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### Hubstaff Activities and Time Tracking API

Tracked time as 10-minute activity blocks with keyboard and mouse activity percentages, pre-aggregated daily activities, and the most recent activity per member - filterable by user, project, task, and time range at both the organization and project level.

- **Human URL:** [https://developer.hubstaff.com/docs/hubstaff_v2](https://developer.hubstaff.com/docs/hubstaff_v2)
- **Base URL:** `https://api.hubstaff.com/v2`

#### Tags

- Time Tracking
- Activities
- Productivity

#### Properties

- [API Reference](https://developer.hubstaff.com/docs/hubstaff_v2)
- [Documentation](https://support.hubstaff.com/time-tracking-api/)
- [OpenAPI](openapi/hubstaff-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hubstaff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hubstaff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hubstaff Timesheets and Time Entries API

Create time entries for users, list organization timesheets (aggregate approval records), move timesheets through the open, submitted, approved, and denied statuses, and audit manual time edits via time edit logs. Note that manual time entries that require approval cannot be added through the API.

- **Human URL:** [https://developer.hubstaff.com/docs/hubstaff_v2](https://developer.hubstaff.com/docs/hubstaff_v2)
- **Base URL:** `https://api.hubstaff.com/v2`

#### Tags

- Timesheets
- Time Entries
- Approvals

#### Properties

- [API Reference](https://developer.hubstaff.com/docs/hubstaff_v2)
- [OpenAPI](openapi/hubstaff-openapi.yml)
- [Postman Collection](collections/hubstaff.postman_collection.json)
- [Open Collection](collections/hubstaff.opencollection.json)

### Hubstaff Organizations and Teams API

Manage organizations, seats, members and their pay and bill rates, teams and team membership, and invites - the workforce structure that all tracked time hangs off of.

- **Human URL:** [https://developer.hubstaff.com/docs/hubstaff_v2](https://developer.hubstaff.com/docs/hubstaff_v2)
- **Base URL:** `https://api.hubstaff.com/v2`

#### Tags

- Organizations
- Teams
- Members
- Workforce Management

#### Properties

- [API Reference](https://developer.hubstaff.com/docs/hubstaff_v2)
- [OpenAPI](openapi/hubstaff-openapi.yml)
- [Postman Collection](collections/hubstaff.postman_collection.json)
- [Open Collection](collections/hubstaff.opencollection.json)

### Hubstaff Projects and Tasks API

Create and manage projects (including budgets and project members) and tasks (to-dos) at the project and organization level. Tasks synced from third-party integrations are read-only through the API and must be changed in the integrated tool.

- **Human URL:** [https://developer.hubstaff.com/docs/hubstaff_v2](https://developer.hubstaff.com/docs/hubstaff_v2)
- **Base URL:** `https://api.hubstaff.com/v2`

#### Tags

- Projects
- Tasks
- Project Management

#### Properties

- [API Reference](https://developer.hubstaff.com/docs/hubstaff_v2)
- [OpenAPI](openapi/hubstaff-openapi.yml)
- [Postman Collection](collections/hubstaff.postman_collection.json)
- [Open Collection](collections/hubstaff.opencollection.json)

### Hubstaff Users API

Retrieve the authenticated user (`/users/me`) and individual user profiles by ID.

- **Human URL:** [https://developer.hubstaff.com/docs/hubstaff_v2](https://developer.hubstaff.com/docs/hubstaff_v2)
- **Base URL:** `https://api.hubstaff.com/v2`

#### Tags

- Users
- Profiles

#### Properties

- [API Reference](https://developer.hubstaff.com/docs/hubstaff_v2)
- [OpenAPI](openapi/hubstaff-openapi.yml)
- [Postman Collection](collections/hubstaff.postman_collection.json)
- [Open Collection](collections/hubstaff.opencollection.json)

### Hubstaff Time Off and Attendance API

Time off requests with approval workflow and balance previews, time off policies and balances, attendance schedules (expected shifts, including repeating schedules), actual clock-in and clock-out attendance shifts, and organization holidays.

- **Human URL:** [https://developer.hubstaff.com/docs/hubstaff_v2](https://developer.hubstaff.com/docs/hubstaff_v2)
- **Base URL:** `https://api.hubstaff.com/v2`

#### Tags

- Time Off
- Attendance
- Scheduling
- Workforce Management

#### Properties

- [API Reference](https://developer.hubstaff.com/docs/hubstaff_v2)
- [OpenAPI](openapi/hubstaff-openapi.yml)
- [Postman Collection](collections/hubstaff.postman_collection.json)
- [Open Collection](collections/hubstaff.opencollection.json)

### Hubstaff Clients, Invoices, and Payments API

Manage the clients projects are billed to, list client invoices, and list team payments (payroll) generated from tracked time.

- **Human URL:** [https://developer.hubstaff.com/docs/hubstaff_v2](https://developer.hubstaff.com/docs/hubstaff_v2)
- **Base URL:** `https://api.hubstaff.com/v2`

#### Tags

- Clients
- Invoicing
- Payroll

#### Properties

- [API Reference](https://developer.hubstaff.com/docs/hubstaff_v2)
- [OpenAPI](openapi/hubstaff-openapi.yml)
- [Postman Collection](collections/hubstaff.postman_collection.json)
- [Open Collection](collections/hubstaff.opencollection.json)

### Hubstaff Screenshots and App Tracking API

Retrieve screenshots captured while tracking time, application and URL usage (raw and daily aggregates), and read or update the organization's app and URL tracking settings.

- **Human URL:** [https://developer.hubstaff.com/docs/hubstaff_v2](https://developer.hubstaff.com/docs/hubstaff_v2)
- **Base URL:** `https://api.hubstaff.com/v2`

#### Tags

- Screenshots
- Activity Monitoring
- App Tracking

#### Properties

- [API Reference](https://developer.hubstaff.com/docs/hubstaff_v2)
- [OpenAPI](openapi/hubstaff-openapi.yml)
- [Postman Collection](collections/hubstaff.postman_collection.json)
- [Open Collection](collections/hubstaff.opencollection.json)

### Hubstaff Webhooks API

Subscribe to real-time HTTP event notifications at the organization, project, or user level - timer.start, timer.stop, project.create, task.create, task.assign, schedule and shift events, work breaks, and billing seat snapshots - with an X-Hook-Secret verification and activation handshake and signed deliveries.

- **Human URL:** [https://developer.hubstaff.com/docs/hubstaff_v2](https://developer.hubstaff.com/docs/hubstaff_v2)
- **Base URL:** `https://api.hubstaff.com/v2`

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [API Reference](https://developer.hubstaff.com/docs/hubstaff_v2)
- [OpenAPI](openapi/hubstaff-openapi.yml)
- [Postman Collection](collections/hubstaff.postman_collection.json)
- [Open Collection](collections/hubstaff.opencollection.json)

## Common Properties

- [GitHub Organization](https://github.com/NetsoftHoldings)
- [LinkedIn](https://www.linkedin.com/company/hubstaff)
- [Website](https://hubstaff.com)
- [Documentation](https://developer.hubstaff.com/)
- [Pricing](https://hubstaff.com/pricing)
- [Support](https://support.hubstaff.com/)
- [Blog](https://hubstaff.com/blog)
- [Plans](plans/hubstaff-plans-pricing.yml)
- [Rate Limits](rate-limits/hubstaff-rate-limits.yml)
- [Fin Ops](finops/hubstaff-finops.yml)

## Access Model

The Hubstaff API is public and documented, but it is an account-holder API rather than an anonymous one - every request operates on the organizations the authenticated user belongs to. There is no separate API subscription: API access comes with a Hubstaff account (paid plans start at $4.99/user/month billed annually, with a 14-day free trial and a single-user free tier). OAuth 2.0 / OpenID Connect is used for apps acting on behalf of users; personal access tokens (90-day refresh tokens exchanged for access tokens) cover server-side scripts.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
