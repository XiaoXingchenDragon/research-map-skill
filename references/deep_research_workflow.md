# Deep Research Workflow

Generate staged Deep Research prompts based on the maturity of the local map.

## Dashboard

| Round | Goal | Timing | Output | Paper Target |
|---|---|---|---|---|
| 1 | First usable group map | New PI / new lab | PI identity, directions, people, representative papers, timeline, uncertainty | 3-5 papers |
| 2 | Verify and stabilize | After manual cleanup | corrected directions, checked people, core paper selection | 5-10 total papers |
| 3 | Expand literature | After map is stable | recent paper expansion, RPG first-author coverage, tags | 20-40 total papers |

## Round 1 Prompt Goals

Ask for:

- official PI identity, aliases, institution, department, email, ORCID, Google Scholar, lab name
- main research directions
- major coauthors and collaborators
- current and recent RPGs / students if available
- representative papers
- recent research trends
- basic timeline
- uncertainty / to verify

Constrain the answer:

- prefer official and publisher sources
- do not infer advisor-student relationships without evidence
- do not treat one-time coauthorship as strong collaboration
- mark uncertainty explicitly
- avoid personal background matching

## Round 2 Prompt Goals

Ask for:

- re-check and correct research directions
- decide whether directions should merge, split, or remain separate
- select 1-2 core papers per direction
- add supporting papers only where useful
- audit coauthor and RPG identities, current affiliations, and evidence levels
- verify first-author papers for existing people nodes
- map funding / projects to directions if available

Expected output:

- correction table
- direction audit
- people audit
- core/other paper recommendation
- suggested local file updates

## Round 3 Prompt Goals

Ask for:

- recent papers from the last five years unless the user specifies otherwise
- about 30 new papers if the library already has about 10
- total paper set of about 20-40
- coverage of all stable major directions
- at least one first-author paper per RPG / possible group member where possible
- tags for every candidate paper
- recommended `core` or `other` placement by direction

Useful tags:

- `#direction/<direction-slug>`
- `#paper/core-candidate`
- `#paper/other`
- `#paper/review`
- `#paper/recent`
- `#people/current-rpg`
- `#people/graduated-rpg`
- `#people/first-author`
- `#evidence/official-profile`
- `#evidence/publisher`
- `#evidence/research-portal`
- `#status/unverified`

## Agent Checklist Before Writing Prompt

Read:

- `dashboard.md`
- relevant PI map in `06_maps/`
- `01_people/`
- `02_research_directions/`
- `03_papers/`
- latest relevant files in `00_inbox/`
- current prompt files in `08_outputs/`

Then decide the round:

- unstable identity/directions/people: Round 1
- existing but uncertain map: Round 2
- stable map needing more papers: Round 3

Every prompt should request:

- proposed node names
- evidence URLs
- confidence levels
- `status: unverified` for uncertain claims
- suggested folder target: `core` or `other`
- suggested tags
- suggested updates to people, direction, paper, map, and dashboard files
