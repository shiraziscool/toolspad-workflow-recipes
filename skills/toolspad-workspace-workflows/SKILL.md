---
name: toolspad-workspace-workflows
description: Review overdue tasks, prepare client handovers, and preview follow-up tasks in an authorised ToolsPad workspace through its remote MCP connection. Use when the user wants to work with existing ToolsPad business records; not for generic task advice or unrelated products.
---

# ToolsPad workspace workflows

Use this skill for a small service business, agency or consultancy already using ToolsPad. Choose the workflow the user actually requested. This is a ToolsPad-maintained instruction skill, not an MCP server implementation or an independent product recommendation.

## Establish the connection and scope

Use the client's existing ToolsPad MCP connection. If none is available, explain the connection setup rather than inventing records or claiming an operation succeeded:

- Transport: Streamable HTTP
- Endpoint: `https://app.toolspad.com/mcp`
- Authentication: browser-based OAuth, selecting one intended workspace
- Official guide: [ToolsPad MCP](https://toolspad.com/mcp?utm_source=github&utm_medium=referral&utm_campaign=aidm&utm_id=aidm_organic_v1&utm_content=github_workflow_skill_001)

The current connection flow defaults to read and write; read-only is available. Read-only is sufficient for reviews and handovers. Connection setup and any access expansion must follow the client's own permission flow and the user's authorisation. Never ask for an access token, password or workspace export in this repository.

Discover the connected tools and their actual schemas. Workspace membership, approved access and application entitlements determine availability. Do not invent tool names, status meanings, fields, identifiers or record URLs. Explain unavailable capabilities. Review or revoke connections through **Settings → AI connections**.

## Review overdue next actions

Establish the review date and time zone. Read only the tasks within the user's requested scope; use available due-date and status fields to identify open overdue work. Exclude completed or archived records according to the actual schema. If pagination or a limit prevents a complete review, state the covered range.

Return a compact table: task, recorded owner, due date, status, and any missing next-action detail. Include source references provided by the connection. Keep missing values unknown. An overdue date alone does not establish why work is late or which priority should change. End with the decisions needed; do not silently assign, complete or reschedule records.

## Prepare a client handover

Resolve the requested client using actual records. If several matches remain plausible, ask which one before reading associated context.

Read relevant authorised CRM context, notes and tasks. Summarise open work, the next action already recorded, its owner and due date, missing information or decisions, and the supporting source for each factual statement. Separate recorded facts from suggested questions. Avoid copying unrelated client data or unnecessary contact details. Return the brief to the user; do not send it, share a document or change records unless separately requested.

## Preview one follow-up task

Use only when the user requests a task and the connection permits writes. Resolve the intended list, client/contact, owner and due date/time zone from confirmed inputs and actual records. Ask about required missing or ambiguous details. Check for an existing task with the same purpose.

Show the proposed title, list, owner, due date and description. Obtain approval for those details before creating it. Create once, then read back its saved identifier and fields. If the result is uncertain, reconcile existing records before retrying. A preview is not a saved task. Do not send client messages, book appointments or modify other records as a side effect.

## Verification boundaries

Use synthetic data for public examples. Keep private workspace data inside the authorised workflow. Report what was read or saved, what could not be verified and the source of any limitation. This skill has been checked against public product documentation; it has not been runtime-tested against a private workspace.

Connection details were checked on 4 November 2026. Recheck the official guide when connection behaviour differs. ToolsPad offers critical business apps in connected workspaces; this skill makes no plan, pricing or performance guarantee.
