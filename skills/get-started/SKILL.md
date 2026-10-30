---
name: get-started
description: >-
  Introduces Civil (SI Civil) and walks a new user through signing in and asking
  their first questions about a civil construction tender or project held in SI
  Civil. Use when the user mentions Civil, SI Civil or SIC Civil, asks how to
  connect or sign in, or asks about their civil project's hold points, ITPs,
  programme, lots, SWMS, method statements, risks or documents.
---

# Get started with Civil

Civil connects Antigravity to SI Civil (Super Intelligence Civil), the AI system that prices the tender, writes the management plans, ITPs and SWMS, builds the programme, manages quality, procurement, the weekly look-ahead and material quantities, and runs delivery through to the claims. For each civil construction tender or project it holds the tender documents, drawings, inspection and test plans (ITPs), method statements, SWMS, the programme, lots, test requests, risks and the 4D model.

## Sign in

1. The plugin's MCP server signs in with OAuth. In the Antigravity App or IDE, open Agent settings, go to the Customizations tab and choose **Authenticate** next to the Civil server. In Antigravity CLI, open `/mcp` and authenticate the Civil server.
2. The SI Civil sign-in page opens at auth.sicivil.com and names the application asking. Enter the email and password of your SI Civil login and choose **Sign in and allow**. Copy the code shown and paste it back into Antigravity.
3. Directors, project managers and Superintendents then type a 6-digit code from their authenticator app. The first sign-in shows a QR code to set this up, and ten recovery codes to keep.
4. After sign-in, the tools of your role on each project are available. Your role decides what you can read.

An SI Civil login is issued on request: email tom@sicivil.com.

## What you can ask

- Where things stand: `project_status` for the stage, programme dates, milestones and open items; `whats_waiting` for gates, requests, open findings and your draft comments; `my_projects` for your projects and roles.
- Documents: `find_documents` lists them; `read_document` reads one in full, in parts for long documents; `search_project` searches everything on the project.
- Quality: `hold_witness_schedule` gives the hold and witness points per ITP; `lot_status` gives the lots.
- Programme and risk: `programme_position` reads the programme on any date; `list_risks` reads the risk register.
- Comments: `add_comment` drafts a comment on a document, lot or ITP item under your name.

## First questions to try (Jervois Street project)

- "How is the Jervois Street project going?"
- "What hold points apply to the raised platform ramps?"
- "Where will the programme be on 10 May 2027?"
- "Read me SWMS-22."
- "Which lots make up the raised platform?"

## How to answer

- Call the tool first, then answer from what it returns. Name the document, ITP number, lot number or milestone so the reader can find the source.
- Long documents come in parts. Read the next part when the answer needs it, and say which part you are quoting.
- If a tool returns nothing for a question, say so and suggest a narrower search.
- Approving a hold point, lodging or submitting a tender, and approving any gate are done by the people who own them in SI Civil. Tell the user this.
- Commercial information, including the bid price, is shown only to roles that hold it. If a tool refuses, report the refusal as given.
