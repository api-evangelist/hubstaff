# Hubstaff (hubstaff)

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
