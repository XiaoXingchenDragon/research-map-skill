# Archive Workflow

Use this workflow when the user provides or updates a Deep Research report in `00_inbox/`.

## 1. Inspect Sources

1. List candidate files in `00_inbox/`.
2. Identify the newest or user-named report.
3. Confirm the report is the intended source when there are multiple similar reports.
4. Read existing `dashboard.md`, PI map, people, directions, and paper structure before editing.

## 2. Extract Without Over-expanding

Move only useful cleaned information into formal files:

- PI identity, aliases, institution, lab, identifiers
- research directions
- current RPGs / students and graduated RPGs when evidence exists
- coauthors and collaborators with evidence levels
- representative papers
- funding / projects
- timeline facts
- uncertainty list

Do not create many low-priority people files in early rounds unless the user asks.

## 3. Update Formal Files

Suggested order:

1. PI file
2. people files
3. direction files
4. paper files
5. core/other link files
6. PI-specific map
7. timeline and dashboard
8. next Deep Research prompt

Respect local graph rules for links.

## 4. Evidence and Status

Use:

- `status: verified` only when evidence is strong and source-backed
- `status: unverified` for uncertain, inferred, or weakly sourced information
- clear notes for source type: official, publisher, DOI, research portal, database, AI report, or interpretation

Do not turn report interpretation into fact.

## 5. Clean Raw Reports

After extracting information, remove Obsidian `[[...]]` links from the raw report so the inbox does not pollute the graph.

The raw report may keep ordinary text, URLs, citations, and headings. Only remove graph-forming wiki links unless the user asks for stronger cleanup.

## 6. Finish With Gaps

Report what was updated and list remaining gaps. When appropriate, update a next Deep Research prompt with:

- missing people details
- weak direction evidence
- missing first-author papers
- paper-count target
- core/other selection needs
- tags needed for archiving
