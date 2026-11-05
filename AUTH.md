# ToolsPad workspace authentication

ToolsPad uses browser-based OAuth for its hosted MCP connection. This is a public setup guide, not a credential file or an MCP server implementation.

## Connect one intended workspace

1. Use an MCP client that supports remote Streamable HTTP and browser-based OAuth.
2. Add `https://app.toolspad.com/mcp` through the client’s normal MCP connection interface.
3. Complete the ToolsPad sign-in and select the intended workspace in the browser flow. The account must have the required workspace membership and permissions.
4. Check the access mode before approving. The documented flow defaults to read and write; choose read-only for reviews and handover summaries. Grant write access only when needed for the user’s requested workflow.
5. Let the client finish its normal connection flow, then discover the actual tools and schemas. Application entitlements and granted access determine what is available.

The initial browser authorisation requires the workspace user. This guide does not provide unattended account creation, a shared service account, a reusable public token or a way around consent. Do not invent client-specific configuration or OAuth registration details when the official guide does not provide them.

## Review and revoke access

In ToolsPad, use **Settings → AI connections** to review or revoke a connection. If access is missing, expired or revoked, use the normal client connection flow. Do not change workspace permissions or silently expand access to make a workflow succeed.

Never put passwords, access tokens, client secrets, callback URLs containing codes, workspace exports or private business records in repository files, issues or public examples. Do not ask a user to paste them here.

[Official ToolsPad MCP setup guide](https://toolspad.com/mcp?utm_source=github&utm_medium=referral&utm_campaign=aidm&utm_id=aidm_organic_v1&utm_content=github_workflow_auth_001)

Connection behaviour above follows public ToolsPad documentation checked on 4 November 2026. Recheck the official guide when behaviour differs. No client-specific runtime test, private-workspace test, plan entitlement or successful connection is claimed by this document.
