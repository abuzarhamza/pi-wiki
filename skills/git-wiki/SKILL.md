---
name: git-wiki
description: Maintains documentation directly inside a Git repository, automatically updating pages based on code changes and git history. Use to keep documentation in sync with the codebase.
---

# Git Wiki Skill

This skill implements the "Documentation as Code" pattern, specifically tailored for Git repositories. It uses your Git history and codebase structure to ensure your `docs/wiki/` directory stays current.

## Setup

1.  **Initialize:**
    Navigate to your project root and initialize:
    ```bash
    /skill:git-wiki init
    ```
2.  **Configure Schema:**
    A `GIT_WIKI_SCHEMA.md` will be created in your root to define conventions for mapping code to docs.

## Operations

### Sync with Code
```bash
/skill:git-wiki sync
```
*Analyzes recent commits and code changes since the last sync. Automatically updates relevant doc pages in `docs/wiki/`.*

### Identify Purpose
```bash
/skill:git-wiki identify
```
*Analyzes the current wiki content and structure to generate or update `PURPOSE.md`. This explicitly defines what this wiki is tracking (e.g., Code Documentation, TODO Tracker, Project Roadmap).*

### Wiki Status/Audit
```bash
/skill:git-wiki status
```
*Compares your current documentation against the codebase structure. Identifies stale docs, undocumented modules, or missing cross-references.*

### Query Codebase
```bash
/skill:git-wiki query "How does the authentication flow work in this repo?"
```
*Synthesizes an answer by combining information from both the code and the wiki.*
