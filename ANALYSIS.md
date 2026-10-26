# to.co Business Page Domains: Opportunity Analysis in an Agentic World

## Executive Summary

to.co provides free, AI-readable business pages and addresses (e.g., `yourname.uk.to.co`) with structured data via HTML, JSON, Markdown, and an MCP server. In an agentic world, where AI agents autonomously discover, interact with, and manage business operations, to.co can evolve from a static public record into a full **agentic business operating system** for SMBs. This includes owner apps for management, AI agents handling enquiries/CRM/content, B2B portals, integrations, and secure document/payment flows.

**Key Opportunity**: SMBs suffer from fragmented tools (Google Business, website builders, CRM, social managers, accounting, maps). to.co + ABIZ + MCP can be the single source of truth that agents and humans consume, with agents running on behalf of owners.

## Existing Features (from public to.co, MCP docs, ABIZ)

### Core Public Offering
- Free business record and public page at to.co address.
- Registered companies: name-based under country (e.g., `yourname.or.us.to.co`).
- Unregistered: name + town (e.g., `yourname-yourtown.biz.to.co`).
- Paid shorter premium domains (e.g., `yourname.to.co`).
- Multi-format: HTML (people), `?format=json` (software), `?format=md` (AI).
- Edge-served, pre-rendered, cache-busting on updates.
- Preview before publish; nothing public until Publish.
- QR codes (basic free, branded paid).
- Language support (multiple locales).

### Content & Widgets (inferred from site/blogs)
- Services / main buttons (Book, Order, Get Quote, etc.): Free=3, Starter=10+.
- Photos: Free=3, more on paid.
- Video links: paid.
- Opening hours (incl. open now, special hours).
- Contact: phone, email, website.
- Trading locations / addresses (limited free).
- Social links.
- Location maps (Google Maps powered).
- Drag-and-drop page editor mentioned.
- Links to booking/ordering/website.

