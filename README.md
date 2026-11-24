# Seayora for Cursor

Connects Cursor's agent to [Seayora](https://seayora.com), property-management software for US landlords, property-management companies, renters and the contractors who service their buildings.

Ask things like:

- "Which of my units are behind on rent, and by how much?"
- "What repairs are open across my buildings, and which have waited longest?"
- "When does the lease on unit 4B end, and what notice do I have to give?"
- "What sales tax do I charge on this job?"
- "Find me a one-bedroom in Clinton Hill under $3,000."

## What it installs

- **The Seayora MCP server**: `https://seayora.com/mcp` (remote, Streamable HTTP). Cursor signs you in with OAuth the first time a tool is used. Nothing runs on your machine and no API key is stored in this plugin.
- **A get-started skill** that finds out what kind of account is connected and suggests a first task.

## How it behaves

- **Scoped to you.** Every tool answers for the account that signed in: a tenant sees their own tenancy, a landlord their own buildings, a contractor their own jobs.
- **You choose the permissions.** The consent screen lists each permission; leave every "writes" permission unchecked for a strictly read-only connection.
- **Writes are proposals.** On most workspaces a change the agent makes is saved in Seayora's Approvals queue for you to approve, and the result says `staged: true` until you do. `create_listing` only ever saves a draft.
- **No tool moves money** or takes a payment.
- **No account needed to search homes.** Choose "Continue as a guest" on the sign-in screen for read-only access to public listings.

Every tool, its permission and whether it is a Read, a Write or a Sensitive write (it sends something another person receives) is listed in the generated [MCP server reference](https://seayora.com/docs/mcp-server-reference).

## Links

- Docs: https://seayora.com/docs/connect-claude-chatgpt-or-your-own-agent
- Privacy policy: https://seayora.com/privacy-policy
- Terms: https://seayora.com/terms-of-service
- Support: support@seayora.com

Available in the United States. Also listed in the official MCP Registry as `com.seayora/seayora`.

<!-- Source of truth: this folder lives in Seayora's main repository (cursor-plugin/).
     The skill text is copied from backend/scripts/gen_chatgpt_plugin.cjs (SKILL); change both together. -->
