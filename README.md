# ChatArch Public Project Map

This repository backs the public GitHub Pages entry point for ChatArch:

```text
https://arch.gh.wzhecnu.cn/
```

This is the organization-level public project map, recent project pulse, and documentation hub. It must not become a landing page for a single package; individual projects are listed only as peer public repositories.

## Public-safety rule

Only public GitHub repositories are indexed. Private repositories, credentials, deployment details, and internal service URLs must not be added here.

## Generated state

- Public repositories indexed: 72
- Generated: 2026-08-14 05:42 UTC
- Recent pulse timestamp: 2026-08-14 13:42 +08:00
- Shared docs route: `https://arch.gh.wzhecnu.cn/<ProjectName>/`
- Organization homepage route: `https://arch.gh.wzhecnu.cn/`
- Lowercase project aliases generated after each homepage update.
- Alias behavior: `/<projectname>/...` redirects to the canonical `/<ProjectName>/...` route when the public repo name uses mixed case.
- Curated system cards mark `Docs route pending` when the project's public Pages route was verified unavailable; the repository map still shows the conventional future route.

## Local edit

Use the active workspace/project generator or another public-metadata-only generator; do not edit private/internal names into generated files. After editing the homepage source, regenerate aliases and validate:

```bash
python3 scripts/generate_lowercase_aliases.py
python3 scripts/validate_site.py
python3 scripts/build_site.py --output site
```

## Automation

- `CI`: validates generated aliases, public-safety guards, and staged static output.
- `Preview Docs`: publishes PR previews to `https://arch.gh.wzhecnu.cn/dev/` from `gh-pages:/dev/` and comments the PR.
- `Deploy Docs`: publishes the formal site to `https://arch.gh.wzhecnu.cn/` from `gh-pages:/` after merge to `main` / `master`.
- GitHub Pages source should be `gh-pages` branch `/` once this workflow is enabled.
