# Tines

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

Tines is a no-code intelligent workflow automation platform built for security teams. It allows security practitioners to automate repetitive tasks and build sophisticated workflows (called "stories") without writing custom code. The platform connects tools, teams, and AI agents to automate security and IT operations at scale.

## API

The Tines REST API provides programmatic access to all platform resources. The API base URL follows the pattern `https://{tenant-domain}/api/v1/{endpoint}` where each Tines customer has a unique tenant subdomain.

**Documentation:** https://www.tines.com/api/welcome/

### Authentication

The API supports two authentication methods:

- `X-User-Token` header containing an API key
- `Authorization: Bearer {token}` header

Four types of API keys are available: Personal, Service, Tenant Owner, and Team API keys, each with different scope and permission levels.

### Key API Resources

- **Stories** - Workflow definitions and automation sequences
- **Actions** - Individual steps within stories
- **Credentials** - Managed secrets and API key storage
- **Teams** - User group and collaboration management
- **Cases** - Incident and case management
- **Records** - Structured data storage
- **Audit Logs** - Compliance and activity tracking
- **AI Usage** - Token counts and AI credit consumption by model/provider
- **SCIM** - Identity and access provisioning
- **Webhooks** - Inbound triggers for automated workflows
- **Dashboards** - Visualization and monitoring
- **Workbench** - Development and testing environment

### Rate Limits

Most endpoints: **5000 requests/minute** (per IP + API token combination). Specific endpoints have lower limits (actions: 100/min, records: 400/min). Exceeds return HTTP 429.

## Developer Resources

| Resource | URL |
|---|---|
| API Documentation | https://www.tines.com/api/welcome/ |
| Go SDK | https://github.com/tines/go-sdk |
| Terraform Provider | https://github.com/tines/terraform-provider-tines |
| GitHub Organization | https://github.com/tines |
| Story Library | https://www.tines.com/library/ |
| Status Page | https://status.tines.com/ |

## Pricing

Tines uses event-based pricing rather than seat-based licensing:

- **Community Edition** - Free, single-user, unlimited stories with core actions
- **Starter** - $500/month, 1M events/month, 5-20 flows
- **Enterprise** - Custom pricing, unlimited flows, SSO, audit logs, SCIM, SLA

See [plans/tines-plans-pricing.yml](plans/tines-plans-pricing.yml) for full details.

## Links

- **Website:** https://www.tines.com/
- **Blog:** https://www.tines.com/blog/
- **LinkedIn:** https://www.linkedin.com/company/tines-io
- **X:** https://x.com/tines_hq
- **Status:** https://status.tines.com/
