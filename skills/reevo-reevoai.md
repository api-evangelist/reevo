---
name: Reevoai
description: Use when building CRM workflows, automating sales outreach, configuring data integrations, managing contacts and opportunities, creating automated sequences, setting up meeting intelligence, or building custom workflows. Reach for this skill when users need to manage their sales pipeline, automate prospecting, integrate external tools, or configure CRM data structures.
metadata:
    mintlify-proj: reevoai
    version: "1.0"
---

# Reevo AI Skill Reference

## Product Summary

Reevo is an AI-driven sales CRM platform that combines contact and opportunity management with automated outreach, meeting intelligence, and workflow automation. Agents use Reevo to help users manage pipelines, create multi-channel sequences, integrate external tools via APIs, configure custom CRM fields, and automate business processes without code.

**Key entry points:**
- **Workflows**: `https://app.reevo.ai/workflows` — build automation without code
- **Sequences**: `https://app.reevo.ai/connect?tab=sequences` — create multi-channel outreach campaigns
- **Settings**: `https://app.reevo.ai/settings` — configure CRM, integrations, API keys, custom fields
- **API**: Reevo REST API at `https://api.reevo.ai/api/v1/public/` with permission-based keys
- **Ask Reevo**: Built-in AI copilot accessible via Cmd+I (Mac) or Ctrl+I (Windows)

**Primary documentation**: https://help.reevo.ai

---

## When to Use

Reach for this skill when:

- **Building workflows**: User needs to automate tasks when records change, meetings occur, or webhooks fire
- **Creating sequences**: User wants to set up multi-channel outreach (email, calls, LinkedIn) with A/B testing
- **Configuring CRM**: User needs to add custom fields, set up stages, create relationships, or manage data structure
- **Integrating external tools**: User wants to push/pull data from Clay, Zapier, Make, or custom APIs
- **Managing data**: User needs to import CSV, export records, or sync data between systems
- **Setting up meetings**: User wants to enable recording, notetaker bot, or meeting intelligence
- **Troubleshooting**: User's workflow isn't firing, sequence isn't sending, or integration isn't working

---

## Quick Reference

### Workflow Triggers

| Trigger Type | Examples | Use Case |
|---|---|---|
| **Record-based** | Account Created, Contact Updated, Opportunity Created | Automate when CRM data changes |
| **Meetings** | Meeting Created, Time Before Meeting Start, Meeting Ended | Meeting prep, follow-ups, reminders |
| **Schedule** | Recurring Schedule | Time-based automations (daily, weekly) |
| **Webhook** | Webhook Received | External systems trigger workflows |
| **Custom objects** | Custom Object Created, Custom Object Updated | Automate custom data |

### Workflow Action Nodes

| Category | Examples |
|---|---|
| **CRM** | Create/Update/Search Account, Contact, Opportunity; Move Stage |
| **Sequences** | Enroll Contact, Unenroll Contact |
| **Communication** | Send Slack Channel Message, Send Slack DM |
| **Logic** | Condition, Compute, Delay, User Round Robin |
| **Integrations** | Webhook (outbound) |

### Custom Field Types

| Type | Use For | Can Be Unique? |
|---|---|---|
| Text (single line) | Short text, codes | ✓ |
| Text (multi-line) | Longer notes | ✓ |
| URL | Links | ✓ |
| Number | Scores, counts | ✓ |
| Date | Dates | ✗ |
| Single-select | Dropdown choices | ✗ |
| Multi-select | Multiple choices | ✗ |
| Boolean/Checkbox | True/False | ✗ |
| Amount/Currency | Money values | ✓ |

### API Permissions

| Resource | Read | Write |
|---|---|---|
| Accounts | ✓ | ✓ |
| Contacts | ✓ | ✓ |
| Opportunities | ✓ | ✓ |
| Tasks | ✓ | ✓ |
| Activities | ✗ | ✓ |
| Users | ✓ | ✗ |
| Mailbox | ✓ | ✗ |
| Sequence Enrollment | ✓ | ✓ |

---

## Decision Guidance

### When to Use Workflows vs. Sequences

| Need | Use Workflows | Use Sequences |
|---|---|---|
| Automate multi-step outreach (email → wait → call) | ✗ | ✓ |
| Trigger action when record changes | ✓ | ✗ |
| A/B test messaging | ✗ | ✓ |
| Send Slack notification on deal stage change | ✓ | ✗ |
| Enroll contacts in automated campaigns | ✗ | ✓ |
| Move opportunity to next stage automatically | ✓ | ✗ |

### When to Use API vs. Workflow Webhooks

| Scenario | Use API | Use Webhook |
|---|---|---|
| External tool pushes data to Reevo | ✓ | ✗ |
| Reevo triggers external system | ✗ | ✓ |
| One-time data sync from Clay/Zapier | ✓ | ✗ |
| Real-time bidirectional sync | ✓ | ✓ |
| Bulk contact/account creation | ✓ | ✗ |

### Record Auto-Creation Modes

| Mode | Creates Records For | Best For |
|---|---|---|
| **Capture All** | Every email/meeting contact | Maximum visibility |
| **Existing Accounts** | Only people at known accounts | Controlled data |
| **Outbound Only** | Your initiated emails/meetings | Avoiding inbound noise |
| **Do Not Capture** | Manual entry only | Full manual control |

---

## Workflow

### Creating a Workflow