### Verification & Trust
- Self-published baseline.
- Optional: Owner photo-ID (Stripe), trading address proof, domain checked via ABIZ/DNS TXT or file.
- Clear status display (what has/hasn't been checked).

### Developer / Agentic Layer
- **MCP Server** (`https://mcp.to.co/mcp`, Streamable HTTP):
  - Public `identity` tools: resolve by address, search by name, by website hostname.
  - Authenticated `companies`: list/get/update own profiles (name fixed for registered).
  - Authenticated `locations`: list/update hours, phones, social, descriptions.
  - `help`: whoami, guide.
  - Resources: `toco://identity/{host}`, guide.
  - Auth: OAuth (my.to.co) or long-lived agent tokens (`toco_at_...`).
  - Rate limits, structured JSON, snake_case.
- ABIZ standard: open way to link own domain to the record via DNS for AI agents to verify/follow.
- llms.txt, server cards for discovery.

### Pricing Tiers
- Free: core page + address + 3 services/photos + 1 location.
- Starter (~£3/mo): 10 services, 12 photos, 2 videos, 3 locations.
- Higher (Pro/Grow): more capacity, team members, API credits.

### App (my.to.co)
- Sign-in to claim/edit business, publish, QR, security (agent tokens).

**Gaps in existing**: No deep CRM, no enquiry handling, no content generation, limited integrations, no payments/docs/B2B flows, no automated agent roles beyond basic updates.

## Business Pain Points (SMBs) That to.co Can Fix

| Pain Point | Current Reality for SMBs | How Current to.co Helps | Proposed Fix |
|------------|---------------------------|--------------------------|--------------|
| Scattered business details | Hours/services differ across Google, website, social, directories | Single source of truth + JSON/MD/MCP | Auto-publish to Google/Apple Maps, directories |
| Manual updates | Change hours → update 5 places | Edit once, page + formats update | Agents keep listings/maps/social in sync |
| Enquiry chaos | Forms, WhatsApp, email, phone scattered; no tracking | Contact buttons only | Enquiry manager + simple CRM + WhatsApp integration |
| No time for marketing | Hard to post consistently, maintain brand voice | Static page | AI social post generator/manager, brand voice, blog from RSS + publish |
| ICP / targeting | Guess ideal customers | Basic description | ICP generator from business data |
| Accounting / orders | Separate Xero/QuickBooks, manual invoices | None | Common MCP/API for accounting, order taking, B2B invoices/docs |
| Supplier / B2B | Email attachments, Tradeshift-like portals fragmented | None | Agentic supplier portal, B2B connecting, document exchange |
| Maps presence | Manual Google Business Profile | Maps widget on page | One-click / agent publish to Google Maps & Apple Maps |
| Trust / verification | Fake listings, hard to prove ownership | ABIZ + optional checks | Stronger agent-verifiable records |
| AI discoverability | Agents scrape websites unreliably | MCP + structured data | Agents can fully act (book, order, enquire) via expanded MCP |
| Payment security | Scattered processors | None | Secure payment details access for owners/agents |

## Full Opportunity in an Agentic World

Agents (Claude, GPT, custom, open-source) will:
1. Discover businesses via MCP/ABIZ instead of search.
2. Query facts, availability, pricing.
3. Initiate actions (enquiry, booking, order, document request).
4. Manage on behalf of owners (update hours, respond to enquiries, generate content, sync maps).

to.co becomes the **canonical agentic business record + action layer**.

### Suggested Feature Improvements & New Capabilities

#### 1. Owner App Enhancements (Business Owner Dashboard)
- Full listing management (already partial via MCP).
- **Enquiry Manager + Simple CRM**: Inbox for form/WhatsApp/email enquiries, status tracking, notes, follow-ups. Agent-assisted replies.
- **ICP Generator**: AI analyzes description, services, location → ideal customer profiles, messaging angles.
- **Social Media Post Generator / Manager**: Brand voice training, generate posts from services/hours/photos, schedule/publish to major platforms.
- **Brand Voice**: Persistent style guide for all generated content.
- Secure access to payment details (read-only or tokenized for agents).

#### 2. Integrations
- **WhatsApp**: Two-way enquiry/booking, agent responses.
- **Xero / Accounting**: Sync invoices, orders, contacts. Common MCP server that proxies accounting apps with business logic for order acceptance.
- **Google Maps + Apple Maps**: Automated data publishing / updates from to.co record (hours, photos, services, location).
- Blog: Connect existing website RSS → import posts; generate new posts; optionally publish back to website or to.co blog.

#### 3. B2B & Documents (Tradeshift-like)
- Agentic supplier portal: Suppliers discover, submit quotes/docs via MCP.
- Secure document exchange (invoices, contracts, specs).
- Order taking / acceptance flows with access control.
- B2B connecting: Verified businesses find each other via ABIZ/MCP.

#### 4. Agent Roles We Can Run on Behalf of Customers
- **Enquiry Agent**: Monitor channels, classify, draft/respond, escalate.
- **Content Agent**: Generate social posts, blog articles, ICP updates, brand-aligned copy.
- **Listing Sync Agent**: Keep Google/Apple Maps, directories, social bios in sync with record.
- **Order / Invoice Agent**: Accept orders, generate invoices, push to Xero, notify.
- **Supplier Discovery Agent**: Find and connect with verified suppliers.
- **Update Agent**: Proactive suggestions (hours changes based on calendar, photo refresh).
- **Verification Agent**: Guide through ID/address/domain checks.

#### 5. Platform / MCP Expansion
- Expanded MCP tools: enquiries CRUD, content generation triggers, map publish, accounting actions, document upload/access, order lifecycle.
- Own MCP server with pluggable app connectors behind business logic (orders, invoices, access control).
- Agent tokens with scoped permissions (e.g., enquiry-only, content-only).
- Webhooks / events for agent orchestration.

#### 6. Payments & Security
- Secure payment method storage (for customer or B2B).
- Tokenized access for agents.
- Audit logs for all agent actions.

## Implementation Priorities (Suggested)
1. **Quick wins**: Expand MCP for enquiries + basic CRM; WhatsApp integration; brand voice + social gen.
2. **Medium**: Maps publishing, Xero connector, blog/RSS, ICP generator.
3. **Strategic**: Full B2B portal, agent marketplace/roles, common accounting MCP, payment layer.

## Conclusion

to.co already has strong foundations for the agentic era (structured records, MCP, ABIZ, free access). Expanding into owner productivity tools, agent roles, integrations, and B2B flows addresses core SMB fragmentation pain while positioning to.co as the default interface for AI agents interacting with real businesses.

This document can serve as the basis for a product PR/roadmap issue in the main platform repo.

---
*Generated as analysis of public to.co features + proposed expansions. Repo crowers/toco-platform was not publicly accessible.*
