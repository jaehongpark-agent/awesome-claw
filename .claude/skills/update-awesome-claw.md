# Update awesome-claw

Skill for keeping the awesome-claw curated list up to date.

## Instructions

When the user invokes `/update-awesome-claw`, perform the following steps:

### 1. Discover New Entries
- Use web search to find new Claw-related projects, articles, security advisories, and tools released since the last update.
- Search queries to use:
  - `"claw" AI agent new project site:github.com`
  - `openclaw alternative 2026`
  - `openclaw security vulnerability CVE`
  - `AI agent platform self-hosted`
  - `MCP server claw integration`
  - `claw AI agent news`

### 2. Read Current README
- Read `README.md` in the repository root.
- Parse existing entries to avoid duplicates.

### 3. Identify Missing Items
- Compare discovered projects/articles against existing entries.
- Flag any entries that are:
  - **New** — not yet in the list
  - **Updated** — star counts significantly changed, projects renamed/archived
  - **Broken** — links that may no longer work

### 4. Update README.md
- Add new entries to the correct category following existing formatting:
  - Self-hosted platforms: use the table format with Name, Language, Stars, Key Feature
  - Articles: use the link list format with source and description
  - Security: add new CVEs or advisories with verifiable sources
- Move projects between tiers if star counts have changed significantly.
- Remove or mark archived/dead projects.

### 5. Verify Links
- For each new link added, use `WebFetch` to verify the URL is reachable.
- Flag any broken links found in existing entries.

### 6. Present Changes
- Show a summary of all changes made:
  - New entries added (with category)
  - Entries updated (what changed)
  - Broken links found
  - Entries removed or archived
- Ask the user to review the changes before committing.

### 7. Commit & Push (with user confirmation)
- After user approval, stage changes, commit with a descriptive message, and push.
- Commit message format: `update: add [N] new entries, update [M] existing ([date])`

## Notes
- Always preserve the existing structure and formatting of README.md.
- When in doubt about categorization, ask the user.
- Star counts should be approximate (e.g., "2.3K" not "2,347").
- Only add projects that are relevant to the Claw ecosystem (always-on AI agents, not one-shot scripts).
