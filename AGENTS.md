# AGENTS.md
## Quickstart

1. **Install dependencies**
   ```bash
   uv install
   ```

2. **Build the site**
   ```bash
   uv run zensical build
   ```

3. **Serve locally**
   ```bash
   uv run zensical serve
   ```

## Common Tasks

- **Edit content**: Modify markdown files in `docs/` directory
- **Add new page**: Create `.md` file in `docs/` and add to navigation in `zensical.toml`
- **Change theme**: Modify `project.theme` section in `zensical.toml`

## Project Structure

- `docs/` - Markdown content files
- `site/` - Generated site files (output directory)
- `zensical.toml` - Site configuration

## Tips

- Use `uv` for dependency management
- Zensical handles all build/serve operations
- Theme customization via `zensical.toml`
- Navigation defined in `zensical.toml` nav section