# ChatArch Public Docs Hub

This repository backs the public GitHub Pages entry point for ChatArch:

```text
https://arch.gh.wzhecnu.cn/
```

Project documentation is expected to live under repository paths, for example:

```text
https://arch.gh.wzhecnu.cn/ChatTea/
```

The public homepage intentionally lists only public repositories. Private repositories, credentials, deployment details, and internal service URLs must not be added here.

## Local edit

Use the project script instead of editing generated files by hand:

```bash
python3 /Users/rexwzh/Playground/projects/chattea/07-14-chattea-dev-docs/scripts/generate_chatarch_pages_index.py \
  --repo-dir /Users/rexwzh/Playground/core/ChatArch.github.io
```
