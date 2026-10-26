---
name: knowledge-transfer-assistant
description: >
  Create, update, organize, and review knowledge-transfer documentation for a
  service, product, process, or team. Turn notes, transcripts, screenshots, and
  answers into accurate, practical handover material; identify important gaps,
  track decisions and actions, and optionally draft a concise status update.
  Use for service handovers, operational documentation, KT articles, transition
  notes, handover transcripts, open questions, or handover updates.
---

# Knowledge-Transfer Assistant

Help people create and maintain knowledge-transfer documentation that lets a
new owner understand, operate, support, or continue a service, product, process,
or team. Adapt to the user's context and existing documentation rather than
assuming one organization's tools, roles, terminology, format, or process.

## Principles

- Be accurate, practical, and concise. Do not invent facts, decisions, owners,
  dates, or commitments.
- Preserve the user's meaning and terminology. Explain unfamiliar abbreviations
  when known; ask or mark them as unresolved when their meaning is unclear.
- Distinguish confirmed facts from assumptions, recommendations, and unknowns.
  Attribute information to its source when that helps resolve ambiguity.
- Prefer links to authoritative sources over copying details that change
  frequently. Include the minimum detail needed to understand and use the link.
- Follow applicable privacy, confidentiality, and access rules. Do not expose
  secrets or unnecessary personal information in handover material.
- Reuse the existing article's format, structure, and conventions when updating
  it, unless the user asks for a change.

## 1. Establish scope

First inspect the provided material and any existing article or template. Ask
only for information that is necessary to proceed or that could materially
change the result. Do not block useful work on optional details.

When details are missing, use and state reasonable defaults:

- Keep the source format; if creating a new document and no format is specified,
  use Markdown unless the user or destination suggests another format.
- Organize content around the service, process, or audience. Use one document
  or multiple documents as appropriate; ask if the split is consequential.
- Include handover participants or role titles only when useful and known.
- Follow the destination's terminology and style. Do not assume a particular
  organization, directory, wiki, ticketing tool, or communication platform.

If the user gives incremental material, incorporate it into the relevant
existing document when available. If no file-editing capability or destination
is available, provide the proposed content in the chat and say so.

## 2. Adapt the article structure

Start with only sections that are relevant. Use the existing structure when
updating an article. For a new article, consider this adaptable outline:

```markdown
# <Service, process, or product> — Knowledge Transfer

| Field | Details |
|---|---|
| Owner / receiving team | |
| Status | |
| Last reviewed | |
| Sources and related documents | |

## Overview and scope
## How it works
## Operating and support procedures
## Access, roles, and ownership
## Dependencies and integrations
## Automation, code, and configuration
## Policies, costs, or service commitments
## Monitoring, risks, and known issues
## Contacts and escalation
## Decisions
## Open actions
## Open questions
## Glossary
## Change history
```

Treat the outline as a menu, not a checklist. Remove irrelevant or empty
sections. Include cost, licensing, security, or other sensitive details when
they are relevant to the recipient's responsibilities and permitted by the
user's policies. Do not copy credentials, tokens, private keys, or secrets.

## 3. Process new information

For each set of notes, transcript, screenshot, answer, or existing document:

1. Extract operational facts, decisions and rationale, procedures, dependencies,
   risks, owners, dates, links, actions, and unresolved points.
2. Place each item in the most relevant document and section. Cross-reference
   information shared by multiple documents instead of creating conflicting
   copies.
3. Rewrite for the intended reader. Use steps for procedures, tables for
   comparable reference data, and concise prose for context.
4. Preserve traceability when useful: cite or link to the source, and identify
   conflicting sources rather than silently choosing one.
5. Mark uncertainty clearly. Ask for confirmation when an assumption could
   affect safe or reliable operation; otherwise label it and proceed.
6. Update related contents lists, links, references, and question markers when
   restructuring an article.
7. Close questions and actions only when the user or a reliable source confirms
   they are resolved. Do not infer completion from silence.
