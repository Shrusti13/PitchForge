# Sample Brief — ResolveIQ

Paste this brief into Copilot Cowork to generate the one-pager website.
The generated result is included alongside this file as
[`ResolveIQ-OnePager.html`](./ResolveIQ-OnePager.html).

---

**Prompt to use in Cowork:**

> Use these two skills `/presales-brandkit` and `/presales-one-pager` and help
> me create a one-pager for this. Create a pre-sales one-pager for ResolveIQ —
> an AI-Powered IT Support Agent we built for Contoso Technologies.
> Anonymise the client name.

**Brief:**

- **Client:** Contoso Technologies
- **Anonymise:** Yes
- **Industry:** Enterprise SaaS & Cloud Infrastructure
- **Use Case:** AI-Powered IT Helpdesk & Ticket Automation

**Solution Overview:**
ResolveIQ is a fully low-code Copilot Studio agent that serves as the first
point of contact for all internal IT support requests. Employees describe their
issue in natural language through Teams — ResolveIQ either resolves it instantly
using ServiceNow's knowledge base or creates a prioritised ticket and assigns it
to the right support operations team automatically.

**Current Challenges:**
1. Portal fatigue — employees avoided the complex ServiceNow portal, flooding
   the helpdesk with unstructured emails and Teams messages.
2. Slow ticket creation — staff spent 40% of their time manually logging,
   categorising, and assigning tickets.
3. Knowledge base underutilisation — 2,000+ KB articles sat unused.
4. Inconsistent prioritisation — subjective priority levels delayed critical issues.
5. No after-hours support — 9-to-6 coverage left other time zones unsupported.

**Architecture & Tech Stack:**
- Microsoft Copilot Studio (low-code agent builder)
- ServiceNow Connector (ticket create / update / assign / status)
- ServiceNow Knowledge Base integration (self-service resolution)
- Power Automate (routing, priority rules, SLA escalation)
- Microsoft Teams (primary interface)
- Adaptive Cards (confirmations, status, KB display)
- Dataverse (conversation history, ticket metadata, analytics)

**Business Value:**
- 55% of issues resolved at first contact via KB self-service
- 80% reduction in manual ticket logging time
- 3x faster ticket assignment (45 min → under 15 min)
- 100% consistent priority assignment
- 24/7 self-service availability

**Business Outcomes:**
Within 8 weeks: 40% lower average resolution time and a 60% drop in
"how do I…" tickets. Now expanding to HR and Facilities support.

**Contributors:**
- Shrushti Shah — Senior Consultant & Solution Architect
- Aarav Mehta — Power Platform Developer
- Priya Kulkarni — ServiceNow Integration Specialist
- Rohan Deshmukh — IT Operations Lead (Client Side)

**Timeline:** 8-week delivery (February – March 2026)
