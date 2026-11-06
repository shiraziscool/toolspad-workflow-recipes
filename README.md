# ToolsPad workspace workflow recipes

Practical MCP prompt templates for small service businesses, agencies and consultants. Use these recipes to review existing work, prepare a client handover and turn a clear next action into a task.

This documentation project is maintained for ToolsPad. It contains reusable prompts, not an MCP server implementation or a promise of results. The examples use no customer data. Tool availability depends on the connected workspace, permissions and application entitlements.

## Start with an agency inquiry audit

Use the [first-response worksheet](AGENCY-FIRST-RESPONSE-AUDIT.md) to review five recent inquiries, spot where replies stall, and assign backup coverage. You can use the worksheet with a spreadsheet or shared inbox.

## Connect one workspace

Use a client that supports remote MCP with Streamable HTTP and browser-based OAuth:

```text
Server name: ToolsPad
Transport: Streamable HTTP
URL: https://app.toolspad.com/mcp
Authorization: OAuth in your browser
```

1. Add the endpoint through your client's normal MCP connection interface.
2. Sign in to ToolsPad and select the workspace you intend to use.
3. Choose **read-only** for the first two recipes. The current connection flow defaults to read and write, so check the access mode before approving.
4. Ask the client to discover the available tools. Do not assume that an example's fields or operations exist in every connected workspace.

Review or revoke a connection in **Settings → AI connections**. Do not paste access tokens, passwords or a private workspace export into an issue on this repository.

## 1. Review overdue next actions

Use this when a small team needs to distinguish work that is late from work that is simply waiting. The output is a review list, not an automatic change to priorities.

```text
Use the connected ToolsPad workspace in read-only mode.

Review the tasks I am authorised to see. First establish the current date
and the time zone used for this review. Use available status and due-date
fields to find open tasks that appear overdue. Do not treat completed or
archived records as open work. If a field or status meaning is unavailable,
report that limitation rather than guessing.

Return a compact table with task, recorded owner, due date, current status
and the missing next-action detail, if any. Include source references that
the client actually provides; do not invent record URLs or identifiers.

Do not edit, assign, complete, move or delete any record. Finish with the
questions a team member would need to answer before changing the plan.
```

Check the list against the team's actual commitments. An overdue date alone does not explain whether a customer response, an internal decision or a revised deadline is needed.

## 2. Prepare a client handover brief

Choose the client or contact explicitly. A name match by itself is not enough when several records look similar.

```text
Use ToolsPad in read-only mode to prepare a handover brief for [client].
If the client identity is ambiguous, show the relevant matches and ask me
which record to use before continuing.

From authorised CRM context, notes and tasks that are clearly associated
with that client, summarise:
- what is currently open;
- the next action already recorded;
- its owner and due date, where available;
- what information or decision is missing;
- the source record for each statement.

Separate facts recorded in the workspace from your proposed questions.
Do not infer promises from a vague note, copy unrelated client information,
or expose unnecessary contact details. Do not send the brief, share a
document or change any record. Return the brief in this conversation.
```

This is useful before leave or a change of account owner. It does not replace the authoritative client record: the brief should point back to the relevant source rather than create a competing history.

## 3. Preview a follow-up task before creating it

Use this optional recipe only after deliberately granting read-and-write access. Keep a clear boundary between a proposed task and a saved task.

```text
Prepare one follow-up task for [confirmed client/contact] based on this
instruction: [specific action, intended owner and due date/time zone].

Check the available task tools and identify the target list and owner from
real workspace records. If any required detail is ambiguous, ask me.
Check for an existing task with the same purpose before proposing a new one.

Show the proposed title, list, owner, due date and description first.
Do not create it until I approve those exact details. After approval,
create it once, then read it back and report its actual saved identifier
and fields. If the write result is uncertain, reconcile the existing
records before considering another attempt.

Do not send a client message, create an appointment or change other records.
```

For a first trial, use a clearly labelled test task in an appropriate workspace. Confirm its saved details before using the same process for live commitments.

## Adapt the recipes

- Replace bracketed inputs with precise instructions; do not leave them for the agent to invent.
- Start with one workflow and the smallest useful record set.
- Keep unsupported fields visible as unknown, rather than filling them with plausible values.
- Keep customer information inside the authorised workflow; use synthetic examples when discussing improvements publicly.

## Sources and product background

The endpoint, transport, workspace selection, access modes and connection-management instructions were checked against the official ToolsPad MCP page on 4 November 2026. Client interfaces and available operations can change.

- [Official ToolsPad MCP connection guide](https://toolspad.com/mcp?utm_source=github&utm_medium=referral&utm_campaign=aidm&utm_id=aidm_organic_v1&utm_content=github_workflow_recipes_readme_001)
- [ToolsPad Tasks](https://toolspad.com/tasks?utm_source=github&utm_medium=referral&utm_campaign=aidm&utm_id=aidm_organic_v1&utm_content=github_workflow_recipes_readme_001)

ToolsPad brings critical business apps into connected workspaces. These recipes focus on a few practical jobs; they do not require changing every part of a team's process at once.
