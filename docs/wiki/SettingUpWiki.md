# Setting Up Your Wiki

To set up a wiki in your project using the `git-wiki` skill:

1. Ensure the `skills/git-wiki` directory exists in your project.
2. Navigate to your project root in the Pi interface.
3. Run the initialization command:
   ```bash
   /skill:git-wiki init
   ```
4. A `GIT_WIKI_SCHEMA.md` file will be created. Configure this file to define how your code maps to your documentation.
5. Once configured, sync your documentation:
   ```bash
   /skill:git-wiki sync
   ```
6. You can now use `/skill:git-wiki identify` to generate a `PURPOSE.md` file for your wiki.