1. **Navigate** to `https://app.reevo.ai/workflows` and click **New Workflow**
2. **Choose template or start blank** — templates organize by use case (Contact-Based, Account-Based, Lead Routing, Alerts)
3. **Configure trigger** — click trigger node, select type (Account Created, Contact Updated, etc.), add filter conditions if needed
4. **Add action nodes** — click **+** to add steps; configure each node's inputs using static values or variables from earlier steps
5. **Use variables** — click any field to switch to variable mode and reference data from trigger or previous nodes
6. **Test with dry run** — click **Dry run**, select a record, run simulation to see projected behavior without side effects
7. **Deploy** — click **Deploy** when Deploy Checklist shows all items complete
8. **Activate** — toggle **Active** to turn the workflow on; it fires automatically when trigger conditions match

### Creating a Sequence

1. **Navigate** to `https://app.reevo.ai/connect?tab=sequences` and click **New Sequence**
2. **Choose creation method** — start from scratch, use blueprint, or clone existing
3. **Name sequence** — use clear, descriptive title (e.g., "Tech Founders Cold Outreach")
4. **Add steps in order** — automated emails, manual tasks (calls, LinkedIn), wait periods
5. **Configure variants** — set up A/B test variants for different messaging
6. **Set sending schedule** — define business hours for email sends
7. **Launch sequence** — click **Launch** to activate (does not enroll contacts yet)
8. **Enroll contacts** — click **Add contact**, choose source (list, CRM, prospecting, Chrome extension)
9. **Select mailbox strategy** — use CRM owner's mailbox or specific mailboxes; set fallback mailbox
10. **Monitor** — track enrollment status, open rates, replies in Performance tab

### Configuring Custom Fields

1. **Navigate** to Settings → CRM object (Accounts, Contacts, Opportunities)
2. **Click Add Field** under Custom Fields
3. **Enter name and description** — use clear labels
4. **Choose field type** — select from 10 types (text, number, date, select, checkbox, currency, etc.)
5. **Set options** (for select fields) — add predefined choices
6. **Enable unique** (optional) — prevent duplicate values across records
7. **Pin field** (optional) — show on primary details page
8. **Save** — field appears immediately on all records

### Setting Up API Integration

1. **Create API key** — Settings → Integrations → API Keys → New API key
2. **Name the key** — use descriptive name (e.g., "Clay Integration")
3. **Select permissions** — choose read/write for resources needed (Accounts, Contacts, Opportunities, etc.)
4. **Generate and copy** — store securely; cannot be retrieved again
5. **Configure external tool** — add header `x-api-key: [your-key]` to requests
6. **Set endpoint** — use `https://api.reevo.ai/api/v1/public/[resource]`
7. **Test request** — send sample payload to verify permissions and data mapping
8. **Monitor** — check API key status in Settings; expire old keys when no longer needed

---

## Common Gotchas

- **Workflow not firing**: Confirm workflow is **Deployed** (not just saved) AND **Active** toggle is on. Verify trigger conditions match actual events (e.g., specific field must change, not just record viewed).

- **Sequence emails not sending**: Check mailbox is connected and healthy in Settings. Verify contacts are enrolled AND sending method + fallback mailbox were configured during enrollment. Confirm sending schedule allows emails at current time.

- **API key lost**: API keys shown only once at creation. If lost, expire old key and generate new one. No retrieval possible.

- **Custom field type change**: Changing field types after data exists may cause data loss. Plan field types carefully before use; contact support if modification needed.

- **Workflow variables not available**: Variables only reference data from trigger and earlier nodes. Cannot reference data from later nodes. Use Compute node to transform data if needed.

- **Sequence contact enrollment fails**: Check contact has required fields (email for email steps, phone for calls, LinkedIn URL for LinkedIn steps). Configure fallback rules in sequence Settings for missing fields.

- **Webhook trigger not firing**: Verify external system sends POST request to correct webhook URL with JSON body matching configured payload structure. Check API key authentication if required.

- **Duplicate prevention**: Contacts cannot enroll in multiple sequences simultaneously. Must unenroll from one before adding to another.

- **Reply detection**: When TO recipient replies to sequence email, they auto-exit. CC'd recipients replying do NOT exit sequence.

- **Rollup fields locked**: Data source object type cannot change after rollup created. Delete and recreate if source needs to change.

---

## Verification Checklist

Before submitting workflow or integration work:

- [ ] **Workflows**: Deployed ✓, Active toggle on ✓, trigger conditions tested ✓, dry run shows expected behavior ✓, all nodes connected ✓
- [ ] **Sequences**: Launched ✓, contacts enrolled ✓, mailbox strategy selected ✓, fallback mailbox set ✓, sending schedule configured ✓
- [ ] **API integrations**: Key has required permissions ✓, endpoint URL correct ✓, request headers include `x-api-key` ✓, test request succeeds ✓, payload structure matches documentation ✓
- [ ] **Custom fields**: Field type chosen carefully ✓, unique constraint set if needed ✓, field appears on records ✓, data imports map field correctly ✓
- [ ] **Data imports**: CSV headers match field names ✓, custom fields mapped ✓, approval lock reviewed (new accounts) ✓, sample rows validated ✓
- [ ] **Integrations**: External tool configured with correct endpoint ✓, authentication headers set ✓, payload structure matches Reevo expectations ✓, test data flows correctly ✓

---

## Resources

**Comprehensive page navigation**: https://help.reevo.ai/llms.txt

**Critical documentation pages**:
- [Workflow Builder](https://help.reevo.ai/Automations-and-Workflows/Workflow-Builder) — complete guide to building and deploying workflows
- [API Integrations with Other Tools](https://help.reevo.ai/Data-management-and-migration/Integrations-With-Other-Tools) — API endpoints, permissions, examples
- [Sequences: Create Automated Multi-Channel Campaigns](https://help.reevo.ai/Prospecting-and-Outreach/Sequences-Create) — sequence setup, enrollment, mailbox strategy

---

> For additional documentation and navigation, see: https://help.reevo.ai/llms.txt