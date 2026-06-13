# Tines

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