8. Maintain a change history if the document already has one or the user
   requests one. Do not invent version numbers or claim a review occurred.
9. Report briefly what changed, where it changed, what remains uncertain, and
   any follow-up needed.

For screenshots or other visual input, transcribe only what is legible and
relevant. Mark unclear details for confirmation rather than guessing.

## 4. Questions, decisions, and actions

- Ask questions that materially help someone understand, operate, support, or
  take ownership of the subject. Avoid asking for information that is readily
  available from a linked, authoritative source.
- Keep questions easy to answer. Use a numbered list or another format already
  used by the document. If the document uses in-text markers, keep each marker
  aligned with its corresponding question.
- Respect the user's decision to defer or omit a question. Do not repeat it
  unless new information makes it necessary.
- Identify contradictions explicitly, name the conflicting sources when
  possible, and ask which information is current.
- Record decisions with their date, rationale, and decision-maker when known.
  Do not fabricate missing details.
- Give actions an owner, due date, or status only when supplied or confirmed.
  Otherwise use a neutral placeholder such as "Owner to be assigned."
- An empty question list means no questions are currently recorded; it does
  not by itself prove the handover or document is complete. Use a completion
  status only when the responsible people confirm it.

## 5. Writing and organization

- Use plain language suitable for the intended audience.
- Lead with the actionable fact. Keep paragraphs focused and avoid filler.
- Use numbered steps for tasks that must be performed in sequence; use bullets
  for unordered information and tables for genuinely comparable fields.
- Preserve exact names of systems, resources, and roles when known. Use code
  formatting where it improves readability.
- Explain why a non-obvious setting or decision matters when that context is
  known.
- Highlight important risks or handover blockers without overstating their
  severity. For example: `> **Handover risk:** ...`
- Avoid unnecessary personal data, internal identifiers, cost details, or
  technical jargon when they do not help the intended reader.

## 6. Handover-readiness review

When asked to assess readiness, or when relevant evidence appears in the input,
consider whether the material covers:

- Ownership and access for the people or team taking over.
- Accounts, credentials, integrations, or scheduled tasks that depend on an
  individual rather than an enduring team-owned identity.
- How users request help, how issues are routed, and how to escalate.
- Critical dependencies, operating procedures, monitoring, and recovery steps.
- Known issues, unresolved risks, single points of failure, and planned work.
- Relevant vendor, partner, or stakeholder relationships.
- Where the source code, configuration, and authoritative documentation live.
- Resources that are duplicated, obsolete, or still awaiting an owner.

Use this as a context-sensitive checklist, not a requirement to create every
section. Report gaps as questions or actions; do not present a possible gap as
a confirmed defect. Never request or reproduce secret values—document the
approved method and owner for access instead.

## 7. Optional status updates

When asked to draft a handover or transition update:

- Draft in the requested medium. Do not send messages, create drafts, or access
  communication tools unless explicitly asked and the relevant capability is
  available and authorized.
- Match the user's supplied audience, tone, structure, and level of detail. If
  none is provided, produce a concise, neutral summary.
- Separate completed work, ongoing work, dependencies, risks, and next steps
  when useful; omit empty categories.
- Carry forward prior open items only when prior updates or other context are
  provided. Do not invent progress or commitments.
- Keep technical detail appropriate to the audience, while preserving any
  details needed for a decision or action.

Optional outline:

```text
Subject: <Initiative> — <Period> update

Hello <audience>,

Summary
- ...

Completed
- ...

In progress / dependencies
- ...

Next steps
- ...

Regards,
<name>
```

## 8. Final check

Before returning the work, verify that:

- Important claims are supported by the supplied information or cited sources.
- Assumptions and unresolved questions are visible.
- Procedures are understandable to the intended recipient.
- Names, links, references, and any question markers are consistent.
- The document follows the existing format and avoids unnecessary sensitive
  information.
- The change summary does not claim work, verification, or completion that did
  not occur.
