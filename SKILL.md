---
name: research-map
description: Build and maintain reusable Markdown/Obsidian research-group maps for different PIs. Use when archiving Deep Research reports, updating PI-centered people/direction/paper graphs, cleaning inbox reports, selecting core papers, or generating staged Deep Research prompts for a lab or research group.
---

# Research Map

## Purpose

Maintain a reusable Markdown knowledge base for understanding research groups centered on a PI. Treat each PI as a project instance with people, research directions, papers, maps, timelines, funding, and uncertainty tracking.

This skill is for graph curation and research-group intelligence, not ordinary paper summarization.

## First Steps

1. Read local project instructions first: `AGENTS.md`, `dashboard.md`, and any project skill or README the user names.
2. If the task imports a new report, inspect `00_inbox/` and identify the latest relevant report before editing formal files.
3. If the task concerns prompt generation, inspect current people, directions, papers, maps, and latest inbox notes before writing the prompt.
4. Prefer local project rules over this generic skill when they conflict.

## Core Workflow

### Archive a Report

1. Read the report from `00_inbox/`.
2. Extract verified facts into formal folders.
3. Mark uncertain information with `status: unverified`.
4. Keep interpretation separate from facts.
5. Remove Obsidian `[[...]]` links from the raw inbox report after importing useful information.
6. Update the next Deep Research prompt with remaining gaps.

Use `references/archive_workflow.md` for detailed import and cleanup rules.

### Maintain the Graph

Use a PI-specific map file as the human entry point, but keep graph edges layered:

1. PI map links to people only.
2. People files link to research directions.
3. People files link to papers only when the person is confirmed or strongly indicated as first author.
4. Direction files link to per-direction `core.md` and `other.md` link files.
5. Link files link to paper files.
6. Paper files do not link directly back to directions.

Use `references/graph_rules.md` before changing links or moving papers.

### Add People

Separate people by role when the local project uses role folders:

- `pi/`
- `rpg/current/` for current RPGs / students when current/graduated status is known
- `rpg/graduated/` for completed / graduated RPGs when current/graduated status is known
- `rpg/` only as a temporary holding folder when status has not yet been classified
- `coauthors/` for collaborators and coauthors

Do not invent advisor-student relationships. Do not upgrade one-time coauthorship into strong collaboration.

### Add Directions

Create one file per important direction. Each direction should include:

- concise summary
- people in this direction
- links to its `core` and `other` paper link files
- funding / projects when available
- interpretation
- uncertainty / to verify

Funding information belongs in direction files or templates unless the local project says otherwise.

### Add Papers

Use a two-layer paper structure when the project supports core/other classification:

- `03_papers/core/paper/`
- `03_papers/other/paper/`
- `03_papers/core/link/<Direction_Name>/core.md`
- `03_papers/other/link/<Direction_Name>/other.md`

Core papers should normally be limited to 1-2 per direction and selected for representativeness, venue quality, citation impact, or clear route-defining value. Other papers expand coverage without overloading direction cards.

Use `references/graph_rules.md` for exact link behavior.

### Generate Deep Research Prompts

Use staged prompts instead of asking for one giant report:

1. Round 1: PI identity, main directions, people, representative papers, timeline, uncertainties.
2. Round 2: verify directions and people, select core papers, correct weak links, reach about 5-10 papers.
3. Round 3: expand recent literature to about 20-40 papers, cover RPG first-author papers, add tags for archiving.

Use `references/deep_research_workflow.md` when writing the prompt.

## Required Judgment

- Prefer official university, faculty, lab, publisher, DOI, ORCID, Google Scholar, Semantic Scholar, OpenAlex, Crossref, and research portal sources.
- Do not write speculation as fact.
- Use `status: unverified` for uncertain claims.
- Preserve aliases, but use normalized official node names for formal files.
- Keep the graph small early; expand after directions and people stabilize.
- Do not create personal background matching or application-fit analysis unless explicitly requested.

## Resources

- `references/graph_rules.md`: Obsidian graph, folder, and link structure.
- `references/archive_workflow.md`: How to import inbox reports and clean raw reports.
- `references/deep_research_workflow.md`: How to generate staged Deep Research prompts.
- `assets/templates/`: Reusable person, direction, paper, and link templates.
