# Graph Rules

Use these rules when creating or repairing a Markdown/Obsidian research-group map.

## Directory Pattern

Recommended reusable structure:

```text
dashboard.md
00_inbox/
01_people/
  pi/
  rpg/
    current/
    graduated/
  coauthors/
02_research_directions/
03_papers/
  core/
    link/<Direction_Name>/core.md
    paper/
  other/
    link/<Direction_Name>/other.md
    paper/
06_maps/
07_templates/
08_outputs/
```

Adapt to the local project if it already has a different naming convention.

## Link Layers

Use layered graph edges:

```text
PI-specific map -> people
people -> directions
people -> first-author papers only
directions -> per-direction core/other link files
link files -> papers
papers -> people / citation metadata, but not direct direction links
```

The purpose is to prevent overview pages from turning into dense graph hubs.

## Map Files

- The PI-specific map file should link only to people.
- Keep dashboard files human-readable and high-level.
- If the local project says dashboard or timeline should not have structural links, remove Obsidian links from those files.
- Do not recreate deleted map files when a project has intentionally retired them.

## People Files

People files may link to:

- related directions
- first-author papers only when confirmed or strongly indicated
- important collaborators when the relationship is evidence-backed

Separate roles when the project supports subfolders:

- `01_people/pi/`
- `01_people/rpg/current/` for current RPGs / students
- `01_people/rpg/graduated/` for completed / graduated RPGs
- `01_people/rpg/` only as a temporary holding folder when RPG status has not yet been classified
- `01_people/coauthors/`

Do not infer advisor-student relationships from coauthorship alone.

## Direction Files

Direction files should link to:

- people active in the direction
- its own core link file
- its own other link file

Direction files should not directly list every paper as graph links if the project uses link files. Put paper links inside:

```text
03_papers/core/link/<Direction_Name>/core.md
03_papers/other/link/<Direction_Name>/other.md
```

## Paper Files

Paper files should include:

- citation
- year
- authors
- first author
- DOI / source
- why it matters
- connection to the group
- uncertainty

Do not link paper files directly back to directions when the project uses direction-specific link files. Use plain text direction names or frontmatter strings if needed.

## Link Files

Each direction has separate `core.md` and `other.md` link files. Keep their filenames exactly `core.md` and `other.md` when the local project requires that.

Use bullet links rather than Markdown tables to avoid broken Obsidian syntax:

```markdown
- [[2024_Author_Short_Title]]
- [[2026_Author_Short_Title]]
```

Avoid malformed links such as `[[Paper_Name` without closing `]]`.

## Core vs Other Papers

Core papers:

- normally 1-2 per direction
- high-impact venue, high citations, landmark contribution, or route-defining paper
- useful for explaining the group's identity

Other papers:

- useful supporting papers
- recent extensions
- papers that cover RPG first-author evidence
- papers that broaden but do not define the direction
