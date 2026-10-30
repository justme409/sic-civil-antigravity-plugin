# Civil (SI Civil) for Antigravity

Civil connects Antigravity to SI Civil (Super Intelligence Civil), the AI system for civil engineering and civil construction. SI Civil prices the tender, writes the management plans, inspection and test plans (ITPs) and SWMS, builds the programme, manages quality, procurement, the weekly look-ahead and material quantities, and runs delivery through to the claims. With Civil, you ask Antigravity about all of it for the projects you are appointed to, within your role, and draft comments for the team.

Civil is made by Applied Ontologies, Queensland, Australia. Website: https://sicivil.com/

## What is in this plugin

- **The Civil MCP server** (`mcp_config.json`): one remote MCP server, `https://mcp.sicivil.com/mcp`, over Streamable HTTP, with OAuth sign-in (dynamic client registration and PKCE). It runs on SI Civil's servers.
- **The get-started skill** (`skills/get-started/SKILL.md`): how to sign in, what each tool answers, first questions to try, and how the agent should answer from the tools.
- **A short rule** (`rules/AGENTS.md`): which tool answers which question.

## Install

From the Antigravity Marketplace, search for Civil and choose Install. From a copy of this repository:

```
agy plugin install ./sic-civil-antigravity-plugin
```

## Sign in

You need an SI Civil login, issued by Applied Ontologies or by your company's director. Email tom@sicivil.com for one.

1. Install the plugin. In the Antigravity App or IDE, open Agent settings, go to the Customizations tab and choose **Authenticate** next to the Civil server.
2. Your browser opens the SI Civil sign-in page at `auth.sicivil.com`, which names the application asking for access. Enter your email and password and choose **Sign in and allow**, then paste the code shown back into Antigravity.
3. Directors, project managers and Superintendents also type a 6-digit code from an authenticator app. The first sign-in shows the QR code to set it up.

## Tools

| Tool | What it answers | Reads or writes |
|---|---|---|
| `my_projects` | Your projects and your role on each | Reads |
| `project_status` | Stage, tender, programme dates, milestones, open items | Reads |
| `whats_waiting` | Gates waiting on the owner, requests, open findings, your draft comments | Reads |
| `search_project` | Every record on the project that matches a phrase | Reads |
| `find_documents` | The project documents with revision and status | Reads |
| `read_document` | One document in full, in parts for long ones | Reads |
| `hold_witness_schedule` | Hold and witness points per ITP, who releases each, the notice | Reads |
| `lot_status` | Lots by status and work type, or the matching lots | Reads |
| `programme_position` | The programme on any date: in progress, starting soon, milestones | Reads |
| `list_risks` | The risk register and its controls | Reads |
| `add_comment` | Drafts a comment on a document, lot or ITP item under your name | Writes a draft held by SI Civil; the project itself is unchanged |

What you see follows your role on each project. Commercial information, such as the estimate and the bid price, is shown only to the roles that hold it. Approving a hold point, lodging a tender and any change to the project stay with the people who own them in SI Civil.

## Example prompts

- "How is the Jervois Street project going?"
- "What hold points apply to the raised platform ramps?"
- "Where will the programme be on 10 May 2027, and what hold points come up for that work?"
- "Show the method steps and safety controls for the kerb and channel works."
- "Draft a comment on ITP item K08-08: check the cover to the mesh on the pour day."

## Data and privacy

The plugin sends your requests to SI Civil at `mcp.sicivil.com`, with the access token from your sign-in at `auth.sicivil.com`. SI Civil reads the project records you are allowed to see and returns plain-text answers to Antigravity. It records each sign-in and each tool call (the tool, its arguments and the result) for 12 months for audit and support. The servers are in Sydney, Australia (Oracle Cloud Infrastructure), behind Cloudflare, with encrypted backups held by Hetzner in the European Union. Your project records are never used to train AI models.

- Privacy policy: https://sicivil.com/privacy
- Terms: https://sicivil.com/terms
- Support: https://sicivil.com/support, or email tom@sicivil.com. We aim to reply within two business days, Brisbane time.

## Disconnect

Uninstall the plugin with `agy plugin uninstall sic-civil`, or disable it in the Customizations panel. To sign your login out of every application at once, email tom@sicivil.com.
