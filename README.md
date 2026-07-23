# ChatArch Public Project Map

This repository backs the public GitHub Pages entry point for ChatArch:

```text
https://arch.gh.wzhecnu.cn/
```

This is the organization-level public project map and documentation hub. It must not become a landing page for a single package; individual projects are listed only as peer public repositories.

## Public-safety rule

Only public GitHub repositories are indexed. Private repositories, credentials, deployment details, and internal service URLs must not be added here.

## Generated state

- Public repositories indexed: 47
- Generated: 2026-07-23 17:05 UTC
- Shared docs route: `https://arch.gh.wzhecnu.cn/<ProjectName>/`
- Lowercase project aliases generated: 41
- Alias behavior: `/<projectname>/...` redirects to the canonical `/<ProjectName>/...` route when the public repo name uses mixed case.

## Local edit

Use the project script instead of editing generated files by hand, then regenerate aliases and validate:

```bash
python3 /Users/rexwzh/Playground/projects/chattea/07-14-chattea-dev-docs/scripts/generate_chatarch_pages_index.py \
  --repo-dir /Users/rexwzh/Playground/core/ChatArch.github.io
python3 scripts/generate_lowercase_aliases.py
python3 scripts/validate_site.py
```

## Automation

- `CI`: validates generated aliases, public-safety guards, and staged static output.
- `Preview Docs`: publishes PR previews to `https://arch.gh.wzhecnu.cn/dev/` from `gh-pages:/dev/` and comments the PR.
- `Deploy Docs`: publishes the formal site to `https://arch.gh.wzhecnu.cn/` from `gh-pages:/` after merge to `main` / `master`.
- GitHub Pages source should be `gh-pages` branch `/` once this workflow is enabled.
