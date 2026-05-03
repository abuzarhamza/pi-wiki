# Git Wiki Schema & Conventions

This file guides the LLM in maintaining repository documentation.

## Directory Structure
- `docs/wiki/`: Wiki pages (Markdown)
- `docs/wiki/PURPOSE.md`: Defines what this wiki tracks.
- `docs/wiki/index.md`: Main entry point
- `docs/wiki/assets/`: Documentation images

## Maintenance Rules
1. **Repository Aware:** Always check `git log` and `git diff` before updating docs.
2. **Code Mapping:** Every major module/feature in the codebase should have a corresponding page in `docs/wiki/`.
3. **Commit Association:** If a documentation update is triggered by a commit, mention the commit hash/summary in the wiki page metadata or the `CHANGELOG.md` inside `docs/wiki/`.
4. **Stale Check:** If a source file is deleted or renamed, update or archive the corresponding wiki page.
5. **YAML Frontmatter:**
  ```yaml
  ---
  title: Page Title
  associated_files: [path/to/code.ts]
  last_sync_commit: <hash>
  ---
  ```

## Workflows
- **Identify:** Analyze all `docs/wiki/*.md` -> Synthesize purpose -> Create/Update `PURPOSE.md`.
- **Sync:** Git analysis -> Compare code vs docs -> Apply changes -> Update index -> Suggest commit message for docs.
- **Status:** Scan codebase structure -> Validate links in `docs/wiki/` -> Report missing/stale documentation.
